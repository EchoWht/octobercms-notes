# 组件开发

## 先在 *Setting->Misc->Builder* 设置插件作，这样的好处是Bulider会自动识别你自己的插件 

## 新建一个组件

 假设现在要做一个"中国城市 ChinaCity"的扩展(Plugin),这个扩展有一个叫"城市选择 Area"的组件(Component)

1. 先用builder新建一个名为 ChinaCity 的 Plugin
1. 然后新建一个components 文件夹
1. 新建一个名为Area的类继承ComponentBase 同时需要实现componentDetails这个方法 用来介绍这个组件
1. 在Plugin类中的 registerComponents方法中的返回数组中注册这个组件
1. 在components 文件夹中新建一个 与类名相同的文件夹(与Area同名area)，在此文件夹下新建一个default.htm文件
1. 这样一个简单的空白组件就做好了
1. 在底部添加js

  ```html
  {% put scripts %}
  <script src="../plugins/blskye/chinacity/assets/js/distpicker.data.js"></script>
  {% endput %}
  ```

  如果要加后台设置或者权限参考

  https://github.com/rainlab/googleanalytics-plugin/blob/master/Plugin.php
