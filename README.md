# leptos-lints

[Dylint] lints for apps created with the [Leptos] framework.

[Dylint]: https://github.com/trailofbits/dylint
[Leptos]: https://leptos.dev

## Installation

Install [Dylint] with

```sh
cargo install cargo-dylint dylint-link
```

and then, put the next configuration in the _Cargo.toml_ of your workspace

```toml
[workspace.metadata.dylint]
libraries = [{ git = "https://github.com/mondeja/leptos-lints" }]
```

## Usage

Run the lints with

```sh
cargo dylint --all
```

## Lints

| Rule                    | Description                                 |
| ----------------------- | ------------------------------------------- |
| [`leptos_print_stdout`] | Check for calls to `leptos::logging::log!`. |

[`leptos_print_stdout`]: https://github.com/mondeja/leptos-lints/tree/master/lints/leptos_print_stdout#readme

## Contributing

- Run tests: `cargo test --all`
- Lint and format: `pre-commit run -a` (needs [pre-commit] installed)

[pre-commit]: https://pre-commit.com
