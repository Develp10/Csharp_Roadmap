# Этап 8. Облака и эксплуатация (1–2 месяца)

В 2026 году писать backend без понимания облаков и эксплуатации это писать половину работы. Разница между Middle и Senior часто именно тут: умеешь не только реализовать фичу, но и понимаешь, что произойдёт с ней в проде, под нагрузкой, при отказе зоны доступности.

## Облачные платформы

* Azure для .NET-стека ближе по интеграциям (App Service, Functions, Service Bus, Cosmos DB, Application Insights). Сертификация AZ-204 даёт системный взгляд.
* AWS даёт больше работы на глобальном рынке. Минимум: EC2, ECS/EKS, RDS, S3, SQS, SNS, Lambda, IAM. Сертификация Developer Associate.
* GCP реже в .NET-вакансиях, но встречается в data-командах.
* Облако не панацея: вендор-лок, неожиданные счета, эффект холодного старта в serverless. Понимать, когда дешевле и проще выбрать managed-сервис, а когда self-hosted.

## Контейнеры и оркестрация

* Docker: multi-stage builds, минимальные базовые образы (chiseled containers для .NET 8+, distroless), безопасность образов (Trivy, Grype).
* Kubernetes основы: Pod, Deployment, Service, Ingress, ConfigMap, Secret, HorizontalPodAutoscaler.
* Helm и Kustomize для управления манифестами. Argo CD либо Flux для GitOps.
* Service mesh (Istio, Linkerd) обзорно, чтобы понимать, какую проблему решает.
* Альтернативы Kubernetes для небольших проектов: Azure Container Apps, AWS ECS Fargate, Google Cloud Run. Часто проще и дешевле.

## Infrastructure as Code

* Terraform как индустриальный стандарт, OpenTofu как форк после смены лицензии.
* Bicep в Azure-стеке как более удобная альтернатива ARM-шаблонам.
* Pulumi для тех, кто хочет описывать инфраструктуру на C#.
* Принцип immutable infrastructure: окружение пересоздаётся, а не правится руками.
* State management: remote state, locking, разделение по окружениям и сервисам.

## Наблюдаемость в проде

* Метрики через Prometheus и Grafana либо облачные аналоги (Application Insights, CloudWatch, Google Cloud Monitoring).
* Трейсинг через OpenTelemetry, экспорт в Jaeger, Tempo, Honeycomb, Datadog.
* Логи: структурированные, с корреляцией по TraceId. Loki, ELK, либо облачные сервисы.
* SLI, SLO, error budget как способ договариваться с продактами о качестве. «Site Reliability Engineering» книга от Google как основа.
* Alerting на основе симптомов (пользователь страдает), а не причин (CPU 80%). Избегайте alert fatigue.

## CI/CD

* GitHub Actions, GitLab CI, Azure DevOps Pipelines. Принципы одинаковые, синтаксис разный.
* Trunk-based development против Git Flow. Для большинства команд trunk-based с feature flags проще и быстрее.
* Deployment стратегии: blue-green, canary, rolling. Когда какую использовать.
* Feature flags через LaunchDarkly, Unleash, Flagsmith либо собственное решение. Отделяют деплой от релиза.
* Secrets management: GitHub Secrets, Azure Key Vault, HashiCorp Vault, AWS Secrets Manager. Никогда не коммитим секреты, даже в приватный репозиторий.

## Безопасность в эксплуатации

* OWASP Top 10 и OWASP API Top 10 как чек-лист.
* Защита от типовых атак: SQL injection (параметризованные запросы), SSRF, XXE, deserialization, IDOR.
* Управление зависимостями: Dependabot, Renovate, Snyk. SBOM (CycloneDX, SPDX) для прозрачности supply chain.
* Принцип наименьших привилегий: IAM-роли, managed identities, RBAC в Kubernetes.
* Сетевая безопасность: private endpoints, VPC peering, WAF.

## Ресурсы

* «Site Reliability Engineering» и «The Site Reliability Workbook», Google, бесплатно онлайн.
* «Designing Distributed Systems», Brendan Burns.
* «Kubernetes Up and Running», Brendan Burns и соавторы.
* «Terraform: Up and Running», Yevgeniy Brikman.
* Канал TechWorld with Nana на YouTube для практических введений в DevOps.
* Документация облачных провайдеров и CNCF (cncf.io).

## Практика

1. Задеплоить полноценный .NET-сервис в Kubernetes (managed: AKS, EKS, GKE) с Helm-чартами, Ingress, секретами из Vault, метриками в Prometheus.
2. Написать Terraform-модуль на типовой стек (БД, очередь, сервис, балансировщик) с разделением dev/staging/prod.
3. Настроить полноценный CI/CD пайплайн: тесты, security scan, build image, deploy в staging, ручное подтверждение для prod.
4. Сформулировать SLI и SLO для своего сервиса, настроить alerting на их нарушение.

## Сигналы готовности к следующему этапу

* Поднимали и эксплуатировали Kubernetes-кластер, не просто запускали helm install.
* Можете объяснить, почему alert на CPU не нужен, а на latency P99 нужен.
* Писали Terraform-код, который пересоздаёт окружение с нуля без ручных действий.
* Расследовали production incident по трейсам и метрикам, написали постмортем без обвинений.

## Назад к навигации

[К списку этапов](README.md) · [К основному README](../README.md)
