# 举报

反作弊支持通过举报计数来管理 [信誉因素](TrustFactor.md)

## 配置
**anticheat/config.yml**
```yaml
reporting:
  use-external: true
  external-reporting-commands:
    - report
```

- **use-external** 使用外部命令计数
- **external-reporting-commands** 用于计数的外部举报命令, 支持  ```/<command> <player> <reason>``` 格式
