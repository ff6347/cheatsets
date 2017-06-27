| Command                               | Result                        |
| :--                                   | :--                           |
| tmux new -s SESSIONNAME               | creates a new session         |
| ^ - b                                 | command prefix                |
| ^ - b "                               | split pane horizontally       |
| ^ - b %                               | split pane vertically         |
| ^ - b ARROW KEY                       | move between panes            |
| ^ - d or exit                         | close a pane                  |
| ^ - b c                               | new window in session         |
| ^ - b p                               | next window                   |
| ^ - b n                               | previous window               |
| ^ - b NUMBER                          | select window by number       |
| ^ - b d                               | detach from session           |
| ^ - b D                               | select session to detach from |
| tmux ls                               | list session                  |
| tmux attach -t NUMBER                 | attach to session with number |
| tmux rename-session -t NUMBER newname | rename a session              |
| ^ - b ?                               | tmux help                     |
| ^ - b [                               | enter copy mode               |
| ---                                   | scolling around and working   |
| ---                                   | with stdout                   |


Some guides:  

- [A quick and easy guide by hamvocke.com][hamvocke]
- [tmux cheatsheet][gist1]


[hamvocke]: http://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/
[gist1]: https://gist.github.com/MohamedAlaa/2961058