### arrow functions

個人的には、こんなコードがシンプルに書けるので好きです。

```javascript
// ES5.1
var result = array
  .filter(function (i) {
    return i % 2;
  })
  .map(function (i) {
    return i * i;
  });
```

```javascript
// ES6 では return や function が不要な分、少々長くても一行で書けます
var result = array
  .filter(i => i % 2)
  .map(i => i * i);
```
