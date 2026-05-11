# C# Roadmap: с нуля до профи

![Stars](https://img.shields.io/github/stars/Develp10/Csharp_Roadmap?style=social) ![Forks](https://img.shields.io/github/forks/Develp10/Csharp_Roadmap?style=social) ![License](https://img.shields.io/badge/license-MIT-green) ![.NET](https://img.shields.io/badge/.NET-8%20LTS%20%7C%209-512BD4?logo=dotnet) ![Language](https://img.shields.io/badge/lang-RU-blue)

Практическое руководство по росту в C#-разработке. Материал собран для тех, кто хочет получить инженерную глубину, а не просто накликать CRUD по туториалам. Здесь последовательность изучения, лучшие практики, ресурсы и трезвый разбор того, как работать с ИИ-инструментами и оставаться востребованным.

> Roadmap живой. PR с уточнениями, ссылками и опытом приветствуются. См. раздел [Contributing](#contributing).

---

## Как пользоваться этим roadmap

- Не пытайтесь пройти всё подряд за квартал. Это карта на 3–5 лет осознанной работы.
- Этапы 1–8 — базовая траектория от джуна до уверенного мидла. Идите по порядку.
- Этапы 9–17 — специализация и Senior+. Берите то, что нужно вашему рынку и продукту.
- Каждый этап = чтение + конспект + рабочий проект + ретроспектива. Без проекта тема не считается пройденной.
- Возвращайтесь к ранее пройденному раз в полгода: фундамент меняет смысл, когда вы выросли.
- Отмечайте прогресс в форке этого репозитория. Публичный коммит-стрик дисциплинирует лучше любого ментора.

## Оглавление

- [Зачем учить код в эпоху ИИ](#зачем-учить-код-в-эпоху-ии)
- [Этап 1. Фундамент языка и платформы](#этап-1-фундамент-языка-и-платформы-12-месяца)
- [Этап 2. Глубже в платформу .NET](#этап-2-глубже-в-платформу-net-12-месяца)
- [Этап 3. Инструменты профессионала](#этап-3-инструменты-профессионала-параллельно-с-этапом-2)
- [Этап 4. Базы данных и доступ к данным](#этап-4-базы-данных-и-доступ-к-данным-12-месяца)
- [Этап 5. ASP.NET Core и веб-разработка](#этап-5-aspnet-core-и-веб-разработка-23-месяца)
- [Этап 6. Архитектура и проектирование](#этап-6-архитектура-и-проектирование-постоянно)
- [Этап 7. Качество кода и тестирование](#этап-7-качество-кода-и-тестирование-постоянно)
- [Этап 8. Облака и эксплуатация](#этап-8-облака-и-эксплуатация-12-месяца)
- [Этап 9. Специализация](#этап-9-специализация)
- [Этап 10. Глубокая производительность](#этап-10-глубокая-производительность-и-системное-программирование)
- [Этап 11. Распределённые системы](#этап-11-распределённые-системы-продвинутого-уровня)
- [Этап 12. Платформенная инженерия](#этап-12-платформенная-инженерия)
- [Этап 13. DDD на практике](#этап-13-доменно-управляемое-проектирование-на-практике)
- [Этап 14. Расширение стека](#этап-14-расширение-стека-за-пределы-c)
- [Этап 15. ML и AI-инженерия](#этап-15-ml-и-ai-инженерия-в-net-стеке)
- [Этап 16. Open source и техническое лидерство](#этап-16-open-source-и-техническое-лидерство)
- [Этап 17. Бизнес-контекст](#этап-17-бизнес-контекст-и-продуктовое-мышление)
- [Этап 18. DevSecOps и Supply Chain Security](#этап-18-devsecops-и-supply-chain-security)
- [Этап 19. Documentation as Code](#этап-19-documentation-as-code-и-инженерное-письмо)
- [Этап 20. Устойчивая карьера и этика](#этап-20-устойчивая-карьера-этика-и-долгая-игра)
- [Лучшие практики](#лучшие-практики-которые-экономят-годы)
- [Как работать с ИИ-инструментами](#как-работать-с-ии-инструментами-и-не-деградировать)
- [Чек-лист готовности к уровням](#чек-лист-готовности-к-уровням)
- [Антипаттерны обучения](#антипаттерны-обучения-чего-избегать)
- [Минимальная книжная полка](#минимальная-книжная-полка)
- [Awesome-ресурсы и сообщества](#awesome-ресурсы-и-сообщества)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

---

## Зачем учить код в эпоху ИИ

ИИ генерирует текст, похожий на код. Инженер отвечает за то, чтобы система держала нагрузку, не теряла деньги клиента и не падала ночью в проде. Языковая модель не знает контекст вашего бизнеса, не читает требования между строк, не несёт ответственности за архитектурное решение, которое будет жить пять лет.

Чтобы пользоваться ИИ как рычагом, нужно понимать, что он сгенерировал. Видеть гонки в async-коде, отличать рабочий паттерн от карго-культа, читать legacy и проектировать модули так, чтобы их можно было поддерживать. Без фундамента вы будете нажимать Tab в Copilot и копить технический долг, который потом сами не разгребёте.

Рынок смещается от джунов, штампующих формочки, к инженерам уровня middle+, которые проектируют системы и валидируют ИИ-вывод. Учиться нужно глубже, чем раньше, а не поверхностнее.

---

## Этап 1. Фундамент языка и платформы (1–2 месяца)

Установите актуальный .NET SDK (LTS — .NET 8, текущий релиз — .NET 9), JetBrains Rider или Visual Studio. VS Code с расширением C# Dev Kit тоже рабочий вариант для тех, кто привык к лёгкому редактору.

Что осваиваем на этом этапе:

* Синтаксис C#: типы значений и ссылок, nullable reference types, pattern matching, records, init-only свойства, switch expressions.
* Управляющие конструкции, методы, перегрузки, опциональные и именованные аргументы.
* ООП по делу: инкапсуляция, наследование, полиморфизм, интерфейсы, абстрактные классы. Понимание, когда композиция предпочтительнее наследования.
* Generics, ограничения типов, ковариантность и контравариантность.
* Делегаты, события, лямбда-выражения, замыкания и их подводные камни.
* Исключения: иерархия, when-фильтры, finally, корректное пробрасывание без потери стека (throw vs throw ex).
* Базовая работа с коллекциями: List, Dictionary, HashSet, Queue, Stack, ImmutableCollections.
* LINQ to Objects: deferred execution, материализация, типичные ошибки производительности.

Ресурсы:

* Книга «C# in Depth» Jon Skeet — обязательный минимум для понимания языка.
* Официальная документация Microsoft Learn по C# и .NET.
* Канал Nick Chapsas на YouTube для коротких практических разборов.
* Курс «C# Fundamentals» на Pluralsight (Scott Allen).

Практика: написать консольное приложение средней сложности (например, текстовый менеджер задач с сохранением в JSON), решить 50–100 задач на LeetCode или Codewars на C#.

---

## Этап 2. Глубже в платформу .NET (1–2 месяца)

Здесь начинается то, что отличает джуна от мидла. Нужно понимать, как именно ваш код выполняется.

Темы:

* CLR, JIT, AOT, Tiered Compilation, ReadyToRun.
* Управление памятью: стек, куча, поколения GC, Large Object Heap, Server vs Workstation GC.
* Span<T>, Memory<T>, ref struct, stackalloc и зачем они нужны.
* Async/await изнутри: SynchronizationContext, ConfigureAwait, ValueTask, отмена через CancellationToken, ловушки sync-over-async и async void.
* Thread, ThreadPool, Task, Parallel, Channels, примитивы синхронизации (lock, SemaphoreSlim, Interlocked, ReaderWriterLockSlim).
* Reflection, атрибуты, Source Generators (современная альтернатива рефлексии в горячих путях).
* IO: потоки, Pipelines, асинхронные файловые операции.
* Сериализация: System.Text.Json, контракты, кастомные конвертеры, производительность по сравнению с Newtonsoft.Json.

Ресурсы:

* «Pro .NET Memory Management» Konrad Kokosa — глубокое погружение в GC.
* «Concurrency in C# Cookbook» Stephen Cleary.
* Блог Stephen Toub на devblogs.microsoft.com — лучший источник по производительности и async.
* Канал Nick Chapsas, серии по производительности.

Практика: написать свой LRU-кеш, простой пул объектов, измерить производительность через BenchmarkDotNet.

---

## Этап 3. Инструменты профессионала (параллельно с этапом 2)

Без этих инструментов не возьмут на сильную команду:

* Git: branching strategies (trunk-based, GitHub Flow), rebase, cherry-pick, разрешение конфликтов, работа с большими репозиториями.
* Командная строка, базовый Bash или PowerShell.
* Docker: образы, слои, multi-stage builds, docker-compose, сетевые режимы.
* Linux на уровне уверенного пользователя: процессы, права, systemd, логирование.
* CI/CD: GitHub Actions или Azure DevOps Pipelines.
* Отладка: дампы памяти, dotnet-dump, dotnet-counters, dotnet-trace, PerfView.
* BenchmarkDotNet для измерения производительности и опровержения собственных интуиций.

Ресурсы:

* Pro Git book (бесплатно на git-scm.com).
* «Docker Deep Dive» Nigel Poulton.
* Microsoft Learn по диагностике .NET-приложений.

---

## Этап 4. Базы данных и доступ к данным (1–2 месяца)

* SQL на уровне уверенного владения: JOIN, подзапросы, оконные функции, индексы, планы выполнения, транзакции и уровни изоляции.
* PostgreSQL и SQL Server в качестве основных СУБД.
* Entity Framework Core: change tracking, lazy/eager/explicit loading, проблема N+1, AsNoTracking, compiled queries, миграции.
* Dapper и raw ADO.NET для горячих путей и сложных запросов.
* Redis для кеширования и очередей.
* Базово NoSQL: MongoDB или Cosmos DB, понимание, когда они уместны.

Ресурсы:

* «SQL Antipatterns» Bill Karwin.
* «Use the Index, Luke» (бесплатно онлайн) — лучший материал по индексам.
* Документация EF Core с разделом про производительность.

Практика: написать сервис, который грузит миллион записей из БД, найти и устранить N+1, замерить разницу.

---

## Этап 5. ASP.NET Core и веб-разработка (2–3 месяца)

* Kestrel, middleware pipeline, DI-контейнер, конфигурация и Options pattern.
* Minimal APIs и контроллеры, когда что выбирать.
* Аутентификация и авторизация: JWT, OAuth 2.0, OpenID Connect, Identity, политики и роли.
* Валидация (FluentValidation), маппинг (Mapster, ручной маппинг вместо AutoMapper в новых проектах).
* Логирование через ILogger, структурированные логи, Serilog, OpenTelemetry для трейсинга и метрик.
* gRPC, SignalR, GraphQL (HotChocolate) обзорно, под задачи.
* Версионирование API, Swagger/OpenAPI, идемпотентность, обработка ошибок (ProblemDetails).
* Health checks, graceful shutdown, конфигурация через переменные окружения и секрет-сторы.

Ресурсы:

* «ASP.NET Core in Action» Andrew Lock.
* Блог Andrew Lock (andrewlock.net) — глубокие разборы внутренностей.
* Документация Microsoft по ASP.NET Core.

Практика: построить API для задач с аутентификацией, ролями, логированием, контейнеризацией и деплоем в облако.

---

## Этап 6. Архитектура и проектирование (постоянно)

* SOLID без фанатизма, понимание реальной цены каждого принципа.
* DDD: агрегаты, value objects, bounded contexts, ubiquitous language. Читать «Domain-Driven Design» Эванса и «Implementing DDD» Вернона.
* Clean Architecture, Hexagonal, Onion. Уметь объяснить, какую проблему решает каждая.
* CQRS и MediatR, Event Sourcing (понимать, когда уместно).
* Паттерны интеграции: Outbox, Saga, Idempotency Key, Retry с exponential backoff, Circuit Breaker (Polly).
* Микросервисы vs модульный монолит. По умолчанию строим модульный монолит, к микросервисам переходим осознанно.
* Очереди и брокеры: RabbitMQ, Kafka, Azure Service Bus. MassTransit как абстракция.
* Распределённые транзакции, eventual consistency, CAP-теорема на практике.

Ресурсы:

* «Designing Data-Intensive Applications» Martin Kleppmann — главная книга десятилетия для бэкендера.
* «Building Microservices» Sam Newman.
* Блог Vladimir Khorikov (enterprisecraftsmanship.com).
* Канал CodeOpinion (Derek Comartin).

---

## Этап 7. Качество кода и тестирование (постоянно)

* Unit-тесты: xUnit, NUnit. FluentAssertions для читаемых ассертов.
* Моки: NSubstitute или Moq. Чрезмерное моканье сигнализирует о проблемах архитектуры.
* Интеграционные тесты через WebApplicationFactory и Testcontainers (поднимаем реальный Postgres в Docker для тестов).
* Подходы: TDD там, где есть смысл; Arrange-Act-Assert; Given-When-Then.
* Property-based тестирование (FsCheck) для алгоритмов.
* Code review культура, статический анализ (Roslyn analyzers, SonarQube), EditorConfig.
* Покрытие: важно не число процентов, а покрытие критичных путей.

Ресурсы:

* «Unit Testing: Principles, Practices, and Patterns» Vladimir Khorikov.
* «The Art of Unit Testing» Roy Osherove.

---

## Этап 8. Облака и эксплуатация (1–2 месяца)

* Azure или AWS на уровне сертификации Associate. Для .NET-стека Azure ближе, но AWS тоже даёт работу.
* Kubernetes основы: Pod, Deployment, Service, Ingress, ConfigMap, Secret, Helm.
* Observability: метрики (Prometheus, Application Insights), трейсинг (Jaeger, OpenTelemetry), логи (Loki, ELK).
* Infrastructure as Code: Terraform или Bicep.
* Безопасность: OWASP Top 10, секрет-менеджмент, безопасное хранение токенов, защита от SQL injection и SSRF.

---

## Этап 9. Специализация

После прохождения базы выбираем углубление:

* Высоконагруженный бэкенд: производительность, low-allocation код, Span<T>, профилирование.
* Распределённые системы: Kafka, Event Sourcing, CQRS в проде.
* Геймдев: Unity, ECS, оптимизация под платформы.
* Десктоп: WPF, Avalonia, MAUI.
* DevOps-направление в .NET-командах.
* ML.NET и интеграция ИИ в продукты на C#.

---

## Лучшие практики, которые экономят годы

* Пишем код для чтения, а не для написания. Ваш код прочитают в десять раз чаще, чем напишут.
* Простое решение по умолчанию. Усложняем только когда требование подтверждено реальностью, а не воображением.
* Никаких god-объектов и магических чисел. Конфигурация выносится в Options, константы в именованные поля.
* Логи структурированные, с корреляцией запросов. Без этого диагностика в проде превращается в гадание.
* Никогда не ловим Exception молча. Либо обрабатываем осмысленно, либо пробрасываем.
* CancellationToken пробрасываем во все async-методы по умолчанию.
* Не используем .Result и .Wait() в async-коде. Это путь к дедлокам.
* DI без сервис-локатора. Зависимости приходят через конструктор, явно.
* Контракты API стабильны, ломающие изменения через версионирование.
* Миграции БД обратно совместимы. Сначала добавляем колонку, потом деплоим код, потом удаляем старое.
* Перед оптимизацией измеряем. BenchmarkDotNet, профайлер, метрики прода.

---

## Как работать с ИИ-инструментами и не деградировать

ИИ-инструменты ускоряют рутину и экономят часы на бойлерплейте. Они же убивают навыки, если использовать их вместо мышления.

Что использовать:

* **GitHub Copilot** или **Cursor** в редакторе для автодополнения и быстрой генерации шаблонного кода.
* **JetBrains AI Assistant** для тех, кто живёт в Rider.
* **Claude** и **ChatGPT** для проектирования, разбора чужого кода, объяснения сложных концепций, ревью архитектурных решений.
* **Claude Code** или **Codex CLI** для агентных задач: рефакторинг, миграции, генерация тестов на больший объём.
* **Supermaven** или **Codeium** как альтернативы Copilot.
* **Perplexity** для поиска по документации и свежим обсуждениям.

Принципы здоровой работы с ИИ:

* Каждый сгенерированный кусок проходит через ваше понимание. Если не можете объяснить, что делает строчка, не коммитьте её.
* ИИ хорош для бойлерплейта, миграций, тестов, документации, объяснений. ИИ слаб в архитектуре, в работе с уникальным доменом, в проде под нагрузкой.
* Просите модель объяснить альтернативы и риски, а не только дать решение.
* Не передавайте в публичные модели проприетарный код и секреты. Используйте корпоративные инстансы или локальные модели.
* Раз в неделю решайте задачу без ИИ полностью. Это держит мышцы в тонусе.
* Учите фундамент глубже, чем раньше. Поверхностные навыки автоматизируются первыми.

---

## Как оставаться актуальным

Технологии меняются, но базовые навыки (алгоритмы, проектирование, коммуникация, чтение чужого кода) живут десятилетиями. Стратегия долгой карьеры:

* Раз в квартал читаем одну серьёзную книгу по фундаменту (DDIA, Clean Architecture, книги Скита и Клеппмана).
* Подписка на блоги: devblogs.microsoft.com, Andrew Lock, Vladimir Khorikov, Steve Gordon, Konrad Kokosa, Stephen Cleary.
* Отслеживаем релизы .NET и C# на GitHub: dotnet/runtime, dotnet/aspnetcore.
* Pet-проекты, в которых пробуем то, что пока не дают на работе.
* Контрибьютим в open source. Один принятый PR в популярную библиотеку учит больше, чем десять курсов.
* Конференции: .NET Conf, NDC, DotNext. Записи бесплатно на YouTube.
* Менторство и доклады. Объяснение материала вскрывает дыры в понимании быстрее всего.

---

## Чек-лист готовности к уровням

**Junior**: уверенно пишет на C#, знает основы ASP.NET Core, работает с EF Core, понимает Git, покрывает код тестами, читает чужой код без паники.

**Middle**: проектирует модули, понимает async и память, пишет производительный код, разбирается в SQL и индексах, настраивает CI/CD, проводит code review, обоснованно выбирает между подходами.

**Senior**: проектирует системы, видит технический долг и умеет его выплачивать, разбирается в распределённых системах, работает с продом и инцидентами, менторит команду, влияет на технические решения за пределами своего модуля.

**Lead/Staff**: формирует техническую стратегию, выбирает стек, выстраивает процессы качества, общается с бизнесом на их языке, отвечает за результат, а не за код.

---

## Минимальная книжная полка

* Jon Skeet, «C# in Depth»
* Stephen Cleary, «Concurrency in C# Cookbook»
* Andrew Lock, «ASP.NET Core in Action»
* Konrad Kokosa, «Pro .NET Memory Management»
* Martin Kleppmann, «Designing Data-Intensive Applications»
* Vladimir Khorikov, «Unit Testing: Principles, Practices, and Patterns»
* Eric Evans, «Domain-Driven Design»
* Robert Martin, «Clean Code» и «Clean Architecture» (с критическим взглядом)
* Sam Newman, «Building Microservices»

---

Этот roadmap не догма. Подстраивайте под свои задачи и интересы, но не пропускайте фундамент ради модного фреймворка. 

---

## Soft skills и инженерная коммуникация

Технические навыки открывают дверь, soft skills двигают карьеру. Без них синьором не стать, какие бы алгоритмы вы ни знали.

* Писать ясные RFC и ADR. Архитектурное решение должно быть описано так, чтобы команда через год поняла, почему сделано именно так.
* Разбивать большие задачи на инкременты, которые можно влить за день. Pull request на 2000 строк никто не прочитает осмысленно.
* Code review как диалог, а не как война. Комментарии разделяем на blocking, suggestion и nitpick. Объясняем причину, не только указываем на проблему.
* Оценка задач без героизма. Закладываем буфер на отладку и неизвестное, не обещаем нереальные сроки под давлением.
* Грамотные постмортемы без поиска виноватых. Фиксируем системные причины, а не имена.
* Работа с менеджером и продуктом. Уметь объяснить технический долг через бизнес-метрики (потери выручки, риск инцидента, скорость доставки фич).
* Менторство. Обучая джунов, вы шлифуете собственное понимание и зарабатываете доверие команды.

Ресурсы:

* «The Pragmatic Programmer» Hunt, Thomas.
* «A Philosophy of Software Design» John Ousterhout.
* «Staff Engineer» Will Larson, «The Staff Engineer's Path» Tanya Reilly для уровня выше синьора.
* Блог Will Larson (lethain.com).

---

## Алгоритмы и подготовка к собеседованиям

В .NET-сегменте секции с алгоритмами встречаются реже, чем в FAANG, но в крупных компаниях и продуктовых стартапах их любят. Готовиться нужно осознанно.

* LeetCode, разбор по темам: массивы, two pointers, sliding window, hashmap, стеки, очереди, деревья, графы, DP, бинарный поиск, жадные алгоритмы.
* Решаем задачи на C#, не на Python. Тренируем именно тот синтаксис, который пригодится на интервью.
* Системный дизайн: HTTP, кеширование, шардирование, репликация, очереди, выбор хранилища под профиль нагрузки. Книга «System Design Interview» Alex Xu, канал «Hussein Nasser» на YouTube.
* Поведенческие интервью: метод STAR, заранее заготовленные истории про конфликты, провалы, инциденты и выученные уроки.
* Mock-интервью с коллегами и на pramp.com или interviewing.io.
* Подготовка резюме под рынок: CV на одну страницу, цифры и результаты, не должностные обязанности.

Минимальный набор для уверенного прохождения: 150–200 решённых задач на LeetCode (Easy 30%, Medium 60%, Hard 10%), 5–10 разобранных кейсов системного дизайна, 10 готовых поведенческих историй.

---

## Безопасность приложений на практике

Безопасность не отдельная роль, а часть работы каждого разработчика. Базовый минимум, ниже которого опускаться нельзя:

* OWASP Top 10 наизусть с примерами на C#: SQL injection, XSS, CSRF, SSRF, broken access control, insecure deserialization.
* Хранение паролей через Argon2id или PBKDF2. Никогда не пишем свою криптографию, используем System.Security.Cryptography и проверенные библиотеки.
* JWT правильно: короткий access token, refresh token в httpOnly cookie, ротация ключей, валидация issuer и audience.
* Секреты в Azure Key Vault, AWS Secrets Manager или HashiCorp Vault. В git попадать им нельзя; настраиваем pre-commit хуки и git-secrets.
* Защита от race conditions в денежных операциях через optimistic concurrency или distributed locks (Redis, ZooKeeper).
* Rate limiting на уровне API Gateway или middleware. Защита от bruteforce и DDoS базового уровня.
* Безопасные дефолты в ASP.NET Core: HTTPS Redirection, HSTS, антифорджери токены, Content Security Policy.
* Регулярный аудит зависимостей через dotnet list package --vulnerable, Dependabot, Snyk.
* Threat modeling по STRIDE на этапе проектирования, а не после инцидента.

Ресурсы:

* «Web Application Security» Andrew Hoffman.
* OWASP ASVS как чек-лист для review.
* Курсы PortSwigger Web Security Academy, бесплатно.

---

## Производительность и работа в проде

Разница между мидлом и синьором часто видна именно в проде, когда нужно найти и исправить проблему под нагрузкой.

* BenchmarkDotNet для микробенчмарков. Понимать разницу между nanoseconds, allocations и Tiered JIT прогревом.
* Профилирование живого приложения: dotMemory, dotTrace, PerfView, Visual Studio Diagnostics. Чтение flame graphs.
* Анализ дампов памяти через dotnet-dump и WinDbg с расширением SOS. Поиск утечек, deadlocks, GC pressure.
* Сетевые проблемы: tcpdump, Wireshark, dotnet-trace для HttpClient.
* Кеширование на трёх уровнях: in-memory (IMemoryCache), distributed (Redis), CDN. Понимание cache invalidation как одной из двух сложных задач в CS.
* Connection pooling для БД и HTTP. IHttpClientFactory вместо ручного создания HttpClient.
* Graceful degradation: circuit breakers, fallback responses, bulkhead isolation через Polly.
* Capacity planning: понимание throughput, latency percentiles (p50, p95, p99), little's law.
* Чтение метрик прода ежедневно. Дашборды должны быть открыты, а не только при инциденте.

Практика: возьмите своё ASP.NET Core приложение, прогоните через k6 или Bombardier с нагрузкой 1000 RPS, найдите бутылочное горлышко и устраните его. Повторите три раза.

Ресурсы:

* «Pro .NET Benchmarking» Andrey Akinshin.
* «Writing High-Performance .NET Code» Ben Watson.
* Блог Ben Adams и его доклады по оптимизации Kestrel.

---

## Карьерная траектория и деньги

Honest talk о том, как растёт зарплата и что выбирать на каждом шаге.

* Первая работа важнее зарплаты. Идите туда, где сильная команда и есть кому учить, даже если предложение по деньгам слабее. Через два года разница окупится десятикратно.
* Смена работы раз в 1.5–3 года даёт больший прирост дохода, чем повышения внутри. Это рыночная реальность, а не лояльность к компании.
* Аутсорс vs продукт vs стартап vs корпорация. У каждого свой профиль роста: аутсорс прокачивает разнообразие технологий, продукт глубину домена, стартап ответственность и широту, корпорация процессы и масштаб.
* Удалёнка и релокейт расширяют рынок. Английский на уровне B2 умножает доступные вакансии в разы.
* Trade-off менеджмент vs IC (individual contributor). На senior уровне можно выбрать путь staff/principal без перехода в менеджеры. Не все хотят быть тимлидами, и это нормально.
* Зарплатная вилка обсуждается с цифрами рынка на руках. Levels.fyi, Glassdoor, локальные обзоры по .NET.
* Финансовая подушка на 6–12 месяцев расходов даёт переговорную силу. Без подушки приходится соглашаться на первое предложение.
* Pet-проекты, open source, выступления и статьи поднимают цену на рынке быстрее, чем ещё один сертификат.

Что не работает:

* Бесконечное прохождение курсов без проектов. Сертификат без работающего кода в портфолио ничего не стоит.
* Прыжки между языками каждые полгода. Рынок платит за глубину, а не за длинный список технологий в резюме.
* Работа в одной компании 10 лет на одной роли. Стек устареет, и выйти будет тяжело.
Фреймворки сменятся через пять лет, понимание памяти, конкурентности и проектирования останется.

---

## Этап 10. Глубокая производительность и системное программирование

Уровень, на котором вы пишете код, конкурирующий по скорости с C++ и Rust. Нужно, если работаете в трейдинге, игровых движках, базах данных, ML-инфраструктуре, реальном времени.

* SIMD и векторизация через System.Numerics.Vector, Vector256, Vector512. Intrinsics из System.Runtime.Intrinsics для AVX, SSE, NEON.
* unsafe код, fixed buffers, работа с указателями. Понимание, когда это оправдано, а когда стрелять себе в ногу.
* Hardware intrinsics, prefetching, выравнивание данных по cache line, false sharing и его измерение.
* Memory layout: StructLayout, LayoutKind.Sequential vs Explicit, padding, упаковка структур.
* Lock-free структуры данных: Interlocked, volatile, memory barriers, модель памяти .NET (release/acquire semantics).
* Кастомные аллокаторы, ArrayPool, MemoryPool, RecyclableMemoryStream.
* Native AOT: ограничения, размер бинарника, startup time, тестирование совместимости рефлексии.
* Профилирование на уровне CPU: Intel VTune, AMD uProf, чтение perf counters, IPC, branch misprediction, cache misses.
* Заводить дружбу с дизассемблером. SharpLab, Disasmo для просмотра JIT-кода.

Ресурсы:

* «Pro .NET Performance» Sasha Goldshtein.
* «Mechanical Sympathy» Martin Thompson, доклады с QCon.
* Блог EgorBo (egorbogatov.com) про оптимизации в RyuJIT.
* Доклады Federico Andres Lois на DotNext про low-latency.

Практика: написать структуру данных, которая обгоняет System.Collections аналог на 30% по выбранной метрике, доказать измерениями.

---

## Этап 11. Распределённые системы продвинутого уровня

Когда модульный монолит уже не справляется и нужно строить настоящие распределённые системы. Сложность растёт нелинейно с числом узлов.

* Теория: модель FLP impossibility, CAP подробно, PACELC, теорема Брюера. Согласованность: linearizable, sequential, causal, eventual.
* Алгоритмы консенсуса: Paxos, Raft, Multi-Paxos. Реализации (etcd, ZooKeeper, Consul) и их применение.
* Распределённые транзакции: 2PC, 3PC, Saga (orchestration vs choreography), TCC, Outbox pattern на практике.
* Event Sourcing и CQRS в проде: snapshotting, projections, eventual consistency читающей стороны, проблема re-build.
* Kafka в глубину: партиционирование, exactly-once семантика, transactional outbox, Kafka Streams.
* Stream processing: Apache Flink, ksqlDB, обработка late events, watermarks, окна.
* Distributed tracing на серьёзном уровне: W3C Trace Context, baggage, sampling strategies, корреляция через границы сервисов.
* Service mesh: Istio, Linkerd. Когда нужен и когда это overengineering.
* Multi-region архитектуры: репликация данных, conflict-free replicated data types (CRDT), геораспределённые БД (CockroachDB, YugabyteDB, Spanner).
* Chaos engineering: Chaos Monkey, Litmus, искусственные сбои в стейджинге и проде.

Ресурсы:

* «Designing Data-Intensive Applications» (перечитать с другим уровнем понимания).
* «Database Internals» Alex Petrov.
* Курс MIT 6.824 Distributed Systems на YouTube.
* Статьи Martin Kleppmann в его блоге, особенно про CRDT.
* Jepsen-отчёты о реальных багах в распределённых БД.

---

## Этап 12. Платформенная инженерия

Если вы строите внутренние платформы для других команд, занимаетесь developer experience, инфраструктурой для микросервисов.

* Service templates: golden paths, скаффолдинг новых сервисов через Backstage, cookiecutter, dotnet new templates.
* Internal Developer Platform: Backstage, Port, Humanitec. Каталог сервисов, ownership, scorecards.
* Service mesh, API Gateway (Kong, Envoy, YARP), policy as code (OPA).
* GitOps: ArgoCD, Flux. Декларативное описание состояния кластера.
* Kubernetes operators на C# через KubeOps. Кастомные CRD под нужды компании.
* Multi-tenancy: изоляция данных, ресурсов, secrets, биллинга на уровне платформы.
* SRE-практики: SLI, SLO, error budgets, toil reduction, постмортемы без поиска виноватых.
* FinOps: атрибуция облачных расходов на команды, контроль cost drift, reserved instances, spot.

Ресурсы:

* «Team Topologies» Skelton, Pais.
* «Site Reliability Engineering» книги Google (бесплатно онлайн).
* «Platform Engineering on Kubernetes» Mauricio Salatino.
* Блог Charity Majors про observability.

---

## Этап 13. Доменно-управляемое проектирование на практике

DDD на уровне выше книжного. Когда вы реально проектируете сложные домены, а не просто называете папки Aggregate.

* Strategic DDD: context mapping, anti-corruption layer, partnership, customer/supplier, shared kernel, conformist.
* Event Storming как метод изучения домена. Big Picture, Process Modeling, Software Design сессии.
* Bounded contexts и команды по Conway's law. Размер контекста под размер команды.
* Tactical DDD: агрегаты с инвариантами, value objects вместо примитивов, доменные события как контракт между контекстами.
* Specification pattern, doman services, factories. Когда они уместны, когда вырождаются в anemic model.
* CQRS как естественное следствие DDD, а не отдельный паттерн навешанный сверху.
* Modular monolith как переходная стадия и постоянная архитектура для большинства продуктов.
* Микросервисы по границам bounded contexts, а не по техническим слоям.

Ресурсы:

* «Learning Domain-Driven Design» Vlad Khononov, современная замена книге Эванса.
* «Implementing Domain-Driven Design» Vaughn Vernon.
* «Domain Modeling Made Functional» Scott Wlaschin (на F#, но идеи переносятся на C#).
* Канал Eric Evans на YouTube, доклады с DDD Europe.

---

## Этап 14. Расширение стека за пределы C#

Senior+ инженер не сидит в одном языке. Расширение стека делает вас сильнее в основном языке и открывает двери.

* F# для функционального программирования, моделирования доменов, скриптов, data science. Учит мыслить через типы и неизменяемость.
* Rust для системного программирования, FFI с .NET через C ABI, написания горячих участков как native библиотек.
* Go для CLI-инструментов, инфраструктурных утилит, операторов Kubernetes.
* TypeScript на уровне комфортной работы. Фронтенд закрыт, full-stack тикеты не пугают.
* Python для скриптов, ML, интеграций. Минимум pandas, numpy, requests.
* SQL расширенный: window functions, CTE, recursive queries, query optimization на уровне понимания execution plans.
* Lua, Wasm, Elixir для отдельных задач (скриптинг, edge computing, fault-tolerant системы).

Не нужно знать всё. Нужен второй язык на хорошем уровне и три-четыре на читающем.

Ресурсы:

* «Programming Rust» Blandy, Orendorff.
* «Domain Modeling Made Functional» (F#).
* «The Go Programming Language» Donovan, Kernighan.
* exercism.io для практики синтаксиса в новых языках.

---

## Этап 15. ML и AI-инженерия в .NET-стеке

Если хотите быть тем разработчиком, который встраивает ИИ в продукт, а не просто пользуется ChatGPT.

* ML.NET для классических задач: классификация, регрессия, кластеризация, рекомендации, anomaly detection. AutoML.
* ONNX Runtime для запуска моделей, обученных в PyTorch или TensorFlow, прямо из C#. Inference на CPU и GPU.
* Semantic Kernel и Microsoft.Extensions.AI для построения LLM-приложений на .NET: оркестрация промптов, function calling, агенты.
* RAG-архитектуры: эмбеддинги, векторные БД (Qdrant, Weaviate, pgvector, Azure AI Search), chunking, re-ranking.
* Локальные модели через Ollama, llama.cpp, интеграция через REST или gRPC.
* Fine-tuning, prompt engineering, evaluation: BLEU, ROUGE, LLM-as-judge, regression-тесты для промптов.
* MLOps базово: версионирование моделей и данных (DVC, MLflow), мониторинг drift, A/B-тестирование моделей в проде.
* Safety и guardrails: prompt injection защита, output filtering, PII detection, токен-лимиты, кост-контроль.

Ресурсы:

* Документация ML.NET и Semantic Kernel.
* «Building LLMs for Production» книги от LlamaIndex.
* Курс «AI Engineering» Chip Huyen.
* Блог Simon Willison про практическое применение LLM.

Практика: построить RAG-систему по корпоративной документации на .NET с локальной моделью через Ollama и pgvector. Замерить latency, точность, стоимость.

---

## Этап 16. Open source и техническое лидерство

Уровень, на котором ваше имя начинают узнавать за пределами компании.

* Контрибьют в крупные .NET-репозитории: dotnet/runtime, dotnet/aspnetcore, dotnet/efcore. Начинать с good-first-issue, переходить к фичам.
* Поддержка собственной open source библиотеки. Это другая работа: документация, релизы, обработка issues и PR, общение с пользователями.
* NuGet-пакеты с правильной семантикой версий, source link, deterministic builds, подписанные сборки.
* Выступления на конференциях: DotNext, NDC, .NET Conf, локальные митапы. Путь от 15-минутного lightning talk до часового keynote.
* Технические статьи и блог. Регулярность важнее идеального текста. Кросс-постинг на Habr, Medium, dev.to.
* Менторство и преподавание. Курсы, школы, корпоративные тренинги.
* Tech radar внутри компании: формализованный процесс выбора и отказа от технологий.
* Архитектурный комитет и принятие решений уровня компании, а не команды.

Ресурсы:

* «The Manager's Path» Camille Fournier, даже если не идёте в менеджмент.
* «An Elegant Puzzle» Will Larson.
* Подкасты .NET Rocks, RunAs Radio.
* Изучение работы крупных open source мейнтейнеров (David Fowler, Stephen Toub, Andrew Lock).

---

## Этап 17. Бизнес-контекст и продуктовое мышление

Senior+ инженер понимает, зачем компания платит ему зарплату, и принимает решения, исходя из этого.

* Unit-экономика продукта: CAC, LTV, churn, ARR, gross margin. Уметь прочитать дашборд бизнеса и понять, что важно сейчас.
* Связка технических решений с метриками: как изменение архитектуры влияет на скорость доставки фич, на cost per request, на retention.
* Discovery vs delivery. Когда писать прототип за день, а когда вкладываться в production-grade решение.
* Working backwards от пользователя. Amazon-овский PR/FAQ как формат проектирования продукта до написания кода.
* Понимание базовой финансовой отчётности компании, особенно в публичных компаниях. P&L, cash flow, balance sheet на минимальном уровне.
* Юридические основы: лицензии open source (MIT, Apache, GPL и их совместимость), GDPR, обработка персональных данных, экспортный контроль.
* Переговоры: с командой, с менеджментом, с заказчиками. «Never Split the Difference» Криса Восса как минимальная база.

Ресурсы:

* «Inspired» Marty Cagan про продуктовое мышление.
* «The Lean Startup» Eric Ries.
* «Accelerate» Forsgren, Humble, Kim про DORA-метрики и связь инженерных практик с бизнес-результатами.
* «Working Backwards» Bryar, Carr про процессы Amazon.



---

## Этап 18. DevSecOps и Supply Chain Security

С учётом инцидентов уровня SolarWinds, log4shell и xz-backdoor (2024), безопасность цепочки поставок — обязательная компетенция Senior+.

- SBOM (Software Bill of Materials) через CycloneDX или SPDX. Генерация на CI, хранение в артефактах релиза.
- Подпись артефактов: Sigstore/cosign для контейнеров, NuGet package signing для пакетов.
- Reproducible builds, deterministic compilation (`<Deterministic>true</Deterministic>`, ContinuousIntegrationBuild).
- Сканирование зависимостей: `dotnet list package --vulnerable --include-transitive`, Dependabot, Renovate, OWASP Dependency-Check, Trivy для образов.
- Static Application Security Testing: GitHub CodeQL, Semgrep, SonarQube с security-профилем.
- Dynamic Application Security Testing: OWASP ZAP, Burp Suite в CI как gate перед релизом.
- Secrets scanning: gitleaks, trufflehog, GitHub secret scanning. Pre-commit хуки обязательны.
- Container hardening: distroless или chiseled .NET images, non-root user, read-only filesystem, минимальные capabilities.
- Runtime защита: Falco, eBPF-сенсоры, поведенческие политики в Kubernetes (Kyverno, OPA Gatekeeper).
- Zero Trust в сервисной сети: mTLS через service mesh, SPIFFE/SPIRE для идентичности нагрузок.
- Incident response плейбуки: что делать при утечке секрета, при компрометации образа, при подозрении на бэкдор в зависимости.

Ресурсы:
- SLSA framework (slsa.dev) как референс уровня зрелости supply chain.
- «Securing DevOps» Julien Vehent.
- Доклады с BlackHat и DEF CON по supply chain атакам последних лет.

## Этап 19. Documentation as Code и инженерное письмо

Senior+ инженер пишет столько же, сколько кодирует. Документация — артефакт уровня кода, со своим CI и review.

- README, ARCHITECTURE.md, CONTRIBUTING.md, CHANGELOG.md, SECURITY.md как обязательный минимум каждого проекта.
- ADR (Architecture Decision Records) в формате Michael Nygard, хранятся рядом с кодом и проходят PR-review.
- C4 model (Simon Brown) для архитектурных диаграмм: System Context, Container, Component, Code.
- Diagrams as Code: PlantUML, Structurizr, Mermaid, D2. Diff читается в PR, версии хранятся в git.
- DocFX или Docusaurus для документации API и Handbook'ов команды.
- XML-doc комментарии с примерами для публичных API. `<inheritdoc/>`, cref-ссылки, `<example>`.
- Runbooks для эксплуатации: пошаговые инструкции на каждый частый инцидент, тестируются game day'ями.
- Onboarding-документация: новый инженер должен запустить проект локально за день, не задавая ни одного вопроса.
- Style guide для письма: лаконичность, активный залог, отсутствие маркетинговых штампов, ссылки вместо пересказа.

Ресурсы:
- «Docs for Developers» Bhatti, Corleissen и др.
- Google Developer Documentation Style Guide.
- Microsoft Writing Style Guide.
- Документация Diátaxis framework (tutorials/how-to/reference/explanation).

## Этап 20. Устойчивая карьера, этика и долгая игра

Технические навыки гаснут без устойчивого режима работы и ясных ценностей.

- Режим сна, движение, регулярные ретриты от экранов. Без этого карьера длиной 20+ лет невозможна.
- Burnout-профилактика: лимит часов в неделю, отпуска без ноутбука, разделение рабочих и личных устройств.
- Финансовая независимость как страховка от вынужденных компромиссов. Без неё легко согласиться на токсичный проект из страха.
- Этика инженера: отказ от участия в манипулятивном UX, dark patterns, проектах массовой слежки, продуктах, вредящих уязвимым группам.
- Право говорить «нет» как профессиональная компетенция, а не дерзость. Обоснованный отказ от плохой задачи ценнее десяти выполненных хороших.
- Постоянное обучение в режиме T-shape: глубина в одной вертикали, широкий горизонт по смежным.
- Сеть контактов как актив. Поддержание связей с бывшими коллегами через годы окупается на каждом переходе.
- Личный бренд без шума. Качественные статьи и доклады раз в квартал работают лучше ежедневного шитпостинга.
- Долгосрочные pet-проекты, которые живут годами и эволюционируют вместе с вашими навыками.
- Регулярная ретроспектива карьеры раз в полгода: что выросло, что протухло, куда идти дальше.

Ресурсы:
- «So Good They Can't Ignore You» Cal Newport.
- «Deep Work» Cal Newport.
- «Atomic Habits» James Clear для системы привычек обучения.
- «The Almanack of Naval Ravikant» как взгляд на долгую игру и leverage.

---

## Антипаттерны обучения, чего избегать

- Tutorial hell: бесконечный просмотр курсов без написания собственного кода. Курс без проекта не считается пройденным.
- Tech radar головокружения: метаться между Blazor, MAUI, Avalonia, Uno каждый месяц вместо доведения одного до прода.
- Stack Overflow Driven Development: копировать без понимания. Гарантированный путь к плато на джуновской зарплате.
- Premature optimization: оптимизировать то, что не измерено. Сначала бенчмарк, потом изменение.
- Resume Driven Development: тащить Kubernetes и микросервисы в проект ради строчки в CV, а не ради задачи.
- Перфекционизм без релиза: pet-проект третий год в ветке refactor/v2 — это не проект, а форма прокрастинации.
- Изоляция от сообщества: учиться только по книгам без обсуждения. Чужой код и review ускоряют рост в разы.
- Игнорирование основ ради хайпа: «зачем мне SQL, есть же Cosmos DB и LLM-агенты». Хайп пройдёт, индексы останутся.

## Awesome-ресурсы и сообщества

- [awesome-dotnet](https://github.com/quozd/awesome-dotnet) — каталог библиотек и инструментов.
- [awesome-dotnet-core](https://github.com/thangchung/awesome-dotnet-core).
- [practical-aspnetcore](https://github.com/dodyg/practical-aspnetcore) — сотни рабочих сниппетов.
- [dotnet/runtime](https://github.com/dotnet/runtime) и [dotnet/aspnetcore](https://github.com/dotnet/aspnetcore) — чтение исходников как практика.
- [System Design Primer](https://github.com/donnemartin/system-design-primer) для подготовки к интервью.
- [The Twelve-Factor App](https://12factor.net/) — must-read для бэкендера.
- r/dotnet, r/csharp на Reddit, .NET Discord, локальные Telegram-чаты по C#.
- Конференции с открытыми записями: .NET Conf, NDC, DotNext, dotnetos.
- Подкасты: .NET Rocks!, The Modern .NET Show, Coding Blocks, Software Engineering Daily.

## FAQ

**С чего начать, если я полный новичок?**
Этап 1 без пропусков. Установите .NET SDK, пройдите официальный туториал на learn.microsoft.com, прочитайте первые главы Skeet'а и сразу пишите код. Не переходите ко второму этапу, пока консольный pet-проект не работает стабильно.

**Сколько часов в день нужно учиться?**
Час осознанной практики каждый день эффективнее восьми часов выходного марафона. Главное — регулярность и проектная работа, а не количество часов.

**Java/Python/Go developer хочет в C#. С какого этапа стартовать?**
Этап 1 быстро (1–2 недели на синтаксис), затем сразу Этап 2 и параллельно Этап 5. Архитектура и базы данных переносимы, нужно лишь освоить идиомы платформы.

**Достаточно ли .NET для трудоустройства в 2026?**
Да, рынок стабильно большой: финтех, e-commerce, корпоративный B2B, геймдев на Unity, медицина. Спрос смещается в Senior+ уровни — учитесь глубже, чем требовало время дешёвых джуниоров.

**Нужны ли сертификаты Microsoft?**
Сертификат сам по себе не открывает двери. Полезен как структура для подготовки и как сигнал в B2B/enterprise среде. Pet-проект и open-source контрибы весят больше.

**Что выбрать: Rider или Visual Studio?**
Rider, если вы платите сами и работаете на Mac/Linux. Visual Studio, если у работодателя есть лицензии и вы на Windows. VS Code + C# Dev Kit — для лёгких задач и совместной работы по SSH/Codespaces.

**Стоит ли учить F#?**
Да, на этапе 14. F# дисциплинирует мышление через типы и неизменяемость, и эти привычки делают ваш C# на порядок чище.

**Как понять, что я готов сменить уровень?**
Когда задачи прошлого уровня перестают казаться вызовом и вы устойчиво решаете задачи следующего уровня без помощи. Чек-листы выше — ориентир, не догма.

## Contributing

PR с уточнениями, обновлениями ссылок, новыми ресурсами и опытом приветствуются. Перед отправкой:

- Один PR — одна логическая правка. Большие переработки сначала обсуждаются в issue.
- Сохраняйте тон: трезвый, прикладной, без маркетинга и без академической воды.
- Ресурсы добавляем только те, которые сами читали и можете обосновать пользу.
- Не ломайте оглавление и якоря разделов.
- Опечатки и битые ссылки — без issue, сразу PR.

## License

MIT. Используйте, форкайте, адаптируйте под свои команды и студии. Атрибуция приветствуется, но не обязательна.

---

_Этот roadmap — карта местности, а не маршрут. Маршрут вы прокладываете сами, исходя из задач, рынка и того, что вас зажигает. Удачи на пути._
