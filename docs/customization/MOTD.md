# MOTD

## Configurations
**customization/config.yml**
```yaml
motd:
  enabled: false
  allow-maintain-mode: false
```

- **motd.allow-maintain-mode** Allow to use maintain mode

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
- **defaults** Standard MOTDs
- **xxx.xxx.line1** MOTD Line 1
- **xxx.xxx.line2** MOTD Line 2
- **maintain.join-message** Kick message when joined in maintain mode
- **maintain.motd** Maintain MOTDs
