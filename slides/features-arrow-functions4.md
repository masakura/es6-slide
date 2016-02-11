### arrow functions

`arrow functions` では `this` は外側の `this` を束縛します。便利だけど、`function` の代わりに使えるところと使えないところがあります。

```javascript
$('#button1').on('click', () => {
  // この this はボタンではなく、外側の this なので
  // 期待通りには動きません
  var $button1 = $(this);

  // ...
});
```
