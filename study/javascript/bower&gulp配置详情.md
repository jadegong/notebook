# 前端自动构建工具配置
## dependencies & devdependencies
依赖包的版本：
安装特殊的angular作为依赖，又想让其他的依赖angular的包指向改依赖：
```shell
bower install --save angular=angularjs-ie8-build#1.4.7
```

```json
"angular": "angularjs-ie8-build#1.4.7",
"angular": "1.4.7" //版本固定为1.4.7（精确）
```
##overrides
当依赖包没有指定主要的文件（需要使用）时，可以通过配置overrides来实现。例如bootstrap：
```json
"overrides": {
    "bootstrap": {
        "main": [
            "dist/css/bootstrap.css",
            "dist/js/bootstrap.js",
            "./fonts/*"
       ]
   }
}
```
