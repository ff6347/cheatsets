---
tags:
  - cheatsets
---
## Reset Restore

| Command                         | Result                              |
| :------------------------------ | :---------------------------------- |
| git checkout -- filename        | reset file to last commit           |
| git clean -i                    | clean untracked files interactively |
| git reset --hard origin/develop | reset to last state remote          |
| `git restore <FILENAME>`        | Reset file to last commit           |

## diff

| Command                   | Action               |
| :------------------------ | :------------------- |
| ` git diff staging..HEAD` | Compare two branches |

## log

| Command                                                    | Action                                                              |
| :--------------------------------------------------------- | :------------------------------------------------------------------ |
| `git log --pretty=format:"- %s %h" staging...main \| sort` | Logs all commit subjects and hashes between staging and main branch |

https://git-scm.com/docs/pretty-formats

## branches

| Command                                          | Action                                                         |
| :----------------------------------------------- | :------------------------------------------------------------- |
| `git branch --no-merged <YOUR BRANCH NAME HERE>` | Show all branches that where not merged into your selected one |
