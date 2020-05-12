# Javascript 规范

## 语法

- 缩进使用soft tab(4个空格)。
- 参数之间用', '分隔，注意逗号后有一个空格。

```javascript
function test(m, n) {
    var x = 0;
    x++;
}

```

- 一元运算符与变量之间无空格，二元运算符两边各保留一个空格。
- 对象的属性与冒号之间无空格，冒号与属性值之间保留空格。
- 对象属性名不要加引号，最后一个属性不要添加逗号。
- 括号“{ }、[] 、()"使用前保留一个空格.
- 声明函数时，大括号“{”后换行，“}"独占一行。
- 定义变量时，大括号"{}"和方括号“[]”可写成一行，包裹字符两边保留一个空格。
- 圆括号"{}"包裹字符两边无空格。
- 函数之间、代码块之间和文件末尾保留一行空行。

```javascript
var country = [ China, Janpan, Korea ];
var car = { color: blue, logo: BMW };
var person = {
    name: 'jack',
    age: 42
}

person.age++;

if (person.age > 24) {
    
}
```

- 最外层使用单引号。

``` javascript
var template = '<div class="test"></div>';
```

- 使用typeof和字符串'undefined'对变量进行判断。
- 用'===', '!=='代替'==', '!='。
- 不要混用tab和空格。

```javascript
if (typeof name === 'undefined') {
    
}
```


- 用函数命名表达式，并定义函数名，而不是函数声明。

```javascript
// 不好的
function test() {

}
// 好的
var getInfo = function () {};
```
- 把立即执行函数包裹在圆括号里。

```javascript
(function () {

});
```

- 布尔值用缩写，而字符串和数字要明确比较对象。

```javascript
if(isUse) {

}

if(name !== 'Jack') {

}

if(arr.length > 0) {

}
```
- 在语句开始执行强制类型转换。

```javascript
var name = String(007);
var number = Number('007');
```


- jQuery对象用$变量表示,Class命名中划线转成驼峰法。

```javascript
var $sidebar = $('.sidebar');
var $sidebarBtn = $('.sidebar-btn');
```

- 赋值统一使用const,每个变量单独使用const命名。

```javascript
// 不好的
const name = 'Jack',
      age = 24;
// 好的
const name = 'Jack';
const age = 24;
```

- 使用字面量生成对象或数组。

```javascript
// 不好的
const person = new Object();
const country = new Array();
// 好的
const person = {};
const country = [];
```

- 对象方法简写。

```javascript
// 不好的
const person = {
    name: 'jack',
    getAge: function(){

    }
};
// 好的
const person = {
    name: 'jack',
    getAge(){

    }
};
```

- 使用属性值缩写,放在所有属性前面。

```javascript
const madeInChina = 'made in china';
//不好的
const product = {
    madeInChina: madeInChina,
    name: 'car'
};
//好的
const product = {
    madeInChina,
    name: 'car'
};
```

- 对象浅拷贝时，使用扩展运算符，而不要使用Object.assignObject.assign，获取对象属性时，使用解构运算符。

```javascript
// 浅拷贝 copy = { a: 1, b: 2, c: 3 }
const original = {
    a: 1,
    b: 2
};
const copy = {
    ...original,
    c: 3
}
// 解构 notA = { b: 2, c: 3 }
const { a, ...notA } = copy;
```
- Array浅拷贝时，使用扩展运算符。

```javascript
const country =  [ 'China', 'Janpan', 'Korea' ];
const copy = [ ...country ];
```

- 二维数组和类数组声明格式如下。

```javascript
const arr = [ [0, 1], [2, 3], [4, 5] ];

const employees = [
  {
    id: 003,
    name: 'Jack'
  },
  {
    id: 008,
    name: 'Games'
  }
];
```
- 用对象或数组进行解构。

```javascript
const employee = { id: 003, name: 'Jack' };
const { id, name } = employee;

const arr = [ 1, 2, 3 ];
const [ first, second ] = arr;
```

- 使用字符串模版``。

```javascript
const name = 'Jack';
const template = `welcome to join us, ${name}`;
```
- 不要保存this，使用箭头函数绑定。
- 在函数或方法内部使用箭头函数。

```javascript
const test = function() {
  return () => {
    console.log(this);
  };
}
```

- 不要用import通配符“*”。

```javascript
// 不好的
import * as CodeGuide from './CodeGuide';

// 好的
import CodeGuide from './CodeGuide';

```

- 在一个单一导出模块里，用 export default。

```javascript
// 不好的
export function test() {}

// 好的
export default function test() {}

```

## 注释

- 单行注释

独占一行，斜杠后留取一个空格。

```javascript
// 搜索
function search() {}
```

- 多行注释

避免使用”/**/“，使用多个单行注释。

```javascript
// 测试
// if() {

// }else {

// }
```

- 模块注释

```javascript
/* 测试 - begin */
if() {

}else {

}
/* 测试 - end */
```

- 文件注释 js doc
- 函数注释 js doc

注释参考 js doc guide。

```javascript
/**
 * @file Jack
 * @author Jack <jack@gmail.com> 
 */

 /**
 * @func
 * @desc 测试
 * @param {string} name - 姓名
 */
function test(name) {}
```
