# Этап 4. Базы данных и доступ к данным

**Длительность:** 1–2 месяца.

**Цель этапа:** научиться работать с данными без ботяня порога в проде. Джун пишет LINQ-запросы и надеется, что EF Core всё придумает. Мидл читает plan execution и знает, почему запрос работает именно за такое время.# Этап 4. Базы данных и доступ к данным

**Длительность:** 1–2 месяца.

**Цель этапа:** научиться работать с данными без бутылочного горлышка в проде. Джун пишет LINQ и надеется, что EF Core всё придумает. Мидл читает execution plan и знает, почему запрос работает именно столько времени.

## SQL на уровне уверенного владения

База без знания SQL — это карго-культ.

- JOIN всех типов с пониманием, какой когда нужен.
- Подзапросы, CTE (`WITH`), рекурсивные CTE.
- Оконные функции: `ROW_NUMBER`, `RANK`, `LAG`/`LEAD`, `SUM() OVER (PARTITION BY ...)`.
- Группировка, `HAVING`, `GROUPING SETS`, `ROLLUP`, `CUBE`.
- Транзакции и уровни изоляции: Read Uncommitted, Read Committed, Repeatable Read, Serializable, Snapshot. Что такое phantom read, dirty read, non-repeatable read.
- Блокировки: shared, exclusive, update, intent. Deadlock и его диагностика.

Ресурсы:

- [Use the Index, Luke](https://use-the-index-luke.com/) — бесплатно онлайн, лучший материал по индексам.
- «SQL Antipatterns» Bill Karwin.
- «SQL Performance Explained» Markus Winand.

## Индексы и планы выполнения

Самая частая причина медленных запросов в проде.

- Clustered vs non-clustered индекс.
- Covering index, included columns, фильтрованные индексы.
- Когда индекс не помогает: leading column violation, функции в WHERE, OR-условия, низкая селективность.
- Page splits, fillfactor, fragmentation, перестроение индексов.
- Чтение плана выполнения: seek vs scan, hash join vs nested loop vs merge join, key lookup, RID lookup.
- Statistics и cardinality estimation.

Практика: возьмите таблицу на миллион строк, напишите 5 типичных запросов, замерьте время с индексами и без, прочитайте план каждого, объясните разницу.

## PostgreSQL и SQL Server

Достаточно знать одну СУБД хорошо. PostgreSQL чаще встречается в новых проектах, SQL Server в энтерпрайзе и legacy.

**PostgreSQL специфика:**

- MVCC и VACUUM. Почему таблица «разбухает» и как с этим бороться.
- TOAST для больших значений.
- JSON и JSONB, GIN-индексы по ним.
- Расширения: pg_stat_statements, pg_trgm, postgis, pgvector.
- Партиционирование, declarative partitioning.

**SQL Server специфика:**

- Query Store для анализа регрессий.
- Extended Events вместо устаревшего SQL Profiler.
- Columnstore индексы для аналитики.
- Always On Availability Groups.
- TempDB и его конфигурация под нагрузку.

## Entity Framework Core

Главный инструмент доступа к данным в .NET. И главный источник проблем у тех, кто не понимает, что он генерирует.

- Change tracking: как работает, когда отключать через `AsNoTracking()`.
- Lazy, eager (`Include`, `ThenInclude`), explicit loading. Когда что использовать.
- Проблема N+1: как находить (логирование SQL), как устранять.
- Compiled queries для горячих путей.
- Split queries vs single queries при `Include`.
- Миграции: `Add-Migration`, `Update-Database`, ручное редактирование, idempotent scripts для прода.
- Value converters, owned types, table splitting.
- Global query filters для soft delete и multi-tenancy.
- `ExecuteUpdate` и `ExecuteDelete` (EF Core 7+) для bulk-операций без change tracking.
- Interceptors: `SaveChangesInterceptor`, `DbCommandInterceptor`.

Ресурс: [официальная документация EF Core](https://learn.microsoft.com/en-us/ef/core/), особенно раздел Performance.

Антипаттерны:

- `SaveChanges()` в цикле вместо batch-вставки.
- Загрузка всей таблицы в память через `.ToList()` перед фильтрацией.
- Использование `.Include()` там, где хватило бы projection в DTO.
- Доверие к EF в генерации сложных запросов. На определённой сложности проще написать SQL.

## Dapper и raw ADO.NET

Для горячих путей и сложных запросов EF не подходит. Альтернативы:

- **Dapper** — тонкая обёртка над ADO.NET. Сами пишете SQL, Dapper маппит результат.
- **Raw ADO.NET** через `DbConnection`, `DbCommand`, `DbDataReader`. Максимальный контроль, максимальная скорость, максимальное количество кода.

Хороший подход в проектах: EF Core для команд (write), Dapper для запросов (read). Это естественный путь к CQRS.

## Кеширование

- **IMemoryCache** для in-process кеша. Прост, но не работает в multi-instance деплое.
- **IDistributedCache + Redis** для распределённого кеша.
- Стратегии invalidation: TTL, write-through, write-behind, cache-aside.
- Cache stampede и его предотвращение через locks или semaphore.
- HybridCache (новый в .NET 9) — двухуровневый кеш с защитой от stampede из коробки.

## NoSQL: когда оно действительно нужно

- **MongoDB**, **Cosmos DB**: документные базы, удобны для агрегатов в стиле DDD.
- **Redis** не только кеш, но и Pub/Sub, Streams, lock-сервис.
- **Elasticsearch / OpenSearch** для полнотекстового поиска и log analytics.
- **ClickHouse** для аналитики на колоночных данных.
- **TimescaleDB / InfluxDB** для time-series.

NoSQL — не «современная замена SQL», а другой инструмент с другими trade-off. По умолчанию берите PostgreSQL и переходите на NoSQL, когда есть конкретная причина.

## Чек-лист готовности к Этапу 5

- [ ] Прочитаю любой execution plan и объясню, почему запрос медленный.
- [ ] Создам covering index под конкретный запрос и докажу замерами выигрыш.
- [ ] Объясню разницу между Read Committed и Snapshot Isolation.
- [ ] Найду и устраню N+1 в чужом коде, покажу до/после через логи SQL.
- [ ] Опишу проблему cache stampede и приведу два способа её решения.
- [ ] Напишу миграцию EF Core, безопасную для прода (обратно совместимая, без блокировок).
- [ ] Выберу между EF Core, Dapper и raw ADO.NET для конкретной задачи с обоснованием.

## Практическое задание этапа

Возьмите учебный проект с одной из публичных БД (например, Northwind или Chinook) и реализуйте:

1. CRUD на EF Core с миграциями.
2. Один сложный отчёт через Dapper с оконными функциями.
3. Двухуровневый кеш (память + Redis) для самого тяжёлого read-запроса.
4. Нагрузочный тест через k6 на 100 RPS. Найдите N+1, исправьте, замерьте разницу.
5. Документ `PERFORMANCE.md` в репозитории: что было, что стало, какие индексы добавили, какие планы изменились.

Это задание заменяет десять курсов по EF Core.

---

[← К списку этапов](README.md) · [Этап 3 ←](03-tooling.md) · [→ Этап 5](05-aspnetcore.md)
