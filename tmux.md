# tmux

Original mapping is to ^ + b but I changed that


| Command                               | Result                        |
| :------------------------------------ | :---------------------------- |
| tmux new -s SESSIONNAME               | creates a new session         |
| ^ + SPACE                             | command prefix                |
| ^ + SPACE "                           | split pane **horizontally**   |
| ^ + SPACE %                           | split pane **vertically**     |
| ^ + SPACE ARROW KEY                   | move between panes            |
| ^ - d or exit                         | close a pane                  |
| ^ + SPACE c                           | new window in session         |
| ^ + SPACE p                           | **next** window               |
| ^ + SPACE n                           | **previous** window           |
| ^ + SPACE NUMBER                      | select window by number       |
| ^ + SPACE d                           | detach from session           |
| ^ + SPACE D                           | select session to detach from |
| tmux ls                               | list session                  |
| tmux attach -t NUMBER                 | attach to session with number |
| tmux rename-session -t NUMBER newname | rename a session              |
| ^ + SPACE ?                           | tmux help                     |
|` ^ + SPACE [ `                          | enter copy mode               |
| ---                                   | scolling around and working   |
| ---                                   | with stdout                   |




    CTRL-b-c create new full-sized window (and start a shell)
    CTRL-b-n switch to next full-sized window
    CTRL-b-p switch to previous full-sized window
    CTRL-b-" split current pane horizontally (and start a shell)
    CTRL-b-% split current pane vertically (and start a shell)
    CTRL-b-o switch to next pane
    CTRL-b-UP/DOWN/LEFT/RIGHT switch to pane in that direction
    CTRL-b-x kill current pane (as well as shell running in it)
    CTRL-b-& kill current window (as well as shell running in it)
    CTRL-b-d detach tmux



Some guides:  

- [A quick and easy guide by hamvocke.com][hamvocke]
- [tmux cheatsheet][gist1]


[hamvocke]: http://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/
[gist1]: https://gist.github.com/MohamedAlaa/2961058