## Notes

- You dont need () to call a method e.g. `Cards.hello` is the same as `Cards.hello()`
- Elixir has an implicit return on functions. Last statement is the return type

## Command Line

| Command             | Action                                                                   |
| :------------------ | :----------------------------------------------------------------------- |
| `iex -S mix`        | Compiles current module and startrs repl containing it                   |
| `iex(n)> recompile` | if in the repl run recompile to recompile the currently included project |
| `mix new <name>`    | Scafolds a new project with `<name>`                                     |
| `mix deps.get`      | Install dependencies                                                     |
| `mix test`          | Run all tests                                                            |
| `mix test --cover`  | Run all tests with coverage support                                      |
| `mix docs`          | Generate docs from comments                                              |

### Tests

To watch tests install https://github.com/lpil/mix-test.watch

and run `mix test.watch`
