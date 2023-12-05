# 聊天过滤

聊天过滤会替换玩家聊天信息中被检测到的特定词汇

使用 ```general.management.bypassChatFilter``` 权限以绕过此过滤

## Configurations
```yaml
chat-filter:
  enabled: false
  
  replacement-text: "*"
  including-messaging-commands:
    vanilla: true

  use-banned-words: true
  banned-words:
    - "f*ck"

  use-regex: false
  regex:
    - ""
```

- **replacement-text** 用于替换检测到词汇的字符
- **including-messaging-commands** 检测消息命令
    - **vanilla** ```/msg, /tell, /me, /say```
- **use-banned-words** 使用 ```banned-words``` 中的词汇
- **use-regex** 使用 ```regex``` 中的正则
