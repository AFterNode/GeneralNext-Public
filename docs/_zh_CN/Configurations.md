# 配置

```yaml
language: en_US

services:
  Management: true

data:
  database:
    type: h2
    host: 127.0.0.1
    port: 3306

    username: ""
    password: ""
    db-name: ""
```

<!-- Misc -->
* **language** 控制台和游戏内语言，请见 [Locale](Locale.md)

<!-- Services -->
* **services** 控制服务开关

<!-- Data -->
* **data**
    * **database**
        * **type** 数据库类型，`h2`支持本地文件，`mysql`支持MySQL数据库
        * **host** 数据库地址, 使用本地数据库时应为 ```127.0.0.1```
        * **port** 数据库端口，通常情况应为```3306```
        * **username** 连接数据库时使用的用户名
        * **password** 连接数据库时使用的密码
        * **db-name** 数据库名称，使用MySQL时必须提前创建对应数据库
