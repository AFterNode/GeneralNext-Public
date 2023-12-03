# Alias Definitions

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

- **xxx.description** Description for the alias, default as ```No description```
- **xxx.usage** Usage for the alias, default as ```/%name%```
- **xxx.aliases** Aliases for the alias
- **xxx.args** Arguments definition, see [Arguments](#arguments)
- **xxx.execution** Alias execution steps, see [Execution](#execution)
- **xxx.permission** Permission for the command, leave blank for none


## Execution
**case-sensitive**
| Type | Description | Example |
| ---  | --- | --- |
| RUN  | Execute a command as current executor | RUN say example

## Arguments
**case-sensitive**
| Type | Description |
| ---  | --- |
| ANY | Redirect argument in current index
| PLAYER | A player name, returns ```messages.unknown-player``` when cannot find this player

# Messages
**customization/alias.yml@messages**
```yaml
missing-args: Missing argument(s)
unknown-player: Unknown player %d
```

- **missing-args** Displayed when missing argument(s)
- **unknown-player** Displayed when cannot find target player in argument type **PLAYER**
