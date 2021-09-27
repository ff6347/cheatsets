# Vim

## Movement

| Action                     | Command                  |
| -------------------------- | ------------------------ |
| Move to end of line        | `$`                      |
| Move to start of line      | `^` or `0`               |
| Move to end of line & edit | `A`                      |
| Move to end of file        | `G`                      |
| Move to start of file      | `gg`                     |
| Move one word forward      | `w`                      |
| Move one word backward     | `b`                      |
| Format JSON                | `:%!python -m json.tool` |
| Move one page down         | `^f`                     |
| Move one page up           | `^b`                     |

## Search and Replace

| Action                                          | Command         |
| ----------------------------------------------- | --------------- |
| Change each 'foo' to 'bar' in all the lines.    | `:%s/foo/bar/g` |
| Change each 'foo' to 'bar' in the current line. | `:s/foo/bar/g`  |

## Settings

| Action                      | Command             |
| --------------------------- | ------------------- |
| Set the syntax highlighting | `:set filetype=xml` |
| Set word wrap               | `:set wrap`         |
| Unset word wrap             | `:set nowrap`       |
| toggle word wrap            | `:set wrap!`        |
