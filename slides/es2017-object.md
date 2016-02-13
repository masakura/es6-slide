### Object.values/Object.entries

`Object.keys` はあったけど、`values` や `entries` はなかったのね...

```javascript
var obj = {a: 1, b: 2, c: 3}

// ['a', 'b', 'c']
Object.keys(obj);

// [1, 2, 3]
Object.values(obj);

// [['a', 1], ['b', 2], ['c', 3]]
Object.entries(obj);
```
