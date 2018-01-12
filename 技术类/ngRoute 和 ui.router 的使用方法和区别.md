在单页面应用中要把各个分散的视图给组织起来是通过路由机制来实现的。本文主要对 AngularJS 原生的 `ngRoute` 路由模块和第三方路由模块 `ui.router` 的用法进行简单介绍，并做一个对比。

[](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#ngRoute "ngRoute")ngRoute
--------------------------------------------------------------------------------------------------

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#使用方法 "使用方法")使用方法

1) 引入 `angular-route` lib

无论是 `ngRoute` 还是 `ui.router` ，作为框架额外的附加功能，都必须以 `模块依赖` 的形式被引入。

    1

    \<script src="lib/angular-route.js"\>\</script\>

<>

2) 配置路由

    1
    2
    3
    4
    5
    6
    7
    8
    9

    var app = angular.module('ngRouteApp', ['ngRoute']);

    app.config(function($routeProvider){
     $routeProvider
     .when('/Main', {
     templateUrl: "main.html",
     controller: 'MainCtrl'
     })
     .otherwise({ redirectTo: '/tabs' });

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#服务与指令 "服务与指令")服务与指令

`ngRoute` 路由模块名

`$routeProvider` 服务提供者，用来定义一个路由表，即地址栏与视图模板的映射，对应于 `ui.router` 中的 `urlRouterProvider` 和 `stateProvider`

`$route` 服务，完成路由匹配，并且提供路由相关的属性访问及事件，如访问当前路由对应的 Controller，对应于下面的 `$urlRouter` 和 `$state`
`$routeParams` 服务，保存了地址栏中的参数，对应于下面的 `$stateParams`

`ng-view` 指令，用来在主视图中指定加载子视图的区域，对应于下面的 `ui-view`

[](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#ui-router "ui.router")ui.router
--------------------------------------------------------------------------------------------------------

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#使用方法-1 "使用方法")使用方法

1) 引入 `angular-ui-router` lib

    1

    \<script src="lib/angular-ui-router.min.js"\>\</script\>

2) 配置路由

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10

    var app = angular.module("uiRouteApp", ["ui.router"]);

    app.config(function($urlRouterProvider, $stateProvider) {
     $urlRouterProvider.otherwise("/index");
     $stateProvider
     .state("Main", {
     url: "/main",
     templateUrl: "main.html",
     controller: 'MainCtrl'
     })

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#服务与指令-1 "服务与指令")服务与指令

`ui.router` 路由模块名

`$urlRouterProvider` 服务提供者，用来配置路由重定向
`$stateProvider` 服务提供者，用来配置路由

`$urlRouter` 服务
`$state` 服务，用来显示当前路由状态信息，以及一些路由方法（如：跳转）
`$stateParams` 服务，用来存储路由匹配时的参数

`ui-view` 指令，路由模板渲染，对应的 dom 相关联
`ui-sref` 指令，链接到特定状态

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#路由的创建 "路由的创建")路由的创建

#### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#基本配置 "基本配置")基本配置

调用 `$stateProvider.state(...)` 方法，并可配置以下参数

    1
    2
    3
    4
    5
    6

    $stateProvider
     .state("Main", {
     url: "/main",
     templateUrl: 'main.html',
     controller: 'MainCtrl',
     })

#### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#parent "parent")parent

有两种方式可以指定父子状态关系。

一种是，使用点标记法，像本文最后嵌套视图部分举得栗子那样：

    1

    .state("tabs.tab1", {})

另一种是，使用 `parent` 属性

    1
    2
    3

    .state("tab1", {
     parent: 'tabs' // 也可是一个状态对象， parent: tabs
    })

#### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#abstract "abstract")abstract

使用 `abstract` 可以为所有的子状态提供一个基 `URL`，这样做的好处就是可以在抽象出来的这个状态所对应的 `html` 页面中来定义静态资源。抽象模板不能被激活。

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10

    $stateProvider
     .state('contacts', {
     abstract: true,
     url: '/contacts',
     templateUrl: 'contacts.html',
     })
     .state('contacts.list', {
     url: '/list',
     templateUrl: 'contacts.list.html'
     })

#### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#resolve "resolve")resolve

`resolve` 在 `state` 配置参数中，是一个对象(`key-value`)，每一个 `value` 都是一个可以依赖注入的函数，并且返回的是一个 `promise` (当然也可以是值)。

    1
    2
    3
    4
    5
    6

    resolve: {
     'myResolve': ['contacts',
     function(contacts){
     return contacts.all();
     }]
     }

这样做的目的：

* 简化了 `controller` 的操作，将数据的获取放在 `resolve` 中进行，这在多个视图多个 `controller` 需要相同数据时，有一定的作用。
* 只有当 `reslove` 中的 `promise` 全部 `resolved`(即数据获取成功)后，才会触发 `$stateChangeSuccess`切换路由，进而实例化 `controller`，然后更新模板。

更多参数可参考 [angular 系列八 ui-router详细介绍及ngRoute工具区别](http://yijiebuyi.com/blog/3aab7ad8bccb22b4a881849c0593d5e2.html) 中 state 参数的讲解。

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#路由控制 "路由控制")路由控制

`url` 动态部分被称为参数，有以下几种方式设置

1） 使用花括号的方式可以设置一个正则表达式规则的参数：

    1
    2

    //只会匹配 pageId 为1到8位的数字
    url: "/pages/{pageId:[0-9]{1,8}}"

可以通过 `?` 来指定参数作为查询参数

    1
    2

    //比如匹配 href="/page?type='new'"
    url: "/page?type"

如果需要不止一个查询参数，用 `&` 分隔：

    1
    2

    //比如匹配 ui-sref="page({type:'all', title:'test ui-router'})"
    url: "/page?type&title"

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#路由的查找匹配 "路由的查找匹配")路由的查找匹配

* `angular` 在刚开始的 `$digest` 时，`$rootScope` 会触发 `$locationChangeSuccess` 事件（`angular`在每次浏览器 `hash` change 的时候也会触发 `$locationChangeSuccess` 事件）
* `ui.router` 监听了 `$locationChangeSuccess` 事件，于是开始通过遍历一系列 `rules`，进行路由查找匹配列表项
* 当匹配到路由后，就通过 `$state.transitionTo(state,...)`，跳转激活对应的 `state`
* 最后，完成数据请求和模板的渲染

在视图中，建议使用 `ui-sref="xxxState"` 而不是 `href="#/abc"`，这样做能减少一遍 `rules` 循环的遍历，提升性能。

[](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#两者区别 "两者区别")两者区别
-----------------------------------------------------------------------------------------

`ngRoute模块` 是 Angular 自带的路由模块，而 `ui.router模块` 是基于 `ngRoute模块` 开发的第三方模块。

`ui.router` 是基于 `state`(状态)的， `ngRoute` 是基于 `url` 的，`ui.router模块` 具有更强大的功能，主要体现在视图的嵌套方面。

### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#嵌套视图 "嵌套视图")嵌套视图

页面某个动态变化区块中，嵌套着另一个可以动态变化的区块。

前面的栗子就是一个很好的业务场景。

在首页中包含一个动态区块：

    1
    2
    3
    4

    \<body ng-app="ngRouteApp"\>
     \<h3\>AngularJS UI-Router Tabs\</h3\>
     \<div ng-view\>\</div\>
    \</body\>

在标签页中又包含动态区块：

    1
    2
    3
    4
    5
    6

    \<div\>
     \<span\>\<a href="\#/tab1"\>Page-1\</a\>\</span\>
     \<span\>\<a href="\#/tab2"\>Page-2\</a\>\</span\>
     \<span\>\<a href="\#/tab3"\>Page-3\</a\>\</span\>
    \</div\>
    \<div ng-view\>\</div\>

一运行，报了一个这样的错误：

```
RangeError: Maximum call stack size exceeded

```

发现浏览器崩溃了，因为 `ng-view` 会陷入死循环，无限递归下去。

使用 `ui.router` 能很容易解决这个问题，因为它定义的路由有明确的父子关系，并通过 `ui-view` 指令将子路由模版插入到父路由模板的 `<div ui-view></div>` 中去，从而实现视图嵌套。看代码：

    1
    2
    3
    4
    5
    6
    7
    8
    9

    $stateProvider
     .state("tabs", {
     url: "/tabs",
     templateUrl: "pageTab.html"
     })
     .state("tabs.tab1", {
     url: "/tab1",
     templateUrl: "tab1.html"
     })

#### [](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#其他区别 "其他区别")其他区别

ui-router（左） ： ngRoute（右）

* 应用程序内的一个区域 ： 应用程序中的 url
* 可以嵌套的层次结构 ： 只是平面层次结构
* 名称可以自定义 ： 名称只能是 url
* 通过名称或 url 导航 ： 只能通过 url 导航
* 可以存在多个视图（ui-view） ： 只能单一视图（ng-view）
* 可以填充任何视图 ： 只能填充一个视图
* 通过状态填充某一部件 ： 通过指令将填充某一部件

[](http://huangtengfei.com/2015/10/the-useage-of-ng-route-and-ui-router/#参考： "参考：")参考：
--------------------------------------------------------------------------------------

1. [ui.router源码解析](http://www.html-js.com/article/Front-end-source-code-analysis-original-uirouter-source-code-analysis)
2. [AngularJS ui-router (嵌套路由)](http://www.open-open.com/lib/view/open1416878937309.html)
3. [ngRoute VS ui-router](http://www.w3cscript.com/Angular/2014-12-01/29.html)
4. [angular的uiRouter服务学习](http://www.cnblogs.com/liulangmao/p/4155015.html)