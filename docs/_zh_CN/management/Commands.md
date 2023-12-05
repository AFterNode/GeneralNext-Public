# Commands

需要 ```general.management.command``` 权限

## /management help

展示 ```/management``` 的帮助

## /management query

### 配置
```yaml
query:
  enabled: true
  standalone: false
```

- **standalone** 启用独立命令 (`/query`) 注册

### 用法

需要 ```general.management.command.query``` 权限

**Usage**: ```/management query <player>```

**argument "player"** 查询时使用的玩家名称，支持离线玩家
