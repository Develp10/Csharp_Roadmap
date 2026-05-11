# Этап 5. ASP.NET Core и веб-разработка (2–3 месяца)

ASP.NET Core это рабочая лошадка большинства .NET-команд. На этом этапе цель не просто поднять Hello World, а понимать, что происходит в pipeline, как устроена аутентификация в реальных продуктах и как отдать сервис в эксплуатацию без сюрпризов.

## Что освоить

* Kestrel как HTTP-сервер, reverse proxy (Nginx, YARP), HTTP/2 и HTTP/3, gRPC-транспорт.
* Middleware pipeline: порядок имеет значение, понимание Use, Run, Map, кастомные middleware для логирования, корреляции, обработки ошибок.
* DI-контейнер: lifetimes (Singleton, Scoped, Transient), captive dependency, регистрация по интерфейсам, decorator pattern через Scrutor.
* Конфигурация: appsettings, переменные окружения, секрет-сторы (Azure Key Vault, AWS Secrets Manager, HashiCorp Vault). Options pattern, IOptionsMonitor для горячей перезагрузки.
* Minimal APIs против контроллеров. Minimal APIs выигрывают по производительности и читаемости в небольших сервисах, контроллеры удобнее в крупных API с фильтрами и сложной маршрутизацией.
* Model binding, валидация (FluentValidation либо DataAnnotations), маппинг (Mapster, ручной маппинг). AutoMapper в новых проектах берут реже из-за лицензионных изменений и скрытой магии.

## Аутентификация и авторизация

* JWT-токены: устройство, подпись, валидация, refresh-токены, безопасное хранение на клиенте.
* OAuth 2.0 и OpenID Connect: грantы, flows, scopes. Identity-провайдеры: Auth0, Keycloak, IdentityServer (Duende), Azure AD B2C.
* ASP.NET Core Identity для собственной системы пользователей, когда внешний провайдер избыточен.
* Policy-based авторизация против role-based, claims, requirement handlers.
* Защита от типовых атак: CSRF, XSS, открытые редиректы, IDOR. ASP.NET Core даёт встроенные механизмы, важно понимать, когда они работают, а когда нет.

## Наблюдаемость и эксплуатация

* Структурированное логирование через ILogger и Serilog, корреляция запросов через TraceId.
* OpenTelemetry: трейсинг, метрики, экспорт в Jaeger, Tempo, Prometheus, Grafana. Это стандарт индустрии, а не опция.
* Health checks (liveness, readiness), graceful shutdown, hostedservices, BackgroundService.
* ProblemDetails для единообразных ошибок API, идемпотентность критичных операций, версионирование API (URL, header, media type).
* Swagger/OpenAPI и генерация клиентов (NSwag, Kiota).

## Дополнительные технологии

* gRPC для внутренней коммуникации между сервисами, контракт-first подход через .proto.
* SignalR для real-time сценариев: чаты, дашборды, уведомления. Понимать ограничения масштабирования и backplane (Redis).
* GraphQL через HotChocolate, когда у клиента сложные требования к выборке данных. Минусы: сложность кэширования и rate limiting.
* Background jobs: Hangfire, Quartz.NET, либо нативные HostedService для простых сценариев.

## Ресурсы

* «ASP.NET Core in Action», Andrew Lock, актуальное издание под последнюю LTS.
* Блог Andrew Lock (andrewlock.net), глубокие разборы внутренностей фреймворка.
* Документация Microsoft по ASP.NET Core, особенно разделы Security и Performance.
* Канал Nick Chapsas на YouTube для практических разборов фич.
* Блог David Fowler в GitHub (davidfowl/AspNetCoreDiagnosticScenarios) обязателен к прочтению.

## Практика

Построить полноценный API сервиса задач:

1. Авторизация через JWT с refresh-токенами и ролями.
2. Persistence через EF Core, миграции, репозитории либо прямой DbContext.
3. Валидация через FluentValidation, маппинг руками.
4. Структурированные логи в Serilog, экспорт трассировок в Jaeger.
5. Health checks, Dockerfile, деплой в облако (Azure App Service, AWS ECS либо Kubernetes).
6. CI/CD через GitHub Actions с прогоном тестов и линтинга.

## Сигналы готовности к следующему этапу

* Понимаете, почему порядок middleware важен, и можете сходу написать собственное.
* Объясните разницу между Scoped и Singleton без подсказок и приведёте пример captive dependency.
* Настраивали OpenTelemetry в проекте, который ушёл в прод.
* Умеете спроектировать API так, чтобы повторный запрос не создавал дубль платежа.

## Назад к навигации

[К списку этапов](README.md) · [К основному README](../README.md)
