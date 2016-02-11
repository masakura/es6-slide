### for...of loops

ようやく `foreach` が JavaScript にも!

```javascript
// ES5.1
for (var i = 0; i < array.length; i++) {
  var item = array[i];

  // ...
}
```

```javascript
// ES6
for (var item of array) {
  // ...
}
```

* for..in があると思った人! バグの温床なので要注意!
