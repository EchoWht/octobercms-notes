# 项目管理

## 项目安装或迁移

实际开发中我们肯定需要多次迁移项目，因为我们可能在开发中已经修改了October的核心代码，所以不能通过以上的安装方式安装October，我打算还是使用git来迁移项目或者更新项目。以下有两种方式管理October项目，我建议**第一种**

### 方式一：Fork October

1. fork october 的原始仓库(fork后如果想和作者仓库保持同步更新请参考：[fork后保持和原始仓库同步更新](git-notes.md))
    
    > git clone https://github.com/EchoWht/october

1. 创建对应的数据库    
1. 配置 **config/app.php** **config/database.php**(参考[项目迁移时必需要配置的文件](common-config.md))
1. 给予文件夹权限

    > chmod -R 777 october/
    
1. 安装依赖

    > composer install

1. 迁移库表以及初始化数据

    > php artisan october:up


### 方式二：新建一个git仓库，将安装后的源码提交到仓库，通过这个仓库来管理项目。

#### 克隆源码

#### 执行数据库迁移命令（生成全新的数据表以及数据）
        
    php artisan october:up
    
> **注意：** 默认后台管理员用户名（admin）和密码（admin）,如需修改，请修改`october/modules/backend/database/seeds/SeedSetupAdmin.php`文件。

### 方式三：通过安装文件安装

1. 克隆安装文件

    > git clone https://github.com/octobercms/install.git october

1. 给予文件夹权限
    
    > chmod -R 777 october/
    
1. 然后通过浏览器访问

    > http://october.dev/install.php
    
1. 如果服务器参数都没问题，下一步是配置数据库环境，默认是mysql，如果不需要更改则需要填入数据库名(需要提前创建)，以及数据库的用户名和密码
1. 再者是填写后台管理员密码等
1. 配置后台访问的路由url，默认是backend；加密code和文件夹权限
1. 选择安装模式，我选择第一种，第一种不安装任何插件和主题
1. 最后，安全起见删除 *install.php* 文件和 *install_files/* 文件夹，也可以吧 *.git/* 文件夹删掉

## 数据迁移