# ES6 勉強会スライド (案)

## 案
### ECMAScript って何?
* JavaScript は実装で ECMAScript は規格
  - 基本は ECMAScript の規格に従ってブラウザーメーカーが JavaScript として実装している
* ECMAScript は ECMA International が標準化している
  - ECMA International はもともとは ECMA というヨーロッパの計算機システムの標準化団体
  - ECMA-262 specification として策定されている
* 最新のものは ECMA-262 6th Edition
  - 2015/06/02 に承認された
  - 言語の名前は ECMAScript® 2015 Language Specification と書かれているので、ECMAScript 6 ではなく、ECMAScript 2015 が正しいと思う (どうでもいいけど...)


### JavaScript/ECMAScript の歴史
* 1996: Netscape 2.0 に、JavaScript が搭載される
  - すぐに Microsoft も JScript という似たような実装を IE 3.0 に追加
  - Netscape 社が標準化を目的として ECMA-262 を ECMA Internaltional に提案
* 1997: ECMAScript 1 が承認
* 1998: ECMAScript 2 が承認
  - そんなに変わってないらしい
* 1999: ECMAScript 3 が承認
  - 正規表現・例外ハンドリングなど、今の JavaScript の基礎がある程度揃った
* ????: ECMAScript 4 破棄
  - 欲張り過ぎたらしい...
  - 名前空間・クラス・インターフェイスなど、ActionScript 由来のもの
  - イテレーター・ジェネレーターなどの、JavaScript 1.7 (Firefox 2) 由来のもの
  - オーバーロード・テンプレート (C++ のあれ)などの、新しいもの
  - これらのうちいくつかは ECMAScript 6 の礎になっている
* 2009: ECMAScript 5 が承認
  - ECMAScript 3 をベースにやり直したもの
  - 3 -> 5 だけど、大きな変更はあまりない
  - ストリクトモード・JSON・配列操作メソッド・ゲッターセッターなど
* 2011: ECMAScript 5.1 が承認
  - 正誤表のみ
  - 今時のブラウザーはこれにほぼ対応していて、何も考えずに使える
* 2015: ECMAScript 6 が承認
  - 久々の大規模アップデート
  - ES5.1 に ES4 の機能を激選して取り込んだものがベースっぽい
  - クラス・ジェネレーター・イテレーター・Promise・for/of などなど、盛りだくさん (ES4 ほどじゃないけど...)
  - 昨日の追加だけでなく、標準化を GitHub で行っている
* 2015: ECMAScript 2016 が承認されるはず
  - 先日、追加される仕様が決定したらしい


### ECMAScript 2016
* EMCAScript 6 の次は 7 ではなく、6 のまま 2016 と年号になるっぽい
* 基本的に毎年更新される
* ECMAScript 2015 (ES6) はこの年次リリースのために非常に重要なリリースだった


### JavaScript を取り巻く話
* JavaScript はプロトタイプベースオブジェクト指向言語かつ関数型言語
* JavaScript はいくつかの言語に影響を受けている
  - 文法は Java から
  - 文字列や配列及び正規表現は Perl から
  - クロージャーや environments (?) を Scheme から
  - イベントを HyperTalk から
  - プロトタイプを Self から
  - function を AWK から
* JavaScript は 10 日で書き上げたとのこと
  - もっと前から考えてはいたっぽいけど、すごいね!
  - こんな経緯があって、出来が悪いところと出来のよい所を併せ持つ不思議な言語が生まれたんだと思う
  - 最初は割とおもちゃ扱いされてたみたい
* 世の中がかわる
  - JavaScript がすごい言語だと認識され始める (Douglas Crockford 氏の功績が大きい?)
  - DOM や XMLHttpRequest の導入や、prototype や jQuery の台頭
  - DHTML や Ajax の登場
  - Google Maps によって、実用的なアプリが書けることが証明された
  - JIT コンパイラの導入を始めとした、JavaScript エンジンのパフォーマンス向上
  - JavaScript でアプリを書けるようにするための、HTML5 の登場
  - JavaScript をより良くするための改善 -> ES6


### ECMAScript 6 って使える?
* ECMAScript 6 そのものは、規格化の前からブラウザーメーカーは実装を始めている
  - 実験的に実装してみて、テストしたりもしていた
  - なので、使えるものも結構多い
* [ECMAScript 6 compatibility table](http://kangax.github.io/compat-table/es6/)
  - モダンブラウザーと呼ばれるものはそれなりに対応している
  - IE は...
  - iOS の対応具合を考えると、気にせずに使えるレベルではない
* 現状では Babel や Closure Compiler を使う
  - TypeScript という手も...


### 今覚える必要がある?
* ES5.1 で書かれたコードは、ほぼ ES6 でも動作する
  - 標準化チームは互換性にはかなり気を使っているように見える
  - ES5.1 でしばらく行くのもひとつの手かも?
* ただ、今の JavaScript のベストプラクティス (ES3/5.1 対応) は ES6 世代では大きく変わってきそう
  - ググった時の情報も ES6 で書かれているというのも少しずつ増えそう
  - 新規プロジェクトだと、ES6 を使うかどうかは検討の価値あり
  - ES6 を使わないにしてもつまみぐらいはしたほうがいいと思う

例...

```javascript
// ES5.1 スタイルの型
// どこからどこまでが型宣言かちょっと分かりにくい
var Foo = function () {};

Foo.prototype.hoge = function () {};

Foo.prototype.fuga = function () {};

var Bar = function () {};

Bar.piyo = function () {};
```

ES6 だと...

```javascript
// ES6 class を使った型宣言
// こっちの方が分かりやすい
class Foo {
  hoge() {}
  fuga() {}
}

class Bar {
  piyo() {}
}
```

完全に等価じゃないけど、ES6 の方が分かりやすい。もちろん、ES5.1 で型宣言をわかりやすく書くこともできるけど、流派がいろいろあってめんどくさい...


### トランスパイラーの紹介
* Babel と Closure Compiler が有名
* ToDo Babel の使い方を紹介? (Closure は私が分からない...)


### 機能紹介
* ToDo いろいろあるけど、全部やってると大変なので選ぶ必要あり
* http://kangax.github.io/compat-table/es6/
* `*` がついてるのは必要
* `?` がついているのは私がよく分かってない
* module loader がない気がする

#### proper tail calls
#### *default function parameters
#### *rest parameters
#### *spread (...) operator
#### ?object literal extensions
#### *for..of loops
#### octal and binary literals
#### *template string
#### RegExp "y" and "u" flags
#### ?destructiong, ...
#### ?Unicode code point escapes
#### ?new.target
#### const/let
#### ?block-level function decla
#### *arrow functions
#### *class/super
#### *generators
#### typed array
#### *Map/Set/WeekMap/WeekSet
#### Proxy/Reflect
#### *Promise
#### Symbol
#### ?Object static methods
#### ?function "name" property
#### String static methods/String.prototype methods
#### RegExp.prototype properties
#### Array static methods/Array.prototype methods
#### Number properties/Math methods
#### ... is subclassable
#### ?prorotype of bound function
#### Proxy
#### ?Object static methods accespt primitives
#### ?own property order
#### ?miscellaneous
#### ?non-strict function semantics
#### ?__proto__ in object literals
#### Object.prototype.__proto__
#### String.prototype.HTML methods
#### RegExp.prototype.compile
#### RegExp syntax extensions
#### HTML-style comments


## 資料
* http://speakingjs.com/es5/index.html
* http://www.publickey1.jp/blog/15/javascript20brendan_eich.html
* http://brendaneich.github.io/ModernWeb.tw-2015/
