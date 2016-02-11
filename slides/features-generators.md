### generators

配列ではないけど、イテレーションが可能な関数を簡単に作れるように!

```javascript
class Range {
  constructor(start, end) {
    this._start = start;
    this._end = end;
  }
  *[Symbol.iterator] () {
    for (var i = this._start; i <= this._end; i++) {
      yield i;
    }
  }
}

// 1 2 3 4 の順で表示される
for (let i of new Range(1, 3)) {
  console.log(i);
}
```
