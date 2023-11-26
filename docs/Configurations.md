# Configurations

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
* **language** Console&In-Game language, see 

<!-- Services -->
* **services** Configures service enable/disable

<!-- Data -->
* **data**
    * **database**
        * **type** Database type, use h2 to local file, mysql to MySQL Database
        * **host** Database host, should be ```127.0.0.1``` if you are using self-hosted database
        * **port** Database port, normally be ```3306```
        * **username** Database username to login
        * **password** Database password to login
        * **db-name** Database name to use, must be created before if using MySQL database
