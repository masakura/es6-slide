### Promise

コールバック地獄...

```javascript
File.loadJson('config.json', function (config) {
  File.loadJson(config.appConfigPath, function (appConfig) {
    Image.load(appConfig.titleImagePath, function (image) {
      // 成功時
    }, function (error) {
      // エラー処理
    });
  }, function (error) {
    // エラー処理
  });
}, function (error) {
  // エラー処理
});
```
