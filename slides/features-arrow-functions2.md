### arrow functions

```javascript
// 基本形
foo((a, b) => { return a + b; });

// {} を省略すると return が不要に
foo((a, b) => a + b);

// 引数がひとつの場合は () を省略可能
foo(a => a * 2);

// 引数がない場合は () を省略できない
foo(() => 1 + 2);
```
