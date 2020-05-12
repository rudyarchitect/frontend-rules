# CSS规范

## 语法

- 使用soft tab（4个空格）作为缩进。
- 每个属性独占一行，末尾添加分号。
- 选择器与括号之间保留空格。
- 属性与冒号之间无空格，冒号与属性值之间保留空格。
- 列表类型属性值书写单行时，逗号后保留空格。

```css
.selector {
    margin: 0;
    font-family: Arial, sans-serif;
}
```

- 多个选择器时，每个选择器独占一行。
- 选择器样式之间空一行。
- 属性选择器的值使用双引号。
- 勿使用id作为选择器。

```css
.tab,
.nav,
.list[data-type = "search"] {

}

.container{

}
```

- 使用属性缩写。

```css
/* 好的样式 */
.container {
    border: 1px solid #efefef;
}
/* 不好的样式 */
.container {
    border-width: 1px;
    border-style: solid;
    border-color: #efefef;
}
```

- 省略外链资源URL协议部分http/https,并添加双引号。

```css
.container {
    background-image: url("//www.google.com/background.png");
}
```
- 勿使用!important声明。
- 0到1之间的数值省略0，长度为0时省略单位。

```css
.nav {
    margin: 0;
    opacity: .8;
}
```

- 颜色值采用小写，尽量采用缩写，勿使用命名色值。
- 属性font-weight使用数值描述。

```css
/* 好的样式 */
.article {
    font-weight: 600;
    background-color: #efc;
}
/* 不好的样式 */
.article {
    font-weight: bold;
    background-color: #eeffcc;
}
```

- 带私有前缀的属性由长到短排列，按冒号位置对齐。

```css
.sidebar {
    -webkit-transition: color 1s;
       -moz-transition: color 1s;
            transition: color 1s;
}
```

## 属性书写顺序

按功能进行分组：
- 若包含content 属性，放在最前面。
- 布局方式和位置: position / top / right / bottom / left / float / display / overflow 等。
- 尺寸：border / margin / padding / width / height 等。
- 文本相关：font / line-height / text-align / word-wrap 等。
- 视觉效果：background / color / transition / list-style 等。

```css
.sidebar {
    /* 布局方式和位置 */
    position: absolute;
    top: 50px;
    left: 0;
    overflow-x: hidden;

    /* 尺寸 */
    width: 200px;
    padding: 5px;
    border: 1px solid #ddd;

    /* 文本 */
    font-size: 14px;
    line-height: 20px;

    /* 视觉效果 */
    background: #f5f5f5;
    color: #333;
    -webkit-transition: color 1s;
       -moz-transition: color 1s;
            transition: color 1s;
}
```

## 注释

- 单行注释

```css
/* 搜索框 */
.search-input {

}
```
- 模块注释

```css
/* 搜索组件 - begin */
.search-input {

}

.search-button {

}
/* 搜索框 - end */
```
