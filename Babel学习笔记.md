# Babel学习笔记

## babel与polyfill的区别、或者与shim的区别

* _polyfill_:  

    > 用于实现低版本浏览器还不支持的原生API的代码;  

    > polyfill 是 shim 的一种。shim 是将不同 api 封装成一种，比如 jQuery 的 $.ajax 封装了 XMLHttpRequest 和 IE 用 ActiveXObject 方式创建 xhr 对象；
    
    > polyfill 特指 shim 成的 api 是遵循标准的，其典型做法是在IE浏览器中增加 window.XMLHttpRequest ，内部实现使用 ActiveXObject。在实际中为了方便做对比，会特指 shim 的 api 不是遵循标准的，而是自己设计的

* _babel:_  

    > 是一个广泛使用的 ES6 转码器，可以将 ES6 代码转为 ES5 代码。注意：Babel 默认只转换新的 JavaScript 句法（syntax），而不转换新的 API

## babel简介

## babel的缺点

### Babel 把 Javascript 语法 分为 syntax 和 api

* _api_: api 指那些我们可以通过 函数重新覆盖的语法 ，类似 includes,map,includes,Promise,凡是我们能想到重写的都可以归属到 api

* _syntax_: 像 箭头函数，let,const,class, 依赖注入 Decorators,等等这些，我们在 Javascript 在运行是无法重写的，想象下，在不支持的浏览器里不管怎么样，你都用不了 let 这个关键字

