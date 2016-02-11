### rest parameters

関数の残りの引数を簡単に取得できるようになりました!

```javascript
// ES5.1
function hoge (name) {
  var args = Array.prototype.slice.call(arguments, hoge.length);

  // ...
}
```

```javascript
// ES6
function hoge (name, ...args) {
  // ...
}
```

しかも、`arguments` と違って配列として扱えます!
