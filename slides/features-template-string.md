### template string

文字列の中での変数展開が楽になりました!

```javascript
// ES5.1
var name = 'taro';

var text = name + 'さん、こんにちわ';
```

```javascript
// ES6
var name = 'taro';

var text = `${name}さん、こんにちわ';
```

* 独自のエンジンを書くこともできるようです

[参考: MDN](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/template_strings)
