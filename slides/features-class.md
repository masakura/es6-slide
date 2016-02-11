### class

型が簡単に宣言できます!

```javascript
// ES5.1
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

* 厳密にはこの二つは同じではありません
* `class` は糖衣構文で、プロトタイプなのは変わりません
