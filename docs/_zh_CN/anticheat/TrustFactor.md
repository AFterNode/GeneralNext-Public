# 信誉因素

信誉因素是一个实验性系统

默认等级为 ```BLUE```

反作弊接收到举报消息时，会降低为 ```GREEN```

被更多玩家举报时，会降低为 ```YELLOW```

被反作弊封禁（触发 max-vl）或被更多用户举报时，会降低为 ```RED```

此系统默认关闭，所有用户等级均为 ```BLUE```，可在 **anticheat/config.yml** 调整

## 配置
**anticheat/config.yml**
```yaml
trust-factor:
  enabled: false

  reports:
    green: 1
    yellow: 5
    red: 10
```

- **reports.green** 接收到此数目的举报后降低为 ```GREEN```
- **reports.yellow** 接收到此数目的举报后降低为 ```YELLOW``

## 对于检测的配置

信誉因素对不同的检测有不同的配置, 以下是在 IllegalMovement 中的示例:

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

- **use-tf** 对此检测弃用信誉因素
- **tf-offset** 降低 max-vl 和 flag-vl 的值
- **ban-durations** 针对特定信誉因素的封禁时间
