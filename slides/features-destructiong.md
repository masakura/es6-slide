### destructiong, ...

配列を小分けできるようになりました!

```javascript
// ES5.1
var array = [1, 2, 3, 4, 5];

var a1 = array[0];
var a2 = array[1];
var rest = array.slice(2);
```

```javascript
// ES6

var array = [1, 2, 3, 4, 5];

var [a1, a2, ...rest] = array;
```

* 関数の戻り値で複数の値を返せるようにも...

[参考: MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Operators/Destructuring_assignment)
