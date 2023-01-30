Load .env files via direnv

```bash
# shellcheck disable=SC2148
export APP_ENV=local
export ML_PGREST_TOKEN=SOMETOKEN

# dotenv
[ -f ".env.${APP_ENV}" ] && dotenv ".env.${APP_ENV}"
dotenv .env.local
```
