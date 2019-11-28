[TOC]

## [详细用法]()



## 常用练习 



-i参数打印出服务器回应的 HTTP 标头和网页前10行内容

`curl -i https://www.z.cn`



-I参数向服务器发出 HEAD 请求，然会将服务器返回的 HTTP 标头打印出来。

`curl -I https://www.example.com`



-X 动词，curl默认支持的HTTP动词是GET，使用-X参数可以支持其他动词。

```shell
curl -X POST www.cnblogs.com
curl -X DELETE www.cnblogs.com
```



-d参数用于发送 POST 请求的数据体。

`curl -d'login=emma＆password=123'-X POST https://google.com/login`

或者

`curl -d 'login=emma' -d 'password=123' -X POST  https://google.com/login`



-F参数用来向服务器上传二进制文件。

`curl -F 'file=@photo.png' https://google.com/profile`



-O参数将服务器回应保存成文件，并将 URL 的最后部分当作文件名。

`curl -O https://www.example.com/foo/bar.html`



-v参数输出通信的整个过程，用于调试。可以看到请求头和响应头

`curl -v https://www.example.com`



--trace参数也可以用于调试，还会输出原始的二进制数据。

`curl --trace - https://www.example.com`

如果想要信息保存在一个文件中

`curl --trace output.txt www.cnblogs.com`





-x参数指定 HTTP 请求的代理。

`curl -x socks5://james:cats@myproxy.com:8080 https://www.example.com`



-L参数会让 HTTP 请求跟随服务器的重定向。curl 默认不跟随重定向。


`curl -L -d 'tweet=hi' https://api.twitter.com/tweet`



在http request头信息中，增加一个referer字段，表示你是从哪里过来的。

`curl --referer http://www.yourblog.com http://www.example.com`