---
tags:
  - cheatsets
---
This replaces [[direnv]] and [[asdf]]


| Command              | Result                                             |
| :------------------- | :------------------------------------------------- |
| `mise use -g <tool>` | Installs a tool globally                           |
| `mise use <tool>`    | Will install it locally and add a `mise.toml` file |
|                      |                                                    |

Mise can also handle env vars in an `[env]` section and also load them `.env` files

```toml
[env]
_.file = '.env'

```