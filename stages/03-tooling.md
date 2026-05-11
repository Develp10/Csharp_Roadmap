# Этап 3. Инструменты профессионала

**Длительность:** параллельно с Этапами 1–2, продолжается всегда.

**Цель этапа:** освоить инструменты, без которых на сильную команду не возьмут. Это не отдельный курс, это фон, в который вы погружаетесь по мере роста.

## Git

Не просто `add`, `commit`, `push`. Понимать:

- Branching strategies: trunk-based development, GitHub Flow, Git Flow (последний — почти всегда оверкилл).
- `rebase` vs `merge` — когда и зачем.
- Cherry-pick, разрешение конфликтов, `git reflog` для спасения.
- `git bisect` для поиска коммита, в котором сломалось.
- `git log -L`, `git blame -w -C -C -C` для archeology.
- Работа с большими репозиториями: shallow clone, sparse checkout, LFS.

Ресурс: бесплатная [Pro Git book](https://git-scm.com/book/en/v2).

## Командная строка

- Bash или PowerShell на уровне уверенного пользователя.
- Pipes, redirections, `grep`, `sed`, `awk`, `find`, `xargs`.
- Базовая работа с процессами: `ps`, `top`/`htop`, `kill`, `nohup`.
- SSH, scp, rsync, ключи и agent.
- Алиасы, скрипты автоматизации повседневных задач.

## Linux

Даже если работаете на Windows, прод почти всегда Linux.

- Файловая система, права доступа, owners and groups.
- Systemd: создание сервиса, логи через journalctl.
- Логирование: `/var/log/`, ротация через logrotate.
- Сеть: ifconfig/ip, netstat/ss, tcpdump для дебага.
- Пакетные менеджеры: apt, dnf, brew на Mac.

## Docker

- Образы, слои, кеширование, multi-stage builds.
- Dockerfile best practices: минимизация слоёв, безопасность, размер.
- docker-compose для локальной инфры.
- Сетевые режимы: bridge, host, overlay.
- Volumes vs bind mounts.
- Distroless и chiseled .NET images для прода.

Книга: **«Docker Deep Dive»** Nigel Poulton.

## CI/CD

- **GitHub Actions** — стандарт де-факто для open source и многих компаний.
- **Azure DevOps Pipelines** — корпоративная Microsoft-среда.
- **GitLab CI** — если используется GitLab.

Что должен уметь делать ваш pipeline:

- Сборка проекта на каждый push.
- Прогон тестов и публикация результатов.
- Линт markdown, C#, YAML.
- Security scan: dependencies, secrets, containers.
- Сборка и публикация артефактов (NuGet, Docker image).
- Деплой в staging автоматически, в prod — по тегу.

## Отладка и диагностика

- **dotnet-dump** — снятие и анализ дампов памяти.
- **dotnet-counters** — мониторинг счётчиков (GC, ThreadPool, exceptions).
- **dotnet-trace** — сбор трейсов для анализа в PerfView или Speedscope.
- **dotnet-gcdump** — анализ кучи без полного дампа.
- **PerfView** — флагман для анализа производительности на Windows.
- **dotMemory, dotTrace** от JetBrains — UI-альтернативы.

## Бенчмаркинг

**BenchmarkDotNet** — стандарт для микробенчмарков на .NET. Учит дисциплине: не доверять интуиции про производительность.

```csharp
[MemoryDiagnoser]
[SimpleJob(RuntimeMoniker.Net80)]
public class Bench
{
    [Benchmark(Baseline = true)]
    public string Baseline() => "...";

    [Benchmark]
    public string Variant() => "...";
}
```

## Анализ кода

- **EditorConfig** — единый стиль кода в команде.
- **Roslyn analyzers** — статический анализ на этапе сборки.
- **SonarQube, SonarCloud** — корпоративный quality gate.
- **NDepend** — глубокий анализ архитектуры (платный, дорогой, но мощный).

## Менеджмент зависимостей

- Central Package Management через `Directory.Packages.props`.
- `dotnet outdated` для проверки обновлений.
- `dotnet list package --vulnerable` для проверки уязвимостей.
- Dependabot / Renovate для автоматических PR.

## Чек-лист готовности

- [ ] Могу провести интерактивный rebase, чтобы причесать историю коммитов
- [ ] Понимаю разницу между `git merge --no-ff`, `--ff` и `--squash`
- [ ] Использую `git stash` и `git worktree` в повседневной работе
- [ ] Уверенно работаю в терминале без визуальных файловых менеджеров
- [ ] Могу написать рабочий Dockerfile для ASP.NET Core приложения
- [ ] Настроил GitHub Actions для своего pet-проекта
- [ ] Снимал dotnet-dump и анализировал его
- [ ] Делал хотя бы один бенчмарк через BenchmarkDotNet
- [ ] Использую `.editorconfig` во всех своих проектах
- [ ] Понимаю, что такое quality gate и зачем он нужен

## Навигация

[← Этап 2](02-platform.md) | [Все этапы](README.md) | [Главный README](../README.md)
