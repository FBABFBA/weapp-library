## 在线借书平台

<img src="https://imageslr.github.io/weapp-library/assets/img/weapp_code.f16279a1.png" width=250 />

**如果你觉得这个仓库有用，请点一个Star支持一下我，谢谢！**  
**如果对哪部分代码有疑问或者需要我讲一下设计和开发的整体理念/部分细节，可以开一个Issue。欢迎大家与我交流。**

> **欢迎关注本项目使用 Taro 重构后的版本**：[taro-library](https://github.com/imageslr/taro-library)，仅包含三个示例页面，非常简单。面向人群主要是 Taro/React/Redux 的初学者，目的是提供一个简单的实践项目，帮助理解 Taro 与 Redux 的配合方式与 Taro 的基本使用。本项目还提供了一个快速搭建本地 mock 服务的解决方案。

### Mock 数据
本项目目前仅提供小程序的开源代码，暂无对应后端服务。Mock 数据来自 [Easy Mock](https://www.easy-mock.com/mock/5aacc9a1d3f6bd35dfb4be65/)，API 文档使用 [Swagger](https://app.swaggerhub.com/apis/imageslr/weapp/1.0.1)。

EasyMock 的证书已经到期，因此需要在开发者工具-详情中勾选“不校验合法域名、web-view（业务域名）、TLS 版本以及 HTTPS 证书”。

EasyMock 现在不太稳定，所以我把 Mock 数据导出了一份，见 [mocks](./mocks) 文件夹。大家可以尝试本地部署 [Easy Mock](https://github.com/easy-mock/easy-mock/blob/dev/README.zh-CN.md)，导入 mock 数据，然后修改 `api/request.js` 中的 `BASE_URL`。

### 文档
[点击查看](https://imageslr.github.io/weapp-library)

### UI
![ui](./ui.png)

### 组件化
在线借书平台小程序——我的——组件展示

![组件展示](./component.png)

### 文件结构

```
.
├── apis                  // 网络请求封装
├── app.js
├── app.json
├── app.wxss
├── component-demos       // 组件展示
├── components            // 可复用组件
│   ├── async-button      // 异步按钮
│   ├── async-switch      // 异步切换器
│   ├── collapse          // 可折叠容器
│   ├── load-more         // 加载更多
│   ├── no-data           // 暂无数据
│   ├── panel             // 带导航标题的面板
│   ├── popup             // 底部弹出层
│   ├── rate              // 可评半星的评分组件
│   ├── search-bar        // 带遮罩的搜索框
│   ├── send-code         // 发送验证码按钮
│   ├── spinner           // 加载中动画
│   ├── sticky            // 固定页头
│   ├── sticky-2          // 固定页头的另一种实现
│   ├── tab-bar           // 标签页
│   ├── toast             // 弹出提示
│   └── toptip            // 顶部提示
├── images                // 图标
├── package.json
├── pages                 // 页面，子页面在父页面的children文件夹中
│ └─components            // 与业务相关的特殊组件
├── project.config.json
├── styles                // 样式
├── templates             // 模板
│   ├── library-list      // 图书馆列表
│   ├── page-status-indicator // 页面加载状态，带有一个“重新加载”按钮
│   └── showcase          // 图书项目
└── utils                 // 辅助模块
    ├── biz-helper.wxs    // 业务相关辅助函数，用于wxml中
    ├── constant.js       // 业务常量
    ├── constant.wxs      // 业务常量，用于wxml中
    ├── es6-promise.js    // Promise语法支持
    ├── event.js          // 全局事件
    ├── permission.js     // 登录鉴权
    ├── promise-polyfill.js // Promise.finally()语法
    ├── promisify.js      // 微信小程序API Promise化
    ├── qrcode.js         // 二维码生成
    ├── tip.js            // 使用帮助
    ├── utils.js          // 辅助函数
    ├── validator.js      // 正则校验器
    └── fundebug.js       // 错误监控
```

### 代码规范
遵循 [JavaScript Standard Style](https://standardjs.com/readme-zhcn.html)

### 声明
Demo 仅作学习使用, 转载请注明出处
