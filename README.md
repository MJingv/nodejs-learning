# [《Node.js 包教不包会》](https://github.com/alsotang/node-lessons) 学习笔记
## QuickStart

### Development

```bash
$ npm i
$ npm run dev
$ open http://localhost:7001/
```

### Deploy

```bash
$ npm start
$ npm stop
```


***

端口的作用：通过端口来区分出同一电脑内不同应用或者进程，从而实现一条物理网线(通过分组交换技术-比如internet)同

通常我们熟悉的url定义成这个样子
`<scheme>://<user>:<password>@<host>:<port>/<url-path>`

用过ftp的估计能体会这么长的，网页上很少带auth信息，所以就精简成这样:
`<scheme>://<host>:<port>/<url-path>`


***

lesson3 写爬虫
==

1. 安装  superagent 与 cheerio  `npm i superagent/cheerio  `
1. 用 superagent 去抓取 https://cnodejs.org/ 的内容
1. cheerio.load拿到html像jquery拼数据


lesson4 eventproxy
===

foreach async 问题
        
        ok i know why... Using Babel will transform async/await to generator function and using forEach means that each iteration has an individual generator function, which has nothing to do with the others. so they will be executed independently and has no context of next() with others. Actually, a simple for() loop also works because the iterations are also in one single generator function

forEach 实现不了 await
for 循环 + await 并发为 1
Promise.all + array.map 并发为 Infinity



