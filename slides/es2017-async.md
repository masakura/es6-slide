### Async Functions

.NET Framework の非同期関数の仕組みが ES にも!

```javascript
// ES6
Image.load('foo.jpg')
  .then(image => {
    // ...
  });
```

```javascript
(async function () {
  var image = await Image.load('foo.jpg');

  // ...
})();
```
