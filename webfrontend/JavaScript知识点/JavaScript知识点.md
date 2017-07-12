# 基础知识
1. 原型，原型链
2. 作用域，闭包
3. 异步，单线程

# JS API
1. DOM操作
2. Ajax
3. 事件绑定

# 开发环境
1. 版本管理
2. 模块化
3. 打包工具

# 运行环境
1. 页面渲染
2. 性能优化

# 几个面试题目
1. js中使用 typeof 能得到哪些类型？ => js变量类型
2. 何时使用 === 何时使用 ==？ => 强制类型转换
3. window.onload 和 DOMContentLoaded 的区别？ => 浏览器的渲染过程
4. 用 JS 创建10个 `<a>` 标签，点击的时候弹出对应的序号 => 作用域
5. 简述如何实现一个模块加载器，类似于require.js的基本功能 => js模块化
6. 实现数组的随机排序 => js的基础算法

# js的基础知识

## 变量类型和计算

题目：
- js中使用 typeof 能得到哪些类型
- 何时使用 === 何时使用 ==  
    ```
    if (obj.a == null){
        // 相当于：obj.a === null || obj.a === undefined
        // jquery源码中推荐的写法
    }
    ```
- js中有哪些内置函数
- js变量按照存储方式分为哪些类型，并描述其特点
- 如何理解JSON


typeof 运算符
```
typeof undefined // undefined
typeof 'abc' // string
typeof 123 // number
typeof true // boolean
typeof {} // object
typeof [] // object
typeof null // object
typeof console.log // function
```

变量计算 - 强制类型转换

- 字符串拼接
- == 运算符 
    ```
    100 == '100' //  true
    0 == '' // true
    null == undefined // true
    ```
- if 语句
- 逻辑运算
    ```
    console.log(10 && 0) // 0
    console.log('' || 'abc') // 'abc'
    console.log(!window.abc) // true

    // 判断一个变量是true还是false
    var a = 100
    console.log(!!a)
    ```

js中有哪些内置函数 -- 数据封装类对象：

- Object
- Array
- Boolean
- Number
- String
- Function
- Date
- RegExp
- Error

如何理解JSON：
JSON是一种数据格式
JSON同时也是js对象，它有两个方法：JSON.parse(), JSON.stringify()
