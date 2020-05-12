# 命名规范

命名规范应当遵循简洁和语义化的原则。常用的命名法如下所示：

- 驼峰命名法：通过首字母大写分割单词，根据第一个字母是否大小写可分为大驼峰和小驼峰命名法。
- 中划线命名法：通过中划线区分割单词。
- 下划线命名法：通过下划线分割单词。

## 目录

1. [项目命名](#项目命名)
2. [目录命名](#目录命名)
3. [文件命名](#文件命名)
4. [常量命名](#常量命名)
5. [变量命名](#变量命名)
6. [函数命名](#函数命名)
7. [类命名](#类命名)
8. [样式命名](#样式命名)

## 项目命名
- 采用中划线命名法。
- 命名规范：全部采用小写。

e.g. vedio-editor

## 目录命名

- [2.1] 采用小驼峰命名法。
- 命名规范：采用复数命名。

e.g. templates,mockResponses

- [2.2] 组件命名无需采用复数。

e.g. editorUploadFile

**[返回目录](#目录)**

## 文件命名

- 采用驼峰命名法。
- 命名规范：常规文件采用小驼峰，框架文件采用大驼峰。

e.g. 

- editorUploadFile.js
- editorUploadFile.css
- editorUploadFile.html
- EditerUploadFile.vue
- EditerUploadFile.jsx

**[返回目录](#目录)**

## 常量命名

- 采用下划线命名法。
- 命名规范：全部采用大写。

e.g. 

- MAX_COUNT

**[返回目录](#目录)**

## 变量命名

- 采用小驼峰命名法。
- 命名规范：前缀勿采用动词，常见单词建议采用缩写。

```javascript
//好的命名
let fileName;
//不好的命名
let setName;
```

**[返回目录](#目录)**

## 函数命名

- 采用小驼峰命名法。
- 命名规范：前缀采用动词，常见单词建议采用缩写。

常见动词前缀：

- can 
- get
- set
- load
- has
- is
- on

e.g. 

```javascript
//好的命名
function getFileInfo() {}

//不好的命名
function fileInfo() {}
```

**[返回目录](#目录)**

## 类命名

- 采用大驼峰命名法。
- 命名规范：使用名词。

e.g. 

- class File {}

**[返回目录](#目录)**    

## 样式命名

采用单一职责和单一来源原则。
+ 组件样式规则
  * 采用大驼峰命名法，表示一个模块。
  * 双下划线表示一个元素。
  * 双中划线表示一个修饰符。

```css
.SearchComponent {

}

.SearchComponent__input {

}

.SearchComponent--disabled {
    
}
```

**[返回目录](#目录)**    

