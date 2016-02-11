### arrow functions

関数の呼び出しが単純化されました! (実はもっと強力...)

```javascript
// ES5.1
var obj = {
  display: function () {}
  init: function () {
    var that = this;

    document.addEventListener('load', function () {
      that.display();
    });
  }
};
```

```javascript
// ES5.1
var obj = {
  display: function () {}
  init: function () {
    var that = this;

    document.addEventListener('load', () => this.display());
  }
};
```
