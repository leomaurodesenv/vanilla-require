# vanilla-require

[![GPLv3 license](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE.md)
[![npm](https://img.shields.io/badge/Code-npm-yellow.svg)](https://www.npmjs.com/package/vanilla-require)
[![JsClasses](https://img.shields.io/badge/Code-JsClasses-yellow.svg)](https://www.jsclasses.org/vanilla-require)
[![GitHub](https://img.shields.io/badge/Code-GitHub-yellow.svg)](https://github.com/leomaurodesenv/vanilla-require)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/b577b1fd54e7442bb6adf61b1c5ffb7c)](https://www.codacy.com/app/leomaurodesenv/vanilla-require?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=leomaurodesenv/vanilla-require&amp;utm_campaign=Badge_Grade)

---
The Node.js and npm have an incredible system for the inclusion of packages, made by `require`.
However, for use packages one must export their modules, through `module.exports`. Yet, it is not possible to use these packages on simple web classes because the web browser does not recognize the `module.exports`.  

This package allows you to develop simple classes to the web and export them to Node.js script as a module. In this sense, you can use your classes in the web browser (pure Javascript) and in the Node.js script, using the `vanilla-require` package.  

[Vanilla JS](http://vanilla-js.com/): pure Javascript.  

---
## Installation

```shell
npm install --save vanilla-require
```

---
## Example

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
## Also look ~

-   [License GPL v3](LICENSE)
-   Create by Leonardo Mauro ~ [leomaurodesenv](https://github.com/leomaurodesenv/)
