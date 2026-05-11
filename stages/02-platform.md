# Этап 2. Глубже в платформу .NET

**Длительность:** 1–2 месяца после уверенного прохождения Этапа 1.

**Цель этапа:** понимать, как именно ваш код выполняется. Это граница, которая отличает джуна, который «пишет работающий код», от мидла, который «пишет код, который работает под нагрузкой и не разваливается».

## Темы

### CLR и компиляция

- CLR, JIT, AOT, Tiered Compilation, ReadyToRun.
- Что происходит между нажатием F5 и выполнением `Main`.
- Просмотр сгенерированного IL и нативного кода через [SharpLab](https://sharplab.io/).

### Управление памятью

- Стек, куча, поколения GC (Gen 0/1/2, Large Object Heap).
- Server GC vs Workstation GC, когда какой выбирать.
- `Span<T>`, `Memory<T>`, `ref struct`, `stackalloc`.
- Pinning, fixed, GCHandle — когда и зачем.
- ArrayPool, MemoryPool, RecyclableMemoryStream для горячих путей.

### Async/await изнутри

- SynchronizationContext и почему он критичен в UI-приложениях.
- `ConfigureAwait(false)` — когда обязателен, когда не нужен.
- ValueTask vs Task — компромиссы.
- CancellationToken — пробрасывайте всегда.
- Ловушки: sync-over-async, async void, `.Result`, `.Wait()`.

### Параллелизм и конкурентность

- Thread, ThreadPool, Task, Parallel.
- Channels для producer-consumer сценариев.
- Примитивы синхронизации: lock, SemaphoreSlim, Interlocked, ReaderWriterLockSlim.
- Lock-free структуры и Memory Model в .NET.

### Reflection и Source Generators

- Reflection, атрибуты, динамический вызов.
- Стоимость рефлексии в горячих путях.
- Source Generators как современная альтернатива (System.Text.Json, regex, logging).

### IO

- Потоки, BufferedStream, MemoryStream.
- Pipelines (`System.IO.Pipelines`) для высокопроизводительного IO.
- Асинхронные файловые операции и их подводные камни на Windows/Linux.

### Сериализация

- `System.Text.Json` как стандарт по умолчанию.
- Кастомные конвертеры, source-generated сериализация.
- Сравнение с Newtonsoft.Json по производительности и фичам.
- MessagePack, Protobuf-net для бинарных форматов.

## Ресурсы

### Книги

- **Konrad Kokosa, «Pro .NET Memory Management»** — глубокое погружение в GC.
- **Stephen Cleary, «Concurrency in C# Cookbook»** — рецепты для async и параллелизма.

### Блоги

- [Stephen Toub на devblogs.microsoft.com](https://devblogs.microsoft.com/dotnet/author/toub/) — лучший источник по производительности и async.
- [Adam Sitnik](https://adamsitnik.com/) — производительность и Span.
- [Bartosz Adamczewski](https://leveluppp.ghost.io/) — внутренности CLR.

### Видео

- Nick Chapsas, серии по производительности и Span.
- [.NET YouTube channel](https://www.youtube.com/@dotnet) — официальные доклады.
- DotNext, NDC, .NET Conf — записи бесплатно.

## Практика

### Микропроекты

1. **LRU-кеш с потокобезопасным доступом.** Замерить throughput при разных уровнях конкурентности через BenchmarkDotNet.
2. **Простой пул объектов.** Сравнить с `ObjectPool<T>` из Microsoft.Extensions.ObjectPool.
3. **Парсер CSV на Span'ах.** Сравнить с наивной реализацией через `string.Split` по аллокациям.
4. **Producer-consumer через Channel<T>.** Реализовать back-pressure и graceful shutdown через CancellationToken.

### Бенчмарки

Установите [BenchmarkDotNet](https://benchmarkdotnet.org/) и сделайте свой первый бенчмарк. Главное правило: не верьте интуиции про производительность, проверяйте.

```csharp
[MemoryDiagnoser]
public class StringConcatBench
{
    [Params(10, 100, 1000)]
    public int N { get; set; }

    [Benchmark]
    public string PlusOperator()
    {
        var s = "";
        for (var i = 0; i < N; i++) s += i;
        return s;
    }

    [Benchmark]
    public string StringBuilder()
    {
        var sb = new StringBuilder();
        for (var i = 0; i < N; i++) sb.Append(i);
        return sb.ToString();
    }
}
```

## Чек-лист готовности к Этапу 3

- [ ] Могу объяснить разницу между Task и ValueTask
- [ ] Знаю, почему `async void` опасен
- [ ] Понимаю, что делает ConfigureAwait и когда он нужен
- [ ] Могу написать метод, принимающий `ReadOnlySpan<char>` для нулевых аллокаций
- [ ] Понимаю, чем отличаются Gen 0/1/2 в GC
- [ ] Знаю, что такое LOH и почему туда не стоит часто кидать большие массивы
- [ ] Делал хотя бы один бенчмарк через BenchmarkDotNet и анализировал результат
- [ ] Понимаю модель памяти .NET на уровне «memory barriers нужны вот тут»
- [ ] Использую Source Generators хотя бы в одном из своих проектов
- [ ] Читаю Stephen Toub-стайл код и понимаю, зачем там `stackalloc`

## Навигация

[← Этап 1](01-foundation.md) | [Все этапы](README.md) | [Главный README](../README.md) | [Этап 3 →](03-tooling.md)
