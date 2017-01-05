# 常用正则表达式
## 邮箱
本表达式来源：[emailregex](emailregex.com)
```javascript
var email = '^(([^<>()\\[\\]\\\\.,;:\\s@"]+(\\.[^<>()\\[\\]\\\\.,;:\\s@"]+)*)|(".+"))@((\\[[0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3}\\.[0-9]{1,3}])|(([a-zA-Z\\-0-9]+\\.)+[a-zA-Z]{2,}))$';
```

## IP地址
ip地址表达式：根据  [StackOverflow](http://stackoverflow.com/questions/26119630/html5-pattern-for-validating-ip-with-mask)  改编
```javascript
var ipPattern = '(((25[0-5])|(2[0-4]\\d)|(1\\d\\d)|([1-9]?\\d))\\.){3}((25[0-5])|(2[0-4]\\d)|(1\\d\\d)|([1-9]?\\d))';
```
