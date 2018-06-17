# 14 caching

## общее

В данном задании необходимо будет реализовать несколько задач,
в которых нужно будет использовать кэширование данных
(иногда несколько искусственно).

В каждом из заданий необходимо будет реализовать 2 варианта:
*   Внутрипроцессный кэш.
    Например, на базе `System.Runtime.Caching` или `System.Web.Caching`.
*   Внепроцессный / распределённый.
    Например, можно взять
    [Redis on Windows](https://github.com/MSOpenTech/Redis)
    и клиент на базе
    [StackExchange.Redis](https://github.com/StackExchange/StackExchange.Redis).

## 02 кэширование данных из базы

Доработайте приведенный пример (см. _CachingSolutionsSamples_)
по кэшированию данных из базы:
*   Добавьте кэширование ещё 2-3 сущностей (на ваш выбор).
*   Добавьте политики _invalidation cache_:
    по времени и с использованием мониторов SQL
    (в зависимости от того, какие варианты поддерживает конкретная библиотека).

**Примечание!!! Чтобы избежать проблем при сериализации данных
(при работе с внешним кэшем),
обязательно отключайте _LazyLoading_ и генерацию _proxy_
при выборке через _Entity Framework_.**
