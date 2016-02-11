### 使う意味はある?

例えば、ES5.1 の型宣言はどこまでが型か分かりにくい。

```javascript
// ES5.1 スタイルの型宣言
var Foo = function () {};
Foo.prototype.hoge = function () {};
Foo.prototype.fuga = function () {};
var Bar = function () {};
Bar.piyo = function () {};
```

```javascript
// ES6 class を使った型宣言
class Foo {
  hoge() {}
  fuga() {}
}
class Bar {
  static piyo() {}
}
```

* この例は等価ではありません!
