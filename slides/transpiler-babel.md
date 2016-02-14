### Babel

Babel だけちょっと使い方を紹介

```javascript
$ npm install -g babel-cli
$ mkdir hoge && cd hoge
$ npm install babel-preset-es2015
$ echo '{ "presets": ["es2015"] }' > .babelrc
$ vim hoge.es6
$ babel hoge.es6 -o hoge.js
```
