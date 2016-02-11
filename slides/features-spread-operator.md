### Spread operator

関数の引数で配列を展開して呼び出したり、配列の合成がやりやすくなりました!

```javascript
// ES5.1
foo.display.apply(null, array1);

console.log(array1.concat(array2));
```

```javascript
// ES6
foo(...array1);

console.log([...array1, ...array2]);
```

[参考: MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Function/apply)
