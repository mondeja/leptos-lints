# leptos_print_stdout

### What it does

Check for calls to `leptos::logging::log!`. The purpose of this lint is to catch
debugging remnants. Analog to `clippy::print_stdout` for Leptos.

### Why is this bad?

People often print on stdout while debugging an application and might forget to
remove those prints afterward.

### Known problems

Only catches `leptos::logging::log!` calls.

### Example

```rust
leptos::logging::log!("This is a log message");
```

Use instead:

```rust
#[allow(unknown_lints)]
#[allow(leptos_print_stdout)]
{
    leptos::logging::log!("This is a log message");
}
```
