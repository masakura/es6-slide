### default function parameters

関数の引数に規定値を書けるようになりました!

```javascript
// ES5.1
function hoge (name, type) {
  if (typeof type === 'undefined') type = 'default';

  // ...
}
```

```javascript
// ES6
function hoge (name, type = 'default') {
  // ...
}
```
