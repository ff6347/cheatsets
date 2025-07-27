---
tags:
  - cheatsets
---
# z (zoxide)

| Command     | Result                                               |
| :---------- | :--------------------------------------------------- |
|             |                                                      |
| `z foo`     | cd to highest ranked directory matching foo          |
| `z foo bar` | cd to highest ranked directory matching fooo and bar |
| `z foo/`    | can also cd into actual directories                  |
| `zi foo`    | cd with interactive selection using fzf              |
| `zq foo`    | echo the best match, don't cd                        |
| `za /foo`   | add /foo to the database                             |
| `zr /foo`   | remove /foo from the database                        |
