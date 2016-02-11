### Promise

`Promise` が言語レベルでサポートされました!

```javascript
// ES5.1
Image.load('foo.jpg', function (image) {
  // 成功時
}, function (error) {
  // エラー処理
});
```

```javascript
// ES6
Image.load('foo.jpg')
  .then(function (image) {
    // 成功時
  })
  .catch(function (error) {
    // エラー処理
  });
```
