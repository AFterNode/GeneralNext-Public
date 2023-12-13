# TrustFactor

TrustFactor is an expermintal system, TF levels will decrease when user triggered flag-vl for any modules

Default level is ```BLUE```

When AC received report message(s), it will decrease to ```GREEN```

When user reported by more users, it will decrease to ```YELLOW```

If user get banned by AC or reported by more and more users, it will decrease to ```RED```

TF levels never increases automaticially

This system is disabled in default, you can enable it in **anticheat/config.yml**

## Configurations
**anticheat/config.yml**
```yaml
trust-factor:
  enabled: false
  allow-auto-increase: true
```

- **allow-auto-increase** Allow TF levels increase automaticially on user reports successfully 
- **reports.green** Change TF level to ```GREEN``` after reports received
- **reports.yellow** Change TF level to ```YELLOW``` after reports received

## Configurations for checks

TF has different configurations in each AC checks, here is an example in IllegalMovement:

```yaml
IllegalMove:
...
    tf-offset: 
        blue: -5
        green: 0
        yellow: 3
        red: 5
...
    ban-durations:
        blue: 10min
        green: 1h
        yellow: 1d
        red: 7d
```

- **use-tf** Use TF for this check
- **tf-offset** Amount to decrese flag-vl and max-vl
- **ban-durations** Durations for each TF level
