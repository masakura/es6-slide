### object literal extensions

オブジェクトリテラルの書き方が簡素化されました!

```javascript
// ES5.1
function hoge(foo, bar) {
  var obj = {
    foo: foo,
    bar: bar,
    buzz: function () {}
  };
  obj[foo + '1'] = true;
  return obj;
}
```

```javascript
// ES6
function hoge(foo, bar) {
  return {
    foo,
    bar,
    [foo + '1']: true,
    buzz() {}
  };
}
```
