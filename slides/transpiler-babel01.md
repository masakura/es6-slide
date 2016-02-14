### Babel

```javascript
// 変換前
class Hoge {
  display() { console.log('Hello, world!'); }
}
```

```javascript
// 変換後
'use strict';

var _createClass = function () { function defineProperties(target, props) { for (var i = 0; i < props.length; i++) { var descriptor = props[i]; descriptor.enumerable = descriptor.enumerable || false; descriptor.configurable = true; if ("value" in descriptor) descriptor.writable = true; Object.defineProperty(target, descriptor.key, descriptor); } } return function (Constructor, protoProps, staticProps) { if (protoProps) defineProperties(Constructor.prototype, protoProps); if (staticProps) defineProperties(Constructor, staticProps); return Constructor; }; }();

function _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError("Cannot call a class as a function"); } }

var Hoge = function () {
  function Hoge() {
    _classCallCheck(this, Hoge);
  }

  _createClass(Hoge, [{
    key: 'display',
    value: function display() {
      console.log('Hello, world!');
    }
  }]);

  return Hoge;
}();
```
