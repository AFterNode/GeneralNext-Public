# MOTD

## 配置
**customization/config.yml**
```yaml
motd:
  enabled: false
  allow-maintain-mode: false
```

- **motd.allow-maintain-mode** 允许启用维护模式

**customization/motd.yml**
```yaml
defaults:
  a:
    line1: MOTD A LINE1
    line2: MOTD A LINE2
  b:
    line1: MOTD B LINE1
    line2: MOTD B LINE2

maintain:
  join-message: This server is under maintain mode
  motd:
    line1: MAINTAIN MODE
    line2: PLEASE WAIT

```
- **defaults** 标准MOTD
- **xxx.xxx.line1** MOTD第一行
- **xxx.xxx.line2** MOTD第二行
- **maintain.join-message** 维护模式时进入的踢出信息
- **maintain.motd** 维护模式MOTD
