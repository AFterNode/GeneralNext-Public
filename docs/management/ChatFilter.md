# ChatFilter

ChatFilter will replace configured words in chat message of players

Use ```general.management.bypassChatFilter``` permission to bypass

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

- **replacement-text** Text to replace detected words
- **including-messaging-commands** Including messaging commands in detections
    - **vanilla** ```/msg, /tell, /me, /say```
- **use-banned-words** Use words in ```banned-words```
- **use-regex** Use regex in ```regex```
