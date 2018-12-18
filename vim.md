# Vim

## Movement

| Action                     | Command                  |
|----------------------------|--------------------------|
| Move to end of line        | `$`                      |
| Move to end of line & edit | `A`                      |
| Move to end of file        | `G`                      |
| Format JSON                | `:%!python -m json.too`l |
| Move one page down         | `^f`                     |
| Move one page up           | `^b`                     |

## Search and Replace

| Action                                          | Command         |
|-------------------------------------------------|-----------------|
| Change each 'foo' to 'bar' in all the lines.    | `:%s/foo/bar/g` |
| Change each 'foo' to 'bar' in the current line. | `:s/foo/bar/g`  |

## Settings

| Action                      | Command             |
|-----------------------------|---------------------|
| Set the syntax highlighting | `:set filetype=xml` |
