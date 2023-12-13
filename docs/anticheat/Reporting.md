# Reporting

AntiCheat service supported use reports counter to manage [TrustFactor](TrustFactor.md) system

## Configurations
**anticheat/config.yml**
```yaml
reporting:
  use-external: true
  external-reporting-commands:
    - report
```

- **use-external** Use external reporting commands for recording
- **external-reporting-commands** External reporting commands for recording reports count, supported ```/<command> <player> <reason>``` format
