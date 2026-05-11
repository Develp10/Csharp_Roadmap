# Этап 1. Фундамент языка и платформы

**Длительность:** 1–2 месяца интенсивно или 3 месяца параллельно с работой/учёбой.

**Цель этапа:** уверенно писать, читать и отлаживать C# код среднего размера. Понимать модель типов и базовые конструкции, не сверяясь с документацией каждые пять минут.

## Окружение

Установите актуальный .NET SDK (LTS — .NET 8, текущий релиз — .NET 9). IDE на выбор:

- **JetBrains Rider** — лучший баланс для большинства, особенно если работаете на Mac или Linux.
- **Visual Studio 2022** — стандарт в корпоративной Windows-разработке.
- **VS Code + C# Dev Kit** — для лёгких задач и удалённой работы через Codespaces.

Дополнительно:

- Git (Pro Git book как опорное руководство).
- Терминал (Windows Terminal, iTerm2, или встроенный в IDE).
- GitHub аккаунт с настроенным SSH-ключом.

## Что осваиваем

### Синтаксис

- Типы значений и ссылок, nullable reference types, default values.
- Pattern matching: `is`, `switch` statements, switch expressions, property patterns.
- Records, init-only свойства, with-expressions.
- String interpolation, raw string literals, UTF-8 strings.
- Управляющие конструкции, методы, перегрузки, опциональные и именованные аргументы.

### ООП

- Инкапсуляция, наследование, полиморфизм.
- Интерфейсы (включая default interface methods).
- Абстрактные классы, sealed классы, partial.
- Композиция vs наследование — понимание, когда что выбирать.
- Generics, ограничения типов, ковариантность и контравариантность.

### Функциональные элементы

- Делегаты, события, лямбда-выражения.
- Замыкания и их подводные камни (захват переменных).
- LINQ to Objects: `Where`, `Select`, `GroupBy`, `Aggregate`, `Any`, `All`.
- Deferred execution и материализация — почему это важно для производительности.

### Исключения

- Иерархия исключений в .NET.
- when-фильтры в catch-блоках.
- finally, корректное пробрасывание (`throw` vs `throw ex`).
- Когда не нужно ловить исключения.

### Коллекции

- `List<T>`, `Dictionary<TKey, TValue>`, `HashSet<T>`, `Queue<T>`, `Stack<T>`.
- `ImmutableArray`, `ImmutableList`, `ImmutableDictionary`.
- Когда использовать массив, когда список, когда словарь.

## Ресурсы

### Книги

- **Jon Skeet, «C# in Depth»** — обязательный минимум. Особенно главы про generics, делегаты, async.
- **Joseph Albahari, «C# 12 in a Nutshell»** — справочник по всему языку.

### Документация

- [Microsoft Learn по C#](https://learn.microsoft.com/dotnet/csharp/)
- [.NET API Browser](https://learn.microsoft.com/dotnet/api/)
- [C# Language Reference](https://learn.microsoft.com/dotnet/csharp/language-reference/)

### Видео

- Nick Chapsas на YouTube — короткие практические разборы.
- Tim Corey — для начинающих, подача с нуля.
- IAmTimCorey, ZoranHorvat — продвинутый ООП.

### Курсы

- [C# Fundamentals](https://www.pluralsight.com/courses/csharp-fundamentals-dev) Scott Allen на Pluralsight.
- Бесплатные модули [.NET на Microsoft Learn](https://learn.microsoft.com/training/dotnet/).

## Практика

### Минимум

1. Решить 50 задач на [Codewars](https://www.codewars.com/) от 8-кю до 5-кю на C#.
2. Решить 50 задач на [LeetCode](https://leetcode.com/) уровня Easy на C#.

### Pet-проект

Текстовый менеджер задач (CLI) со следующими возможностями:

- Добавление, редактирование, удаление, поиск задач.
- Категории, теги, приоритеты, дедлайны.
- Сохранение в JSON-файл через `System.Text.Json`.
- Команды через аргументы командной строки (`System.CommandLine`).
- Цветной вывод через `Spectre.Console`.
- Юнит-тесты на ключевую бизнес-логику.

**Чек-лист готовности проекта:**

- [ ] README с инструкцией по запуску
- [ ] `.gitignore` для C# проектов
- [ ] Хотя бы 20 коммитов с осмысленными сообщениями
- [ ] Логическое разделение по проектам (Domain, App, CLI, Tests)
- [ ] 30+ пройденных тестов
- [ ] Файл `.editorconfig` для единого стиля

## Чек-лист готовности к Этапу 2

- [ ] Могу написать класс с конструктором, свойствами, методами без подсказок
- [ ] Понимаю разницу между `class` и `struct`, могу объяснить, когда что выбрать
- [ ] Знаю, что такое generic constraint и могу его применить
- [ ] Использую LINQ для типичных задач (фильтрация, группировка, агрегация)
- [ ] Понимаю, что такое замыкание, и вижу ловушки при захвате переменной в цикле
- [ ] Могу написать собственное исключение и правильно его пробросить
- [ ] Использую records для immutable-данных
- [ ] Понимаю pattern matching и применяю switch expressions
- [ ] Не использую `throw ex` (знаю почему)
- [ ] Не путаю value types и reference types в типичных сценариях

## Навигация

⏮ [Все этапы](README.md) | [Главный README](../README.md) | [Этап 2 →](02-platform.md)
