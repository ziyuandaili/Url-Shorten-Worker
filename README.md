# Url-Shorten-Worker
A URL Shortener created using Cloudflare Worker

# API

[API Documentation (API文档)](docs/API.md)

# Getting start
### 去Workers KV中创建一个命名空间

Go to Workers KV and create a namespace.

![](docs/kv_create_namespace.png)

### 去Worker的Settings选选项卡中绑定KV Namespace

Bind an instance of a KV Namespace to access its data in a Worker.

![](docs/worker_settings.jpg)

### 其中Variable name填写`LINKS`, KV namespace 选择你刚刚创建的命名空间

Where Variable name should set as `LINKS` and KV namespace is the namespace you just created in the first step.

![](docs/worker_kv_binding.png)

### 添加一个条目Entry，密钥key为password，值value为一个访问URL路径的指定后缀，否则会报404重定向到zyxq.me
例：要访问你的worker域名/url来打开使用页面  如：https://dwz.zyxq.me/url

### 复制本项目中的`index.js`的代码到Cloudflare Worker 

Copy the `index.js` code from this project to Cloudflare Worker. 

### 点击Save and Deploy

Click Save and Deploy

# 后记

你可以通过在你自己的域名下worker页面添加一个路由指向worker的方式来实现比如 dwz.zyxq.me/url 替代 dwz.wqbyc-a1c.workers.dev/url 的效果。
如果你想使用原版，worker里面的脚本使用 https://github.com/xyTom/Url-Shorten-Worker/blob/main/index.js 的内容
