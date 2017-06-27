## Mail Report ##

| Command                | Result                | Comment                   |
| :-                     | :--                   | :--                       |
| `MAILTO="bah@foo.com"` | send mail with stdout | is valid for all ff lines |



    # *   *   *   *   *        command to be executed
    # -   -   -   -   -
    # |   |   |   |   |
    # |   |   |   |   +----- day of week (0 - 6) (Sunday=0)
    # |   |   |   +------- month (1 - 12)
    # |   |   +--------- day of month (1 - 31)
    # |   +----------- hour (0 - 23)
    # +------------- min (0 - 59)