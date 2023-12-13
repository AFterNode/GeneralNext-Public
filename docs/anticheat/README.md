# AntiCheat

Expermintal functions

## Configurations
**anticheat/config.yml**
```yaml
trust-factor:
  enabled: false
  allow-auto-increase: true

  reports:
    green: 1
    yellow: 5
    red: 10

reporting:
  use-external: true
  external-reporting-commands:
    - report

operations:
  ban-command: "/ban %player% %duration% %reason%"
```

- **trust-factor** See [Trust Factor](./TrustFactor.md)
- **reporting** See [Reporting](./Reporting.md)
- **operations**
    - **ban-command** Command to execute when a player triggered max-vl

## Checks Configurations
**anticheat/checks.yml**

**Example in IllegalMove**
```yaml
IllegalMovement:
  enabled: true
  use-tf: true
  tf-offset:
    ...

  ...

  flag-vl: 10
  max-vl: 50

  ban-durations:
    ...
```

- **use-tf** Use TrustFactor system
- **tf-offset** See [Trust Factor](./TrustFactor.md#configurations-for-checks)
- **flag-vl** VL to trigger flags
- **max-vl** VL to execute [`operations.ban-command`](#configurations)
- **ban-durations** See [Trust Factor](./TrustFactor.md#configurations-for-checks)

## Checks

**[Sub Pages](checks/README.md)**
