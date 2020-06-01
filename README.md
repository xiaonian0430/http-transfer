# HTTP-Transfer


`A`可以访问`B`，`B`可以访问`C`，但是`A`不能访问`C`，那么这时候，如果`A`想要访问`C`，那么只能通过`B`来进行请求。

`HTTP-Transfer`不是一个翻墙程序，只是一个简陋的`HTTP`请求转发服务。

目前只支持`Get`请求，为了[`ShareKnow`](https://sk.shareknow.top)的采集功能而开发

## 打包

打包成 Linux 命令
```
bee pack -be GOOS=linux 
```

打包成 Windows 命令 
```
bee pack -be GOOS=windows

打包成 Mac 命令 
```
bee pack -be GOOS=darwin
```

## 使用

启动服务，监听 8101 端口
```
tar zxvf http-transfer.tar.gz
cd http-transfer
chmod 777 http-transfer
./http-transfer 8101
```

例如：请求百度的 logo

```
http://localhost:8101/https://www.baidu.com/img/superlogo_c4d7df0a003d3db9b65e9ef0fe6da1ec.png
```