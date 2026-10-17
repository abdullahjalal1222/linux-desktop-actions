# Linux Desktop on GitHub Actions

An always-on XFCE Linux desktop that renews itself, persists everything, and
emails you the credentials on every renewal.

## Architecture

```
Desktop.yml   the session (~4.8h, 100 save cycles, saves every 2.9 min)
Renew.yml     the guarantee  (~5.5h, dispatches the next session)
Watchdog.yml  the safety net (every 30 min, restarts a dead chain)
```

## Secrets

WEBTOP_PASSWORD, RESEND_API_KEY, MAIL_TO, MAIL_FROM

## Stopping

Actions > Desktop > Run workflow > uncheck keep-alive.
