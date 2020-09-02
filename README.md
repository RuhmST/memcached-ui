你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
## Memcached UI

一个简单实用的Memcached Web客户端。

- 以插件方式支持多种Web框架使用Memached的方式，比如Yii框架会对原始的键值进行处理，存入Memcached的键是一个哈希值，而value只是序列化后的结果。
- 不依赖第三方Memcached客户端库
- 支持Basic Auth身份认证方式

------

插件的实现见代码文件：`middleman/middleman/default.go` 和 `middleman/middleman/yii.go`。

------

界面：

![memcached-ui](https://raw.github.com/youngsterxyf/memcached-ui/master/sample.png)

部署：

1. `go get github.com/youngsterxyf/memcached-ui`
2. `cd $GOPATH/src/github.com/youngsterxyf/memcached-ui`
3. `go build mu.go`
4. `bower install`
5. `cp app.json.example app.json`，并根据需求修改配置信息
6. `nohup ./mu > mu.log 2>&1 &`
7. 访问 http://127.0.0.1:8080
