### arrow functions

関数をより簡単に書けます! (実はもっと強力...)

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
// ES6
var obj = {
  display: function () {}
  init: function () {
    document.addEventListener('load', () => this.display());
  }
};
```
