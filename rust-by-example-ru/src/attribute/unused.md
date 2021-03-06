# `dead_code`

Компилятор предоставляет [*проверку*](https://en.wikipedia.org/wiki/Lint_%28software%29) `dead_code`, которая предупреждает о неиспользованных функциях. Атрибут *dead_code* можно использовать, чтобы отключить данную проверку.

```rust,editable
fn used_function() {}

// `#[allow(dead_code)]` — атрибут, который убирает проверку на неиспользуемый код
#[allow(dead_code)]
fn unused_function() {}

fn noisy_unused_function() {}
// FIXME ^ Добавьте атрибут `dead_code`, чтобы убрать предупреждение

fn main() {
    used_function();
}
```

Обратите внимание, что в реальных программах вы должны удалить неиспользуемый код. В этих примерах мы разрешаем оставить неиспользуемый код в некоторых местах — но это только для примера!
