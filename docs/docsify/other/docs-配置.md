# docsify轻量级文档系统

[![96](https://upload.jianshu.io/users/upload_avatars/686941/9cc6f6fb-1a1b-4d7b-8059-db22059b2c88.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96)](https://www.jianshu.com/u/14161faaa57e)

## root安装

推荐安装 docsify-cli 工具，可以方便创建及本地预览文档网站。

```markdown
npm i docsify-cli -g
```

## 普通用户下初始化项目

如果想在项目的 ./docs 目录里写文档，直接通过 init 初始化项目。

```markdown
docsify init ./docs
```

## 开始写文档

初始化成功后，可以看到 ./docs 目录下创建的几个文件

```
index.html 入口文件
README.md 会做为主页内容渲染
.nojekyll 用于阻止 GitHub Pages 会忽略掉下划线开头的文件
```

直接编辑 docs/README.md 就能更新网站内容，当然也可以写多个页面。

## 本地预览网站

运行一个本地服务器通过 docsify serve 可以方便的预览效果，而且提供 LiveReload 功能，可以让实时的预览。默认访问 `http://localhost:3000` 。

```
docsify serve docs
```

如果需要启动其他端口，可以直接在后面增加`-p 4000`表示启动端口为4000

更多命令行工具用法，参考 [docsify-cli](https://github.com/docsifyjs/docsify-cli) 文档。

## 手动初始化

如果不喜欢 npm 或者觉得安装工具太麻烦，我们其实只需要直接创建一个 index.html 文件。

index.html

```html
<!DOCTYPE html>
<html>
<head>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <meta charset="UTF-8">
  <link rel="stylesheet" href="//unpkg.com/docsify/themes/vue.css">
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      //...
    }
  </script>
  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
</body>
</html>
```

## 更多文档说明{docsify-ignore}

请访问 [docsify轻量级文档](https://docsify.js.org/#/zh-cn/quickstart) 的中文文档页面进行阅读。

## 附录{docsify-ignore}

### 我的目录结构

```
.
├── README.md
├── _sidebar.md              -- 目录索引
├── assets
│   ├── docsify.min.js       -- 从官网拉取下来的js
│   ├── theme-custom.css     -- 自定义的样式
│   └── theme-simple.css     -- 从官网拉取下来主题样式，修改过的本地css
├── index.html               -- 入口页面
├── start.sh                 -- 启动脚本
└── documents          --存放markdown文档的目录
```

### 我的index.html文件

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
  <meta name="description" content="Description">
  <meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">

  <!-- Theme: Simple -->
  <!--
  <link rel="stylesheet" href="https://unpkg.com/docsify-themeable/dist/css/theme-simple.css">
  -->
  <link rel="stylesheet" href="assets/theme-simple.css">

  <!-- Custom theme stylesheet -->
  <link rel="stylesheet" href="assets/theme-custom.css">


  <style>
        nav.app-nav li ul {
            min-width: 100px;
        }

  </style>
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      //定义路由别名，可以更自由的定义路由规则。 支持正则。
      alias: {
            '/.*/_sidebar.md': '/_sidebar.md'
      },
      // 加载 _sidebar.md,加载自定义侧边栏
      loadSidebar: true,
      //加载自定义导航栏
      loadNavbar: false,
      // 强制悬停,切换页面后是否自动跳转到页面顶部。
      auto2top: true,
      // 调整副标题的级数
      subMaxLevel: 2,
      // 替换主题色
      themeColor: '#4CAF50',
      themeable: {
          readyTransition : true, // default
          responsiveTables: true  // default
      },

      showLevel: true,
      //文档标题，会显示在侧边栏顶部。
      name: '',
      //配置仓库地址或者 username/repo 的字符串，会在页面右上角渲染一个 GitHub Corner 挂件。
      repo: '',
      //禁用 emoji 解析
      noEmoji: true,
      tocLevel: 6,
      //搜索配置项
      search: {
        maxAge: 86400000, // 过期时间，单位毫秒，默认一天
        paths: 'auto', // or 'auto'
        placeholder: '搜索',
        noData: '找不到结果',
        // 搜索标题的最大程级, 1 - 6
        depth: 4
      },
      pagination: {
        previousText: '上一章节',
        nextText: '下一章节',
      }

    }
  </script>

  <script src="//unpkg.com/docsify/lib/docsify.min.js"></script>
  <script src="//unpkg.com/docsify/lib/plugins/search.min.js"></script>
  <script src="//unpkg.com/docsify-pagination/dist/docsify-pagination.min.js"></script>
  <script src="//unpkg.com/docsify-copy-code"></script>
  <script src="//unpkg.com/prismjs/components/prism-sql.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-http.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-json.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-bash.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-java.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-markdown.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-nginx.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-php.min.js"></script>
  <script src="//unpkg.com/prismjs/components/prism-python.min.js"></script>
  <script src="//unpkg.com/docsify-pagination/dist/docsify-pagination.min.js"></script>

  <!-- docsify-themeable -->
  <script src="https://unpkg.com/docsify-themeable"></script>


</body>
</html>
```

