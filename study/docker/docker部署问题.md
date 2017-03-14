# docker部署问题
## docker配置问题
详情如下表：
<table>
    <tr>
        <th>问题描述</th>
        <th>想法or思路</th>
    </tr>
    <tr>
        <td>Nginx配置(HTTPS以及多站点)是否需要手写然后导入？</td>
        <td>需要手写然后docker导入</td>
    </tr>
    <tr>
        <td>宿主机一个端口是否可以对应多个docker容器端口？</td>
        <td>不能，应该需要在docker内的Nginx配置分发</td>
    </tr>
    <tr>
        <td>将项目部署为一个容器还是多个容器相互通信？</td>
        <td>一个容器Dockerfile会比较复杂；多个容器之间通信问题。</td>
    </tr>
    <tr>
        <td>``VOLUME /data``中/data的具体含义？</td>
        <td>``docker run -v /dir:/data ...`` 中-v参数表示将宿主/dir目录挂载到容器的/data上--[具体参考](http://dockone.io/article/128)</td>
    </tr>
</table>