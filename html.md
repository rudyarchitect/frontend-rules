# HTML规范

## 语法
- 文档类型使用HTML5规范，doctype大写。
- 在html标签上设置正确的lang属性。
- 使用IE Edge兼容模式。
- 使用无BOM(Byte Order Mark)的UTF-8编码，作为head标签第一个子元素。
- 使用title标签，在编码声明标签之后。
- 保证favicon可访问。
- 引入js和css文件无需添加type属性值，css文件要添加rel="stylesheet"属性。
- 使用soft tab（4个空格）作为缩进层级。
- 使用id作为元素选择hook，不允许使用class。
- 属性使用双引号，不允许使用单引号,布尔类型属性勿添加属性值,自定义属性添加“data-"前缀。
- 标签名使用小写，自闭合标签无需添加“/”，允许自闭合标签勿使用自闭合规则。
- 图片属性src不能为空，添加alt属性，勿添加title属性。
- 省略外链资源URL协议部分http/https。

e.g.
```html
<!DOCTYPE html>
<html lang="zh-CN">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=Edge">
        <title>Page title</title>
        <!--css -->
        <link rel="stylesheet" href="//www.google.com/code-standard.css">
        <style>
        .container {
        }
        </style>
    </head>
    <body>
        <div id="hook" class="container">
            <img src="./logo.svg" alt="Logo">
            <input type="text" disabled>
            <ul data-select="logo">
                <li>google</li>
                <li>facebook</li>
            </ul>
        </div>
        <!--javascript-->
        <script src="code-standard.js"></script>
        <script>
            const container = document.getElementById("hook");
        </script>
    </body>
</html>
```

## 标签属性顺序

属性按照如下顺序，保证易读性；

- class
- id
- name
- data-*
- src, for, type, href, value , max-length, max, min, pattern
- placeholder, title, alt
- aria-*, role
- required, readonly, disabled

```html
<input class="search" id="input" placeholder="Please input something what you want to know." required>
```

## 标签语义化
常见标签语义

- p - 段落
- h1,h2,h3,h4,h5,h6 - 层级标题
- hgroup - 包含大标题和子标题
- strong,em - 强调
- ins - 插入
- del - 删除
- abbr - 缩写
- code - 代码标识
- q - 引用
- blockquote - 一段或长篇引用
- nav - 目录导航
- ul - 无序列表
- ol - 有序列表
- dl,dt,dd - 定义列表
- time - 日期

## 注释

注意注释内容两边留取空格。

- 单行注释

```html
<!-- 搜索框 -->
<input class="search">
```
- 模块注释

```html
<!-- 搜索功能 - begin -->
<div class="search"></div>
<!-- 搜索功能 - end -->
```