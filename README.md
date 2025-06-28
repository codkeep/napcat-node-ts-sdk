# node-napcat-ts

基于 https://github.com/huankong-team/node-napcat-ts 仓库的修改，增加支持 CommonJS 方式调用，兼容NestJS等框架的使用

[![npm version](https://badge.fury.io/js/your-package-name.svg)](https://www.npmjs.com/package/your-package-name)
[![GitHub license](https://img.shields.io/github/license/yourusername/my-package)](https://github.com/yourusername/my-package)

## 😎 介绍

针对 `napcat` 开发的 `SDK`

本 SDK 中所有 `api` 基于 `napcat-v4.5.23`

## 📦 安装

```bash
npm install node-napcat-ts
```

## 🚀 使用

### CommonJS (推荐)

```javascript
const { NCWebsocket, Structs } = require('node-napcat-ts');

// 创建WebSocket连接
const ws = new NCWebsocket({
  protocol: 'ws',
  host: '127.0.0.1',
  port: 8080,
  accessToken: 'your-access-token'
});

// 连接
await ws.connect();

// 发送消息
const message = [
  Structs.text('Hello '),
  Structs.at(123456),
  Structs.text('!')
];

await ws.send_private_msg({
  user_id: 123456,
  message: message
});
```

### ESM

```javascript
import { NCWebsocket, Structs } from 'node-napcat-ts';

// 使用方式同上
```

## 📚 文档

- [napcat 文档](https://napneko.github.io/) <= 遇到问题先看我
- [node-napcat-ts 文档](https://node-napcat-ts.huankong.top) <= 使用前先看我
- [go-cqhttp 文档](https://docs.go-cqhttp.org/)
- [onebot11 文档](https://github.com/botuniverse/onebot-11/)

## 🎉 更新日志

[跳转](./CHANGELOG.md)

## ⭐ 星星

[![Stargazers over time](https://starchart.cc/codkeep/node-napcat-ts.svg)](https://starchart.cc/codkeep/node-napcat-ts)
