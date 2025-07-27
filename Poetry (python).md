---
tags:
  - cheatsets
---
Generate pyrightconfig.json for use in lunarvim

```shell

jq \
	--null-input \
    --arg venv "$(basename $(poetry env info -p))" \
    --arg venvPath "$(dirname $(poetry env info -p))" \
    '{ "venv": $venv, "venvPath": $venvPath }' \
    > pyrightconfig.json
```
