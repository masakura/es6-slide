### Object の強化

オブジェクトの合成が簡単に!

```javascript
var a = {
  name: 'abc',
};

Object.assign(a, {foo: 15, bar: 10});

// a = {
//   name: 'abc',
//   foo: 15,
//   bar: 10
// };
```

* [_.extend](http://underscorejs.org/#extend)/[jQuery.extend](https://api.jquery.com/jquery.extend/)/[angular.extend](https://docs.angularjs.org/api/ng/function/angular.extend)
