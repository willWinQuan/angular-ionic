# angular-ionic
angular,ionic学习笔记

# （一）IONIC介绍：
Ionic是基于Cordova的使用Web技术开发混合应用的前台基于Angular的框架，Ionic1使用的是Angular1，Ionic2之后使用的都是Angular2技术栈，Ionic以后更多的新版本也都是在2的版本上迭代。Ionic2之后只支持android4.3以上的版本。

# （二）Angular主要有五个核心特性：
双向数据绑定—— 实现了把model与view完全绑定在一起，model变化，view也变化，反之亦然。

模板—— 在AngularJS中，模板相当于HTML文件被浏览器解析到DOM中，AngularJS遍历这些DOM，也就是说AuguarJS把模板当做DOM来操作，去生成一些指令来完成对view的数据绑定。

MVVM—— 吸收了传统的MVC设计模式针但又并不执行传统意义上的MVC，更接近于MVVM(Moodel-View-ViewModel)。

依赖注入—— AngularJS拥有内建的依赖注入子系统，可以帮助开发人员更容易的开发，理解和测试应用。

指令—— 可以用来创建自定义的标签，也可以用来装饰元素或者操作DOM属性

ionic主要包括三个部分：

CSS框架- 提供原生_App质感的CSS样式模拟_。ionic这部分的实现使用了ionicons图标样式库。

JavaScript框架- ionic基于AngularJS基础框架开发，遵循AngularJS的框架约束；主要提供了适应移动端UI的 AngularJS的扩展，主要包括指令和服务。此外，ionic使用AngularUI Router来实现前端路由。

命令行/CLI- 命令行工具集用来简化应用的开发、构造和仿真运行。ionic命令行工具使用了 Cordova，依赖于平台SDK（Android & iOS）实现将移动web项目打包成原生app。

由于ionic使用了HTML5和CSS3的一些新规范，所以要求iOS7+/Android4.1+。 在低于这些版本的手机上使用ionic开发的应用，有时会发生莫名其妙的问题。

# (三)搭建Ionic应用

1）安装node.js  npm

2）安装Ionic CLI、cordova；

npm install -g ionic cordova

注意：ionic cordova 的ionic 需写在前面

3)通过Ionic创建一个项目

使用Ionic 官方提供的现有应用程序模拟，或一个空白的项目创建一个IONIC应用；

$ ionic start <name> <template> [options]

 Examples:

    $ ionic start 
    $ ionic start --list
    $ ionic start myApp
    $ ionic start myApp blank
    $ ionic start myApp tabs --cordova
    $ ionic start myApp tabs --capacitor
    $ ionic start myApp super --type=ionic-angular
    $ ionic start myApp blank --type=ionic1
    $ ionic start cordovaApp tabs --cordova
    $ ionic start "My App" blank
    $ ionic start "Conference App" https://github.com/ionic-team/ionic-conference-app

进入电脑的某个文件夹，打开命令行：ionic start MyProject conference

start 代表新建一个IONIC应用；Myproject 是项目名称；
conference 是应用模板;

Ionic2内部还有一些其他的模板：

1、tabs:底部三个tabs模板；

2、sidemenu：侧边栏菜单模板；

3、blank：空白模板；

4、my-first-app：一个使用gallery构建相机例子简单模板；

5、conference:是ionic项目组提供的另一个展示ionic框架及组件使用例子的模板；

附：1.angular官网：https://angular.io/
   2.ionic官网：https://ionicframework.com/docs/

# 问题解决
  1.运行安装ionic(cnpm install -g ionic) 
    问题：报错信息：SyntaxError: Unexpected end of JSON input (file: C:\Users\HP\AppData\Roaming\npm\node_modules\cordova\node_modules\_path-exists@3.0.0@path-exists\package.json)
    解决方法：npm cache clean --force 清空本地缓存
  2.如使用angular 先安装angular
    npm install -g @angular/cli