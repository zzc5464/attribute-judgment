# javascript判断属性的四种方法
## typeof
- console.log(typeof undefined)//'undefined'
- console.log(typeof null) // well-known bug
- console.log(typeof true) //'boolean'
- console.log(typeof 123)  //'number'
- console.log(typeof "abc")  //'string'
- console.log(typeof function() {}) //'function'
- console.log(typeof {}) //'object'
- console.log(typeof [])//'object'
- console.log(typeof unknownVariable) //'undefined'
### Typeof存在的问题
- 在使用 typeof 运算符时采用引用类型存储值会出现一个问题，无论引用的是什么类型的对象（[] {} ），它都返回 "object"。
## toString.call
- console.log(toString.call(123)) //[object Number]
- console.log(toString.call('123')) //[object String]
- console.log(toString.call(undefined)) //[object Undefined]
- console.log(toString.call(true)) //[object Boolean]
- console.log(toString.call({})) //[object Object]
- console.log(toString.call([])) //[object Array]
- console.log(toString.call(function(){})) //[object Function]
### 面试，笔试必考，框架开发必用，五星级知识点
## instanceof
- var arr=[]
- var arr = new Array()console.log(arr instanceof Array) //---------------> true
- console.log(date instanceof Date)     //---------------> true
- console.log(fn instanceof Function)   //------------> true
###  注意：instanceof 后面一定要是对象类型，并且大小写不能错，该方法适合一些条件选择或分支。
## constructor
- console.log(arr.constructor === Array)   //----------> true
- console.log(date.constructor === Date)   //-----------> true
- console.log(fn.constructor === Function) //-------> true
### 根据对象的constructor属性判断 ： constructor
## Jquery中
- //    jQuery提供一系列工具方法，用来判断数据类型，以弥补JavaScript原生的typeof运算符的不足。
- //     以下方法对参数进行判断，返回一个布尔值。
- //    jQuery.isArray()：是否为数组。
- //    jQuery.isEmptyObject()：是否为空对象（不含可枚举的属性）。
- //    jQuery.isFunction()：是否为函数。
- //    jQuery.isNumeric()：是否为数字。
- //     jQuery.isPlainObject()：是否为使用“{}”或“new Object”生成的对象，而不是浏览器原生提供的对象。
- //     jQuery.isWindow()：是否为window对象。
- //    jQuery.isXMLDoc()：判断一个DOM节点是否处于XML文档之中。
