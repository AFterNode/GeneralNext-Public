# 自定义命令

**此页面在docsify可能无法正常展示, 可在 [Github](https://github.com/AFterNode/GeneralNext-Public/blob/master/docs/_zh_CN/customization/Alias.md)查看**

**customization/alias.yml@alias-definitions**
```yaml
example-alias:
    description: Example alias command
    usage: /example-cmd
    permission: ""
    aliases:
        - example-alias-2
    args:
        arg0:
            type: PLAYER
    execution:
        - "RUN minecraft:teleport %arg0%"
```
```Example: teleport to specified player```

- **xxx.description** 此命令的备注，默认为```No description```
- **xxx.usage** 此命令的用法，默认为 ```/%name%```
- **xxx.aliases** 此命令的别名
- **xxx.args** 参数定义, 见 [Arguments](#参数)
- **xxx.execution** 命令执行步骤, 见 [Execution](#执行)
- **xxx.permission** 命令必要的权限，留空则不需要


## 执行
**大小写敏感**
| 类型 | 备注 | 示例 |
| ---  | --- | --- |
| RUN  | 以当前执行者运行指定命令 | RUN say example

## 参数
**大小写敏感**
| 类型 | 备注 |
| ---  | --- |
| ANY | 重定向当前位置的参数
| PLAYER | 玩家名称, 无法找到玩家时回复 ```messages.unknown-player```

# 信息
**customization/alias.yml@messages**
```yaml
missing-args: Missing argument(s)
unknown-player: Unknown player %d
```

- **missing-args** 缺少参数时返回
- **unknown-player** 参数类型为 **PLAYER** 且找不到目标玩家时返回
