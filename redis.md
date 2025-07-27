---
tags:
  - cheatsets
---
| Command                 | Action                                       |
| :---------------------- | :------------------------------------------- |
| `INFO`                  | Display server info, memory usage, and stats |
| `DBSIZE`                | Show number of keys in current DB            |
| `MONITOR`               | Stream live Redis commands                   |
| `KEYS *`                | List all keys (avoid in production)          |
| `SCAN 0`                | Safer way to iterate through keys            |
| `TYPE key_name`         | Get type of specified key                    |
| `TTL key_name`          | Show remaining time to live for key          |
| `EXISTS key_name`       | Check if key exists                          |
| `MEMORY USAGE key_name` | Show memory used by key                      |
| `MEMORY STATS`          | Display memory statistics                    |
| `HGETALL hash_key`      | Get all fields in hash                       |
| `SMEMBERS set_key`      | Get all members in set                       |
| `LLEN list_key`         | Get length of list                           |
| `ZRANGE zset_key 0 -1`  | Get all sorted set members                   |
| `SELECT n`              | Switch to database n (0-15)                  |
| `FLUSHDB`               | Clear current database (use with caution)    |
| `INFO memory`           | Show memory-specific statistics              |
