# 使用插件

## 批量安装插件(包含第三方插件和自己开发的插件)

现在设想的是，写一个中间件通过中间件批量安装，需要实现的功能如下

> 1. 自动从october中下载并安装 *第三方插件* 
> 2. 通过git安装自己开发的插件(git clone后需后可以用builder执行下数据库迁移文件，如果没有显示该插件，检查下这个插件有没有依赖的插件)

## 第三方插件的使用

### 安装方式

1. 安装或卸载通过后台界面操作：**Settings/Update & Plugins**
2. 通过[命令行安装](https://github.com/EchoWht/octobercms-docs-zh/blob/master/console-commands.md#plugin-install-command)(优点：假设我们迁移项目时可以写一个批量安装多个插件的命令)

安装后除了插件自身的数据表，还会在system_plugin_history表中插入这个插件的所有历史更新记录， system_plugin_versions插件的版本信息。管理界面或者命令行移除插件时会自动抹掉所有相关记录

### 修改其他作者的插件

建议不修改，如果需要修改的话可以[fork](git-notes.md)插件的源码进行修改，这样也可以同步作者的更新。
