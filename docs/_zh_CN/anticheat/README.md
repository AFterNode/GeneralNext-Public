# 反作弊

实验性功能

## 配置
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

- **trust-factor** 见 [信誉因素](./TrustFactor.md)
- **reporting** 见 [举报](./Reporting.md)
- **operations**
    - **ban-command** 玩家触发max-vl时执行的命令

## 检测配置
**anticheat/checks.yml**

**IllegalMove中的示例**
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

- **use-tf** 使用信誉因素系统
- **tf-offset** 见 [信誉因素](./TrustFactor.md#configurations-for-checks)
- **flag-vl** 触发flag的VL
- **max-vl** 触发 [`operations.ban-command`](#configurations) 的VL
- **ban-durations** 见 [信誉因素](./TrustFactor.md#configurations-for-checks)

## 检测列表

**[子页面](checks/README.md)**
