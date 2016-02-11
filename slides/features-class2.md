### class

面倒な継承もこの通り!

```javascript
class Foo {
  display() {}
}

// 継承は extends で!
class Bar extends Foo {
  constructor() {
    // 親コンストラクタは super() で!
    super();
  }
  display() {
    // なにかの処理
    super.display();
  }
}
```

* ES5.1 以前の継承は、こう書いたらできたよ! のような感じで、わかりにくかった...
