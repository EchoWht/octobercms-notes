# 使用 Api-Generator

* 生成一个controller文件（生成目录例如plugins/ahmadfatoni/apigenerator/controllers/api/ostController.php）
* 并且修改路由文件（plugins/ahmadfatoni/apigenerator/routes.php）
* 同步生成一条数据库记录(不是很重要，用途是方便管理)

## 迁移默认生成文件

### 迁移后Controller

将文件移动到自己的模块，修改namespace

### 迁移路由

 在自己的Plugin.php同级目录下新建路由，并复制相应地两行路由代码，修改参数中的namespace
 { 'fillable': 'id,title,url,user_id', 'relation': [{ 'name': 'user', 'fillable': 'id' }
