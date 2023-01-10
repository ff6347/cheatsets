## Notation
```plain
    # *   *   *   *   *        command to be executed
    # -   -   -   -   -
    # |   |   |   |   |
    # |   |   |   |   +----- day of week (0 - 6) (Sunday=0)
    # |   |   |   +------- month (1 - 12)
    # |   |   +--------- day of month (1 - 31)
    # |   +----------- hour (0 - 23)
    # +------------- min (0 - 59)
```
## cronic

The cure for cron mailing you everything

https://habilis.net/cronic/

Usae it like this

```cron
* * * * * cronic script
```

## chronic

Alterantive to cronic is chronic which allows to silence the mails even if there is output to stderr. You can define that it only sends with a non zero exit code

```cron
* * * * * chronic script
```


## Mail Report

| Command                | Result                | Comment                   |
| :-                     | :--                   | :--                       |
| `MAILTO="bah@foo.com"` | send mail with stdout | is valid for all ff lines |
