
# mpvue-imooc-book-init

> 第一步，基于mpvue-quickstart模板创建新项目

````vue2
npm install -g cnpm --registry=https://registry.npm.taobao.org【淘宝镜像】

cnpm install -g @vue/cli          [安装脚手架]

vue init mpvue/mpvue-quickstart my-project
````
> 第二步，安装依赖和运行
````vue2
cd my-project

npm install

npm run dev
````
> 安装scss依赖

````vue3
"sass-loader": "^6.0.7",

cnpm i sass-loader@6.x --save-dev
````

淘宝领取优惠券地址： [https://myphp.vip](https://myphp.vip) 

## Build Setup

``` bash
# 初始化项目
vue init mpvue/mpvue-quickstart myproject
cd myproject

# 安装依赖
yarn

# 开发时构建
npm dev

# 打包构建
npm build

# 指定平台的开发时构建(微信、百度、头条、支付宝)
npm dev:wx
npm dev:swan
npm dev:tt
npm dev:my

# 指定平台的打包构建
npm build:wx
npm build:swan
npm build:tt
npm build:my

# 生成 bundle 分析报告
npm run build --report
```


