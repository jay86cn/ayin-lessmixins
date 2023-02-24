[English](./README.en.md) | 简体中文



[Gitee Download](https://gitee.com/ayin86/ayin-lessmixins)

[Github Download](https://github.com/ayin86/ayin-lessmixins)



## 简介

AyinLessMixins 是基于less.js开发的一套样式mixin库 ，本库已开源并上传至npm服务器 [ayin-lessmixins](https://www.npmjs.com/package/ayin-lessmixins)

Less的具体使用方式，请查阅 [less中文文档](https://less.bootcss.com/)

本库最大的作用是，通过简短的代码来调用一些常用的CSS片段。

如 `.bd(@wh)` 实际为`border:1px solid #fff;`

如 `.bgc(@bk)` 实际为 `background-color:#0000;`

如 `.absoluteCenter` 实际为`position: absolute; top:50%; left:50%; transform: translateX(-50%) translateY(-50%) @plus;`

-----

## 使用方式

本mixin库，可以在任意项目中使用

从NPM服务器安装

`npm i ayin-lessmixins --save`

然后通过下面方式全局引入或者单独引入



**vue.config.js中全局引入**

```js
pluginOptions: {
    'style-resources-loader': {
        preProcessor: 'less',
            patterns: [
                path.resolve(__dirname, "./node_modules/ayin-lessmixins/ayin-lessmixins.less")
            ]
    }
},
```



**vite.config.js中全局引入**

```js
css: {
    preprocessorOptions: {
      less: {
        javascriptEnabled: true,
        additionalData:`
          @import "${path.resolve(__dirname, './node_modules/ayin-lessmixins/ayin-lessmixins.less')}";
          `
      }
    }
  },
```

推荐在项目中使用全局引入，这样在所有的组件中均可以方便的调用mixins中的定义，而无需每个文件单独引入。
