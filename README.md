你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
The Destiny Chat Back-End
===========

The chat back-end for destiny.gg, written in Go, based on Golem (http://github.com/trevex/golem) 

Licensed under the Apache License, Version 2.0 

http://www.apache.org/licenses/LICENSE-2.0.html

This is my first not-so-tiny Go project, so if there is anything that could be improved, please do tell.

=== How to Build:

`go get` each package listed in main.go

fix the redis library to this specific commit with:

    cd $GOPATH/src/github.com/vmihailenco/redis
    
    git checkout 28a881e7240a23c43ceee5a9e0c9a56da2da3db3

redis/v2 changed the function argument style for creating a new tcp client

this is the parent commit that we we depend on:

https://github.com/vmihailenco/redis/commit/28a881e7240a23c43ceee5a9e0c9a56da2da3db3

this is the commit that broke our code:

https://github.com/vmihailenco/redis/commit/ce34e39219f360baedf597e03f0a9c938bce59dc

this whole thing won't be an issue any more when we vendor the dependencies with something like godep

