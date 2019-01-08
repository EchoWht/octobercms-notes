# 使用 JWTAuth

> 地址 https://octobercms.com/plugin/vdomah-jwtauth

## 使用方法

### 安装

通过命令行或者后台工具安装，安装后记得复制 */plugins/vdomah/jwtauth/config/auth.php* 到 *{root}/config/auth.php*

### 多处使用

例如在自己的路由中使用token验证，例如：

    Route::post('test', function (\Request $request) {
       return response()->json(('The test was successful'));
    })->middleware('\Tymon\JWTAuth\Middleware\GetUserFromToken');
    
假如想修改插件的路由文件 *plugins/vdomah/jwtauth/routes.php*，可以将此文件复制到其他插件（比如自己开发的）的根目录中，例如：

    plugins/blskye/package/routes.php
    
记得在Plugin.php中声明依赖，例如：
    
    class Plugin extends PluginBase
    {
        public $require = ['Vdomah.JWTAuth'];    
    }

