# lvim

## Terminal

| Command   | Action                               |
| :-------- | :----------------------------------- |
| `:sp +te` | Split the current pane to a terminal |

## Plugins

### which key

| Command    | Action                                       |
| :--------- | :------------------------------------------- |
| `<leader>` | opens a floating panel that shows key combos |

### lightspeed

| Command | Action                                                      |
| :------ | :---------------------------------------------------------- |
| `s`     | start search, then type the character you are searching for |

### Sourround might be useful if remapped to more easier keys

https://github.com/tpope/vim-surround

| Command | Action                             |
| :------ | :--------------------------------- |
| `ysiw"` | Sourround word with ""             |
| `ds"`   | Remove sourrunding ""              |
| `cs'"`  | Change sourrunding from '' to ""   |
| `vS"`   | sourround visual selection with "" |

Works also with HTML tags `t` or back ticks

## Misc Keys

| Command      | Action                                  |
| :----------- | :-------------------------------------- | --- |
| `<leader>bf` | Search in opened buffers                |     |
| `<leader>bb` | Previous buffer                         |     |
| `<leader>bn` | Next buffer                             |     |
| `CTRL+\`     | Open overlay terminal                   |     |
| `<leader>st` | Search in file                          |     |
| `<leader>f`  | Open file                               |     |
| `gd`         | Go to definition                        |     |
| `<leader>lq` | Open LSP issues (eg. Typescript errors) |     |
| `<leader>Lc` | Open lunarvim config                    |     |
