# vanilla-require

Links: [npm](https://www.npmjs.com/package/vanilla-require) and [Github](https://github.com/leomaurodesenv/vanilla-require).   

---
The Node and npm have an incredible system for the inclusion of packages, made by `require`.
However, to use packages one must export their modules, through `module.exports`. Yet, it is not possible to use these packages on simple web pages because the web browser does not recognize the `module.exports`.

This package allows you to develop simple classes to the web and export them in Node as a module. In this sense, you can use your classes in the web browser and in the Node, using the `vanilla-require` package.

[Vanilla JS](http://vanilla-js.com/): pure Javascript.   

---
### Installation

```shell
npm install --save vanilla-require
```

---
### Example

See `test/test.js` for another example.   

A Vanilla class (`Calculator.js`):
```js
class Calculator {

    sum(num1, num2){
        return num1+num2;
    }
}
```
   
Your Node code:
```js
/* Include */
const vr = require('vanilla-require')(__dirname);
// Instance a Vanilla Class
const Calculator = vr.require('Calculator.js');

// Enjoy the Class!
let myCalc = new Calculator(),
    a = 2, b = 3;

console.log('a:'+a+' b:'+b)
console.log('sum:'+myCalc.sum(a, b));
```

---  
### Also look ~

* [License GPL v3](LICENSE)
* Create by Leonardo Mauro (leo.mauro.desenv@gmail.com)
* Git: [leomaurodesenv](https://github.com/leomaurodesenv/)
* Site: [Portfolio](http://leonardomauro.com/portfolio/)