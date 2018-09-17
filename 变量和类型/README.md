## 基础知识一  

### 变量
1. JS中使用typeof能得到哪些类型  

2. === 和 ==   

```
if(obj.a == null) {
    // 相当于 obj.a === null || obj.a === undefined 的简写形式,jquery源码中的推荐写法， 除了这个其他全部 === 
}
```

3. JS中有哪些内置函数  -- 数据封装类对象  
Object
Array
Boolean
Number
String
Function
Date
RegExp
Error
Math(内置对象，并不是函数)  

4. JS变量按照存储方式区分为哪些类型，并描述其特点   -- 值类型 和 引用类型

5. 如何理解JSON  -- 
- JSON只不过是一个JS内置对象而已
JSON.stringify({a: 10, b: 1});
JSON.parse('{"a": 10, "b": 1}');
- JSON也是一种数据格式


- 变量类型
    值类型 VS 引用类型 
    值类型： 
``` 
var a = 100;
var b = a;
a = 200;
console.log(b);    // 100
```

    引用类型: 对象、数组、函数  --- 无限制扩展属性(内存公用空间，节约内存)   
```
var a = {age: 20};
var b = a;
b.age = 21;
console.log(a.age);   // 21
```

- typeof 运算符(六种): 只能区分值类型，不能区分引用类型，但是能区分函数这个引用类型
```
typeof undefined    // undefined
typeof 'abc'        // string
typeof 123          // number
typeof true         // boolean
typeof {}           // object
typeof []           // object
typeof null         // object
typeof console.log  // function  
```

- 变量计算--值类型的强制类型转换  
1. 字符串拼接  
2. ==运算符  
```
100 == '100'
0 == ''
null == underfined
// 以上全为true   === 全为false
```
3. if语句  
4. 逻辑运算符  

- null 和 underfined 

null ： 表示"没有对象"，即该处不应该有值。典型用法是:   
（1） 作为函数的参数，表示该函数的参数不是对象。   
（2） 作为对象原型链的终点。   
```
Object.getPrototypeOf(Object.prototype)
// null
```

undefined: 表示"缺少值"，就是此处应该有一个值，但是还没有定义。典型用法是：   
（1）变量被声明了，但没有赋值时，就等于undefined。  
（2) 调用函数时，应该提供的参数没有提供，该参数等于undefined。   
（3）对象没有赋值的属性，该属性的值为undefined。  
（4）函数没有返回值时，默认返回undefined。   
```
var i;
i // undefined
function f(x){console.log(x)}
f() // undefined
var  o = new Object();
o.p // undefined
var x = f();
x // undefined
```




