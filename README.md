# my-roadmap

我的开发者 线路图谱

[原版](https://github.com/kamranahmedse/developer-roadmap)

[繁体版](https://github.com/goodjack/developer-roadmap-chinese)

[developer-roadmaps-all-in-one-place](https://medium.com/level-up-web/developer-roadmaps-all-in-one-place-75c0402db0e0)

[REACT](https://github.com/adam-golab/react-developer-roadmap)


(+) 表示原版没有,但我认为很重要的

<!-- MarkdownTOC autolink="true" -->

- [基础](#%E5%9F%BA%E7%A1%80)
    - [git](#git)
    - [ssh](#ssh)
    - [http/https APIs](#httphttps-apis)
    - [基本命令行](#%E5%9F%BA%E6%9C%AC%E5%91%BD%E4%BB%A4%E8%A1%8C)
        - [sed](#sed)
    - [编辑器\(+\)](#%E7%BC%96%E8%BE%91%E5%99%A8)
    - [编译原理\(+\)](#%E7%BC%96%E8%AF%91%E5%8E%9F%E7%90%86)
    - [学会专研问题](#%E5%AD%A6%E4%BC%9A%E4%B8%93%E7%A0%94%E9%97%AE%E9%A2%98)
    - [数据结构和算法](#%E6%95%B0%E6%8D%AE%E7%BB%93%E6%9E%84%E5%92%8C%E7%AE%97%E6%B3%95)
    - [字节编码](#%E5%AD%97%E8%8A%82%E7%BC%96%E7%A0%81)
    - [设计模式](#%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F)
    - [Github](#github)
- [前端](#%E5%89%8D%E7%AB%AF)
    - [HTML](#html)
    - [css](#css)
    - [javascript](#javascript)
    - [JQuery-可选](#jquery-%E5%8F%AF%E9%80%89)
    - [设计入门\(+\)](#%E8%AE%BE%E8%AE%A1%E5%85%A5%E9%97%A8)
    - [制作响应式交互网页](#%E5%88%B6%E4%BD%9C%E5%93%8D%E5%BA%94%E5%BC%8F%E4%BA%A4%E4%BA%92%E7%BD%91%E9%A1%B5)
    - [在Github找一些项目](#%E5%9C%A8github%E6%89%BE%E4%B8%80%E4%BA%9B%E9%A1%B9%E7%9B%AE)
    - [给自己点个赞,因为你可以接活了](#%E7%BB%99%E8%87%AA%E5%B7%B1%E7%82%B9%E4%B8%AA%E8%B5%9E%E5%9B%A0%E4%B8%BA%E4%BD%A0%E5%8F%AF%E4%BB%A5%E6%8E%A5%E6%B4%BB%E4%BA%86)
    - [package manager 套件管理 npm yarn, 选一个就可以](#package-manager-%E5%A5%97%E4%BB%B6%E7%AE%A1%E7%90%86-npm-yarn-%E9%80%89%E4%B8%80%E4%B8%AA%E5%B0%B1%E5%8F%AF%E4%BB%A5)
    - [试用一些包](#%E8%AF%95%E7%94%A8%E4%B8%80%E4%BA%9B%E5%8C%85)
    - [css 预处理](#css-%E9%A2%84%E5%A4%84%E7%90%86)
    - [css框架](#css%E6%A1%86%E6%9E%B6)
    - [css 架构,了解他们的差异](#css-%E6%9E%B6%E6%9E%84%E4%BA%86%E8%A7%A3%E4%BB%96%E4%BB%AC%E7%9A%84%E5%B7%AE%E5%BC%82)
    - [构建工具\(build\)](#%E6%9E%84%E5%BB%BA%E5%B7%A5%E5%85%B7build)
    - [写些东西并在 github 和 npm 上发布](#%E5%86%99%E4%BA%9B%E4%B8%9C%E8%A5%BF%E5%B9%B6%E5%9C%A8-github-%E5%92%8C-npm-%E4%B8%8A%E5%8F%91%E5%B8%83)
    - [框架](#%E6%A1%86%E6%9E%B6)
        - [react](#react)
        - [vue vuex](#vue-vuex)
        - [angular](#angular)
    - [设计模式](#%E8%AE%BE%E8%AE%A1%E6%A8%A1%E5%BC%8F-1)
    - [练习](#%E7%BB%83%E4%B9%A0)
    - [测试](#%E6%B5%8B%E8%AF%95)
    - [Progressive Web App 渐进式应用](#progressive-web-app-%E6%B8%90%E8%BF%9B%E5%BC%8F%E5%BA%94%E7%94%A8)
    - [静态检查](#%E9%9D%99%E6%80%81%E6%A3%80%E6%9F%A5)
    - [服务端渲染](#%E6%9C%8D%E5%8A%A1%E7%AB%AF%E6%B8%B2%E6%9F%93)
    - [其它](#%E5%85%B6%E5%AE%83)
- [移动端\(+\)](#%E7%A7%BB%E5%8A%A8%E7%AB%AF)
    - [语言](#%E8%AF%AD%E8%A8%80)
    - [H5](#h5)
    - [框架/组件](#%E6%A1%86%E6%9E%B6%E7%BB%84%E4%BB%B6)
    - [发布](#%E5%8F%91%E5%B8%83)
- [后端](#%E5%90%8E%E7%AB%AF)
    - [选一个语言](#%E9%80%89%E4%B8%80%E4%B8%AA%E8%AF%AD%E8%A8%80)
    - [设计文档\(+\)](#%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3)
    - [命令行应用](#%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%BA%94%E7%94%A8)
    - [pm 套件管理](#pm-%E5%A5%97%E4%BB%B6%E7%AE%A1%E7%90%86)
    - [编码规范和最佳实践](#%E7%BC%96%E7%A0%81%E8%A7%84%E8%8C%83%E5%92%8C%E6%9C%80%E4%BD%B3%E5%AE%9E%E8%B7%B5)
    - [制作一些库给别人使用](#%E5%88%B6%E4%BD%9C%E4%B8%80%E4%BA%9B%E5%BA%93%E7%BB%99%E5%88%AB%E4%BA%BA%E4%BD%BF%E7%94%A8)
    - [测试](#%E6%B5%8B%E8%AF%95-1)
    - [测试实践](#%E6%B5%8B%E8%AF%95%E5%AE%9E%E8%B7%B5)
    - [Relational Database 关系型数据库](#relational-database-%E5%85%B3%E7%B3%BB%E5%9E%8B%E6%95%B0%E6%8D%AE%E5%BA%93)
    - [实践](#%E5%AE%9E%E8%B7%B5)
    - [框架](#%E6%A1%86%E6%9E%B6-1)
    - [实践](#%E5%AE%9E%E8%B7%B5-1)
    - [Nosql](#nosql)
    - [缓存](#%E7%BC%93%E5%AD%98)
    - [RESTFUL api](#restful-api)
    - [认证 authentication 授权 authorization](#%E8%AE%A4%E8%AF%81-authentication-%E6%8E%88%E6%9D%83-authorization)
    - [消息中间件 message broker](#%E6%B6%88%E6%81%AF%E4%B8%AD%E9%97%B4%E4%BB%B6-message-broker)
    - [搜索引擎](#%E6%90%9C%E7%B4%A2%E5%BC%95%E6%93%8E)
    - [docker](#docker)
    - [web 服务器](#web-%E6%9C%8D%E5%8A%A1%E5%99%A8)
    - [RPC RMI](#rpc-rmi)
        - [Dubbo RMI](#dubbo-rmi)
    - [web socket](#web-socket)
    - [graphQL](#graphql)
    - [图形数据库 Graph Databse](#%E5%9B%BE%E5%BD%A2%E6%95%B0%E6%8D%AE%E5%BA%93-graph-databse)
    - [其它](#%E5%85%B6%E5%AE%83-1)
- [运维](#%E8%BF%90%E7%BB%B4)
    - [语言](#%E8%AF%AD%E8%A8%80-1)
    - [操作系统](#%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F)
    - [服务器](#%E6%9C%8D%E5%8A%A1%E5%99%A8)
    - [网络与安全](#%E7%BD%91%E7%BB%9C%E4%B8%8E%E5%AE%89%E5%85%A8)
    - [基础服务](#%E5%9F%BA%E7%A1%80%E6%9C%8D%E5%8A%A1)
    - [基础构建编程](#%E5%9F%BA%E7%A1%80%E6%9E%84%E5%BB%BA%E7%BC%96%E7%A8%8B)
    - [CI/CD 工具](#cicd-%E5%B7%A5%E5%85%B7)
    - [监控应用和基础组件](#%E7%9B%91%E6%8E%A7%E5%BA%94%E7%94%A8%E5%92%8C%E5%9F%BA%E7%A1%80%E7%BB%84%E4%BB%B6)
    - [云服务](#%E4%BA%91%E6%9C%8D%E5%8A%A1)

<!-- /MarkdownTOC -->

## 基础

### [git](/base/git/git.md)
### ssh
### http/https APIs
### 基本命令行
#### [sed](/base/shell/sed.md)
### 编辑器(+)
### 编译原理(+)
### 学会专研问题
### 数据结构和算法
### 字节编码
### 设计模式
### Github

## 前端

### HTML

+ 基础知识 & semantic HTML(语义化HTML)
+ 将页面划分为区段 & 如何正确配置DOM
+ 制作甚少5个HTML页面,主要关注结构
+ 先不用管他是否漂亮

### css

+ 基础css
+ 学会使用网格和弹性盒子(Flexbox)
+ 媒体查询(Media Queries)和响应式网页
    + [媒介查询](https://blog.csdn.net/zhouziyu2011/article/details/61917081)
+ 给上步中你做的网页配一下样式
+ [Debug(+)](./css/debug.md)

### javascript
基本语法 & 基础结构
操作DOM
基本概念 提升hoisting/事件冒泡event bubbling, 原型prototype
AJAX (XHR)
ES6+ 新特性及组件化JS

HTML, CSS, and JavaScript
JavaScript: Getting Started
JavaScript Fundamentals
JavaScript Objects and Prototypes
Practical Design Patterns in JavaScript
Advanced Techniques in JavaScript and jQuery
JavaScript Best Practices
Rapid ES6 Training

### JQuery-可选

### 设计入门(+)

### 制作响应式交互网页

### 在Github找一些项目
+ 改改他们的demo页: 优化UI,改成响应式或是改进设计
+ 看下有什么 issues 你可以解决
+ 学习最佳实践,并重构代码
+ 学习更多的git知识
### 给自己点个赞,因为你可以接活了

### package manager 套件管理 npm yarn, 选一个就可以
### 试用一些包
在你上面的页面里加入一些包
如: 加个 toast 插件,当用户点一下,给他弹个toast消息
做个登录表单,用户验证插件来验证一下
试一下更新不用的插件版本
### css 预处理
预处理给css提供更多功能,看下他都给提供些什么功能
sass(推荐)
postcss
less
sytlus
### css框架
bootstrap
materialize css
bulma
### css 架构,了解他们的差异
BEM(推荐)
OOCSS
SMACSS
SUITCSS
Atomic
### 构建工具(build)
npm scripts
    任务执行器(task runners)
gulp

ESLint
JSlint
JSHint
JSCS

Webpack
    应用程序/函数
Rollup
    函数库
Parcel

### 写些东西并在 github 和 npm 上发布

### 框架

#### react

react有自己的 [roadmap](https://github.com/adam-golab/react-developer-roadmap)

[中文](https://github.com/adam-golab/react-developer-roadmap/blob/master/README-CN.md)

#### vue vuex

[VUE大型SPA项目管理](https://github.com/PerseveranceZ/vue-develop-template/blob/master/docs/tutorial.md)

#### angular

    rx.js 不用angular也可以别的地方使用

    ngrx

### 设计模式

[MVVM最佳解读和实践](https://zhuanlan.zhihu.com/p/38270598)|done

### 练习
性能测量及优化
interactivity time
page speed index
lighthouse分数
### 测试
Jest
Mocha
Protractor
karma
Enzyme
### Progressive Web App 渐进式应用
service worker
### 静态检查
TypeScript
Flow

### 服务端渲染

react next.js after.js
angular jniversal
vue.js nuxt.js

### 其它

Canvas
HTML5 APIS
SVG
Sourcemaps
函数式编程
TC39

## 移动端(+)

原版没有覆盖移动端,很移动端很重要
### 语言
java/kotlin
ooc/
native: react/Wexx

### H5
### 框架/组件
### 发布

## 后端
### 选一个语言
脚本语言
    python
    ruby
    php
    node.js/typescript 推荐

Node.js: Getting Started
Learning To Program - Part 1: Getting Started
NPM Playbook
Building a JavaScript Development Environment
Introduction to Node.js
Building Web Applications with Node.js and Express 4.0 (UPDATE)
RESTful Web Services with Node.js and Express
Node.js Testing Strategies
Node Application Patterns
Advanced Node.js

函数式语言
elixir
scala
erlang
clojure
haskell
其它
java
.net
golang
rust
### 设计文档(+)
[how-to-write-a-good-software-design-document](https://medium.freecodecamp.org/how-to-write-a-good-software-design-document-66fcf019569c)
why
    A design doc — also known as a technical spec — is a description of how you plan to solve a problem.
    设计文档用于描述你解决问题的方案
What
    Title and People(author)
    Overview It should be 3 paragraphs max.
    Context
        A description of the problem at hand,
        why this project is necessary,
        what people need to know to assess this project, 
        and how it fits into the technical strategy, product strategy, or the team’s quarterly goals.
    Goals and Non-Goals
    Milestones
    Current Solution
        user story 
    Proposed(计划) Solution
    Alternative Solutions
    Monitoring and Alerting(监控与报警)
    Cross-Team Impact
        How will this increase on call(待命) and dev-ops burden(负担)?
        How much money will it cost?
        Does it cause any latency regression to the system?
        Does it expose any security vulnerabilities?
        What are some negative consequences and side effects?
        How might the support team communicate this to the customers?
    Discussion
    Detailed Scoping and Timeline
How to write it
    Write as simply as possible
        Simple words
        Short sentences
        Bulleted lists and/or numbered lists
        Concrete examples, like “User Alice connects her bank account, then …”
    Add lots of charts and diagrams
        Pro Tip: remember to add a link to the editable version of the diagram under the screenshot, so you can easily update it later when things inevitably change
    Include numbers
    Try to be funny
    Do the Skeptic(怀疑者) Test
    Do the Vacation Test(假期测试)
### 命令行应用
+ ls
+ 爬虫
+ 找个每天都做的任务,自动之

### pm 套件管理
node.js npm yarn
ruby gems
python pip

### 编码规范和最佳实践
PHP-FIG PSRs
安全相关

### 制作一些库给别人使用
制作一些库
或帮助开源项目改些issue

### 测试
unit test
integration test

node.js mocha chai sinon mockery ava jasmine

### 测试实践
覆盖率
### Relational Database 关系型数据库
oracle mysql mariadb
postgresql
mssql
### 实践
注册/登录
CRUD
BLOG

测试 index  storage engine analyze the queries

### 框架
hapi.js express.js

### 实践
使用框架来写

### Nosql
why?
有什么不同
mongodb
rethinkDB
Cassandra
couchbase

### 缓存
redis memcached

### RESTFUL api

### 认证 authentication 授权 authorization
OAUTH
Basic Authentication
Token Authentication
JWT
OpenID
### 消息中间件 message broker
robbitmq (推荐)
kafka
### 搜索引擎
elasticSearch
solr
sphinx

### docker
### web 服务器
apache
nginx
caddy
MS IIS
### RPC RMI
#### Dubbo RMI

（Remote Method Invocation） 远程方法调用

[如何快速开发一个 Dubbo 应用](https://mp.weixin.qq.com/s/bcwIMIir2RHPbQQr8HgTOQ)

### web socket
### graphQL
### 图形数据库 Graph Databse
### 其它
性能分析 Profiling
静态分析 Static Analysis
领域驱动设计 DDD
简单对象存贮 SOAP

## 运维

### 语言
Pyhone
ruby node.js
go
rust
c/c++
### 操作系统

进程 process
线程 thread
套接字 socket
I/O 管理
虚拟化
内存/存贮
### 服务器
ubuntu
linux/unix/windows
终端
bash
vim/nano/powerShell/Emacs
gcc/make
系统性能 nmon iostat sar vmstat
文字处理 awk sed grep sort uniq cat cut echo fmt tr nl egrep fgrep wc
监控 ps top htop atop lsof
网络 nmap tcpdump ping mtr traceroute airmon airodump dig iptables
其它  strace dtrace systemtap uname df history

### 网络与安全

DNS
OSI model
HTTP
HTTPS
FTP
SSL/TLS
### 基础服务
反向代理 缓存服务 正向代理 负载均衡 防火墙
web服务器 IIS Apache Nginx Tomcat caddy

### 基础构建编程
容器 docker rkt LX
配置管理 Ansible Salt Chef Puppet
基础设施供给 Terraform cloud Formation
kubernetes
    [和我一步步部署 kubernetes 集群](https://github.com/opsnull/follow-me-install-kubernetes-cluster/blob/master/README.md)
### CI/CD 工具
Jenkins
Travis CI
Teamcit
Drone
Cirle CI
### 监控应用和基础组件
基础组件监控 nagios icinga datadog zabbix monit
应用监控 AppDynamics newrelic
日志管理 ELK Stack Graylog splunk patertrail

### 云服务
google cloud
azure
digital ocean
heroku









