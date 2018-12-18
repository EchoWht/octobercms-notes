# 常用配置

## 项目迁移时必需要配置的文件

### app.php

    'url' => 'http://xxx/'
    'key' => 'Hk8jte9BXWzkRUhYwpbT6ElQHYUXjHF6'
    
### database.php

    'mysql' => [
        'driver'    => 'mysql',
        'host'      => 'localhost',
        'port'      => 3306,
        'database'  => 'octobercms',
        'username'  => 'username',
        'password'  => 'password',
        'charset'   => 'utf8mb4',
        'collation' => 'utf8mb4_unicode_ci',
        'prefix'    => '',
    ],
            