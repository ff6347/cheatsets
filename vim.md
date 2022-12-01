# Vim

## General

| Command               | Action                                                                            |
| :-------------------- | :-------------------------------------------------------------------------------- |
| `:h<topic>`           | opens the help                                                                    |
| `:stop` or `:suspend` | suspend Vim while in the middle of editing, return to the suspended Vim, run `fg` |

## Movement

| Command    | Action                                             |
| :--------- | -------------------------------------------------- |
| `$`        | Move to end of line                                |
| `^` or `0` | Move to start of line                              |
| `A`        | Move to end of line & edit                         |
| `G`        | Move to end of file                                |
| `gg`       | Move to start of file                              |
| `w`        | Move one word forward                              |
| `b`        | Move one word backward                             |
| `^f`       | Move one page down                                 |
| `^b`       | Move one page up                                   |
| `42G`      | Goto Line n                                        |
| `k`        | up                                                 |
| `j`        | down                                               |
| `h`        | left                                               |
| `l`        | right                                              |
| `%`        | move to matching bracket if you are on one already |

## Search and Replace

| Command         | Action                                          |
| --------------- | ----------------------------------------------- |
| `:%s/foo/bar/g` | Change each 'foo' to 'bar' in all the lines.    |
| `:s/foo/bar/g`  | Change each 'foo' to 'bar' in the current line. |
| `/`             | search                                          |
| `n`             | move after search forward                       |
| `N`             | move after search backward                      |
| `*`             | search word under the cursor forward            |
| `#`             | search word under the cursor backward           |

## Undo Redo

| Command  | Action |
| :------- | :----- |
| `u`      | undo   |
| `CTRL-r` | redo   |

## Insert Mode

get into insert mode `i`

| Command                   | Action                                                                |
| :------------------------ | :-------------------------------------------------------------------- |
| `i`                       | `i`nsert content before current character                             |
| `a`                       | insert content `a`fter the current character                          |
| `A`                       | insert content `A`fter everything. Move cursor to the end of the line |
| `o`                       | open a new line below the current and start insert                    |
| `O`                       | open a new line above the current and start insert                    |
| `esc`, `CTRL-c`, `CTRL-[` | back to normal mode if in insert mode                                 |

## Buffers, Tabs and Windows

| Command    | Action                               |
| :--------- | :----------------------------------- |
| `Ctrl-W H` | Moves the cursor to the left window  |
| `Ctrl-W J` | Moves the cursor to the window below |
| `Ctrl-W K` | Moves the cursor to the window upper |
| `Ctrl-W L` | Moves the cursor to the right window |

### Windows

| Command            | Action                                                                        |
| :----------------- | :---------------------------------------------------------------------------- |
| `:split file`      | split the current window into half and show another with the `file` as buffer |
| `:vsplit file3.js` | split current window vertically                                               |
| `:new filename`    | Create new window                                                             |
| `Ctrl-W C`         | Close current window. Buffer is still there                                   |
| `Ctrl-W V`         | Opens a new vertical split                                                    |
| `Ctrl-W S`         | Opens a new horizontal split                                                  |
| `Ctrl-W C`         | Closes a window                                                               |
| `Ctrl-W O`         | Makes the current window the only one on screen and closes other windows      |

### Buffers

| Command              | Action                                                                  |
| :------------------- | :---------------------------------------------------------------------- |
| `:buffer <filename>` | Open specific buffer You can have more then one buffer of the same file |

### Tabs

| Command            | Action                     |
| :----------------- | :------------------------- |
| `:tabnew file2.js` | open file in new tab       |
| `:tabnew file.txt` | Open file.txt in a new tab |
| `:tabclose`        | Close the current tab      |
| `:tabnext`         | Go to next tab             |
| `:tabprevious`     | Go to previous tab         |
| `:tablast`         | Go to last tab             |
| `:tabfirst`        | Go to first tab            |
| `gt`               | Move to next tab           |
| `gT`               | Move to previous tab       |

## Settings

| Command             | Action                      |
| ------------------- | --------------------------- |
| `:set filetype=xml` | Set the syntax highlighting |
| `:set wrap`         | Set word wrap               |
| `:set nowrap`       | Unset word wrap             |
| `:set wrap!`        | toggle word wrap            |

## misc

| Command                  | Action      |
| :----------------------- | :---------- |
| `:%!python -m json.tool` | Format JSON |

## Files

| Command          | Action                                                            |
| :--------------- | :---------------------------------------------------------------- |
| `:edit file.txt` | To open a file in Vim, you can use `:edit`.                       |
| `:find`          | Searching Files                                                   |
| `vim .`          | opens the current directory in vims file explorer                 |
| `:edit .`        | opens the current directory in vims file explorer from inside vim |
| `:Explore`       | Starts netrw on current file                                      |
| `:Sexplore`      | No kidding. Starts netrw on split top half of the screen          |
| `:Vexplore`      | Starts netrw on split left half of the screen                     |

### fzf vim plugin

| Command | Action               |
| :------ | :------------------- |
| `Files` | Find files usinf fzf |

### netrw (the default file explroer)

| Command | action                     |
| :------ | :------------------------- |
| `%`     | Create a new file          |
| `d`     | Create a new directory     |
| `R`     | Rename a file or directory |
| `D`     | Delete a file or directory |

[vinegar.vim source] An extension of netrw.

| Command | Action                       |
| :------ | :--------------------------- |
| `-`     | Go one direxctory up         |
| `I`     | Toggle hints on top of newtr |
|         |                              |
|         |                              |

## own keymaps

| Command     | Action                                 |
| :---------- | :------------------------------------- |
| `<leader>/` | Comment uncomment with tComment plugin |

---

[vinegar.vim source]: https://github.com/tpope/vim-vinegar
