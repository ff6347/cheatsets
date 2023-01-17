# Vim / Neovim

## General

| Command               | Action                                                                            |
| :-------------------- | :-------------------------------------------------------------------------------- |
| `:h<topic>`           | opens the help                                                                    |
| `:stop` or `:suspend` | suspend Vim while in the middle of editing, return to the suspended Vim, run `fg` |

## Clipboard

| Command | Action                      |
| :------ | :-------------------------- |
| `"*p`   | Paste from system clipboard |
| `"*y`   | Yank to system clipboard    |

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

## Visual Mode

| Command           | Action             |
| :---------------- | :----------------- |
| `v` plus movement | Select visually    |
| `V`               | linewise selection |

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
| `CTRL + u` | Move up half screen                                |
| `CTRL + d` | Move down half screen                              |
| `CTRL + f` | Move forward one screen                            |
| `CTRL + b` | Move back one screen                               |

## Exit Vim

It is already a meme how to exit vim

| Command      | Action                   |
| :----------- | :----------------------- |
| `:q`         | Exit                     |
| `:wq`        | Save and Exit            |
| `SHIFT + ZZ` | Save and Exit            |
| `:qa`        | Quita all without saving |
| `SHIFT + ZQ` | Exit without saving      |

## Focus Line

| Command     | Action                                                           |
| :---------- | :--------------------------------------------------------------- |
| `zz`        | center screen on current line                                    |
| `zt`        | bring current line to top                                        |
| `zb`        | bring current line to bottom                                     |
| `z.`        | center line and set cursor to beginning                          |
| `z + ENTER` | bring line to top and set cursor to the beginning                |
| `z-`        | bring current line to the bottom and set cursor to the beginning |
|             |                                                                  |

## Character Manipulation

### Change Case

| Command | Action                                             |
| :------ | :------------------------------------------------- |
| `~`     | Change case unser cursor                           |
| `guw`   | Change to end of current WORD from upper to lower. |
| `guaw`  | Change all of current WORD to lower.               |
| `gUw`   | Change to end of current WORD from lower to upper. |
| `gUaw`  | Change all of current WORD to upper.               |
| `g~~`   | Invert case to entire line                         |
| `g~w`   | Invert case to current WORD                        |
| `guG`   | Change to lowercase until the end of document.     |
| `gU)`   | Change until end of sentence to upper case         |
| `gu}`   | Change to end of paragraph to lower case           |
| `gU5j`  | Change 5 lines below to upper case                 |
| `gu3k`  | Change 3 lines above to lower case                 |

### Souround with (no plugin)

| Command        | Action                                                                             |
| :------------- | :--------------------------------------------------------------------------------- |
| `ciw '' Esc P` | Sourround with single quotes by cutting the word, adding quotes and pasting inside |

## Vim Grammar

Text objects are used with operators. There are two types of text objects: inner and outer text objects.

```plain
i + object    Inner text object
a + object    Outer text object
```

| Command                | Action                                                                      |
| :--------------------- | :-------------------------------------------------------------------------- |
| inner and outer objets |                                                                             |
| `di(`                  | delete all content within (). Deletes from ("Hello world") <- "Hello world" |
| `da(`                  | delete all content with (). Deltes from ("Hello world") <- ("Hello world")  |
| `daw`                  | delete the word under the cursor                                            |

Below is a list of common objects

```plain
w         A word
p         A paragraph
s         A sentence
( or )    A pair of ( )
{ or }    A pair of { }
[ or ]    A pair of [ ]
< or >    A pair of < >
t         XML tags e.g. HTML
"         A pair of " "
'         A Pair of ' '
`         A pair of ` `
```

| Command | Action                                               |
| :------ | :--------------------------------------------------- |
| `c`     | Delete text, save to register, and start insert mode |

| Command            | Action                                                                                                                                                                                                                                                  |
| :----------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `r`                | (replace) never enters insert mode at all. Instead, it expects another character, which it will then use to replace the character currently under the cursor.                                                                                           |
| `c`                | (change) takes a vi/vim motion (such as w, j, b, etc.). It deletes the characters from the current cursor position up to the end of the movement. Note that this means that s is equivalent to cl (vim documentation itself claims these are synonyms). |
| `cwsomething<ESC>` | Change the word under the cursor to `something` and leave insert mode                                                                                                                                                                                   |

## Settings

| Command             | Action                      |
| ------------------- | --------------------------- |
| `:set filetype=xml` | Set the syntax highlighting |
| `:set wrap`         | Set word wrap               |
| `:set nowrap`       | Unset word wrap             |
| `:set wrap!`        | toggle word wrap            |

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

## Replace all of current word under cursor

| Command                       | Action                                                                             |
| :---------------------------- | :--------------------------------------------------------------------------------- |
| `*` and then `:%s//new name/` | If you don't specify a pattern, the substitute command uses the last searched one. |

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

## Frameworks

There is LunarVim for Neovim which seems to be marvelous
[lunarvim](lunarvim.md)

## Plugins

### fzf vim plugin

| Command | Action               |
| :------ | :------------------- |
| `Files` | Find files usinf fzf |

### EasyMotion

https://github.com/easymotion/vim-easymotion

| Command              | Action                                               |
| :------------------- | :--------------------------------------------------- |
| `<leader><leader>w`  | Enable easy motion to all words                      |
| `<leader><leader>ft` | Enable easy motion to all occurrences of character t |

### Prettier

https://github.com/prettier/vim-prettier

| Command     | Action |
| :---------- | :----- |
| `<leader>p` | Format |

### tComment

| Command     | Action                                 |
| :---------- | :------------------------------------- |
| `<leader>/` | Comment uncomment with tComment plugin |

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

---

[vinegar.vim source]: https://github.com/tpope/vim-vinegar
