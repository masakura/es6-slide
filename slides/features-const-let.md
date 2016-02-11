### const/let

`const` や `let` で宣言した変数はブロックスコープになります。

```javascript
// ES5.1
var text = 'abc';

if (true) {
  var text = 'def';
  // ...
}

console.log(text); // 'def'
```

```javascript
// ES6
let text = 'abc';

if (true) {
  let text = 'def';
  // ...
  }

console.log(text); // 'abc';
```
