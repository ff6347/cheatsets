# Shell

| command   | outcome                                        |
| :--       | :--                                            |
| ^ + z     | send current job into backgronud and _suspend_ |
| jobs -l   | list current jobs for current session          |
| bg        | start latest background process in background  |
| fg        | get latest bg process into foreground          |
| disown -h | removes the current job from the session       |
|           | bg, fg, and disown can be used with the job    |
|           | number found in jobs -l.                       |

[Source: Mastering Bash and Terminal blockloop.io](https://www.blockloop.io/mastering-bash-and-terminal)