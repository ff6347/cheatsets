# apt-get

## Upgrade ##


| Command                                 | Result                   |
| :--                                     | :--                      |
| `apt-get install --only-upgrade nodejs` | Upgrade specific package |
| `apt-get -u upgrade --assume-no`        | Check upgradable package |
|                                         |                          |


# dpkg

| Command                  | Result                     |
| :--                      | :--                        |
| dpkg --listfiles pkgname | list all files and folders |
|                          | belonging to that package  |
| dpkg --status pkgname    | list mta infos on that pkg |
|                          |                            |