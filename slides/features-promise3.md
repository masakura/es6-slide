### Promise

Promise のある優しい世界

```javascript
File.loadJson('config.json')
  .then(function (config) {
    return File.loadJson(config.appConfigPath);
  })
  .then(function (appConfig) {
    return Image.load(config.titleImagePath);
  })
  .then(function (image) {
    // 成功時
  })
  .catch(function (error) {
    // エラー処理
  });
```
