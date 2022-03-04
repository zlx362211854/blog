# AMD,CMD,CommonJs,ESModule等规范简介


## 1. AMD

AMD 是 RequireJS 在推广过程中对模块定义的规范化产出,它是一个概念，RequireJS是对这个概念的实现



```javascript
define(['package/a.js'], function(a) {
	function log() {
		a.log()
	}
	return {
		log
	}
})
```

关键词：**依赖前置**，所需依赖在最开头定义好


## 2. CMD

**CMD** 是**SeaJS**在推广过程中对模块定义的规范化产出，是一个同步模块定义，是SeaJS的一个标准

```js
define(function(require, exports, module) {
  const a = require('package/a.js')
  a.log()
})
```

关键词：依赖就近引入，在哪里用就在哪里引


## 3. CommonJs

**CommonJS规范--** -是通过**module.exports定**义的，在前端浏览器里面并不支持[module](https://so.csdn.net/so/search?q=module&spm=1001.2101.3001.7020).exports,通过node.js后端使用的


## 4. ES6 Module

**通过export，import对模块进行导出导入的**

关键词：**编译时**就能确定模块的依赖关系，只会引入模块需要的依赖，多次import统一模块，只加载一次，加载性能更高。
