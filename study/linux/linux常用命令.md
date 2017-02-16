# linux常用命令
## 文件操作
- 批量修改文件后缀
如将当前文件夹及子目录下所有.ts文件修改为.ts.pdf文件
```shell
find ./ -name "*.ts" | xargs -i -t mv ./{} ./{}.pdf
```
- 查看10个常用命令
```shell
history | awk '{cmd[$2]++} END{for(i in cmd) print cmd[i],"......",i}' | sort -rn | head
```
- mongodb连接数据库
```shell
mongo 127.0.0.1/dbname -uuser -ppassword
```
- golang测试命令
```shell
go test -v $PackageName -run ^FuncName$
```
