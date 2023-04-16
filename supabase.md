## Network bans

How to list the banned IPs:

```bash
supabase network-bans get --project-ref <project_reference_id> --experimental
```

How to unban the IPs:

```bash
supabase network-bans remove --db-unban-ip <ip_address> --project-ref <project_reference_id> --experimental

```
