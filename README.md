
#  [![NPM version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Dependency Status][daviddm-image]][daviddm-url]  [![Coveralls Status][coveralls-image]][coveralls-url] [![Beerpay](https://beerpay.io/node-weixin/node-weixin-express/badge.svg?style=flat-square)](https://beerpay.io/node-weixin/node-weixin-express)


## 功能说明
  node-weixin-express是一个基于nodejs为基础，以expressjs作为首选http服务器框架的微信公共账号服务器。
  他旨在降低开发微信公共账号时的门槛，节约开发时间。
  

## 主要功能与计划

  1. 可以直接通过一个命令运行微信公共账号服务
  2. 基本的微信功能：
    - 验证服务器
    - OAuth 验证API
    - 微信支付API
    - 消息接口API
  3. 可以任意基于express的框架沟通协作(基本完成)
  4. 模块化机制采用Unix开发哲学：KISS
  5. 建立一个可以方便安装数据库，并且将配置信息存放在数据库里的机制(计划中)
  6. 通过express可以无需任何开发就可以自己建设一个功能全面的微信服务器(计划中)
  

## 重要子模块
  1. [node-weixin-api](https://github.com/node-weixin/node-weixin-api):提供所有基础的微信api
  2. [node-weixin-router](https://github.com/node-weixin/node-weixin-router):提供所有的基于web框架的默认路由与回调机制
  3. [node-weixin-session](https://github.com/node-weixin/node-weixin-session):提供所有基于session的数据保存机制
  4. [node-weixin-settings](https://github.com/node-weixin/node-weixin-settings):提供所有基于appId的数据保存机制


## 问题、反馈与帮助

* 论坛交流  
  [node-weixin交流论坛](http://forum.node-weixin.com/)

* 官方网站  
  [node-weixin](http://www.node-weixin.com/) 用于快速检索更新, 帮助，导航等
  
* 示例网址 
  [demo网址](http://express.ngrok.t1bao.com/) 输入appId，然后匹配成功就可以实现四种服务器功能

* 关注公共账号了解最新动态  
  ![](http://res.cloudinary.com/dawjytvkn/image/upload/v1464858605/qrcode_for_gh_6f66da401fef_430_b1rr96.jpg)



注:
 [node-weixin-express](https://github.com/node-weixin/node-weixin-express)是基于node-weixin-*的服务器端参考实现。

 [node-weixin-api](https://github.com/node-weixin/node-weixin-api)是基于node-weixin-*的API接口SDK。

 它们都是由下列子项目组合而成:

 1. [node-weixin-config](https://github.com/node-weixin/node-weixin-config)
    用于微信配置信息的校验

 2. [node-weixin-auth](https://github.com/node-weixin/node-weixin-auth)
    用于与微信服务器握手检验

 3. [node-weixin-util](https://github.com/node-weixin/node-weixin-util)
    一些常用的微信请求，加密，解密，检验的功能与处理

 4. [node-weixin-request](https://github.com/node-weixin/node-weixin-request)
    微信的各类服务的HTTP请求的抽象集合

 5. [node-weixin-oauth](https://github.com/node-weixin/node-weixin-oauth)
    微信OAuth相关的操作

 6. [node-weixin-pay](https://github.com/node-weixin/node-weixin-pay)
    微信支付的服务器接口

 7. [node-weixin-jssdk](https://github.com/node-weixin/node-weixin-jssdk)
    微信JSSDK相关的服务器接口

 8. [node-weixin-menu](https://github.com/node-weixin/node-weixin-menu)
    微信菜单相关的操作与命令
    
 9. [node-weixin-user](https://github.com/node-weixin/node-weixin-user)
    微信用户API
    
10. [node-weixin-media](https://github.com/node-weixin/node-weixin-media)
    微信多媒体API

11. [node-weixin-link](https://github.com/node-weixin/node-weixin-link)
    微信推广(二维码,URL)API
 
12. [node-weixin-message](https://github.com/node-weixin/node-weixin-message)
    微信消息API

## 安装

```sh
$ npm install --g node-weixin-express
```

> 注意： 使用0.2.x版本时确保npm 版本大于 3


## 使用说明

安装后在命令行会多出一个命令:

```sh
weixin
```
注意：这里的命令名是weixin，不是node-weixin-express

###查看命令

```sh
$ weixin --help
```

不需要再写代码，可以直接通过命令执行。

端口port默认是3333,需要配置HTTP代理才能更好的工作
  >如果没有代理服务器，请将port指定为80，以防微信验证无法通过。


###参数说明：

```sh
--port port         //服务器侦听的端口
```

###运行说明

普通命令运行

```sh
weixin --port port
```

作为永久服务器运行
```sh
forever start $(which weixin) --port port
```
## 已经支持服务器类型

1. 作为微信验证服务器

2. 作为oauth服务器

3. 作为JSSDK服务器

4. 作为支付服务器

详情参考示例网站：
http://express.ngrok.t1bao.com/


## 交流论坛


## License

MIT © [node-weixin](http://www.node-weixin.com)


[npm-image]: https://badge.fury.io/js/node-weixin-express.svg
[npm-url]: https://npmjs.org/package/node-weixin-express
[travis-image]: https://travis-ci.org/node-weixin/node-weixin-express.svg?branch=master
[travis-url]: https://travis-ci.org/node-weixin/node-weixin-express
[daviddm-image]: https://david-dm.org/node-weixin/node-weixin-express.svg?theme=shields.io
[daviddm-url]: https://david-dm.org/node-weixin/node-weixin-express
[coveralls-image]: https://coveralls.io/repos/node-weixin/node-weixin-express/badge.svg?branch=master&service=github
[coveralls-url]: https://coveralls.io/github/node-weixin/node-weixin-express?branch=master
