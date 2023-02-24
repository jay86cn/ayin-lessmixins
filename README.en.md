English | [简体中文](./README.md)

Translated by deepl

[Gitee Download](https://gitee.com/ayin86/ayin-lessmixins)

[Github Download](https://github.com/ayin86/ayin-lessmixins)



## Introduction

AyinLessMixins is a set of style mixin libraries based on less.js , this library has been open sourced and uploaded to the npm server [ayin-lessmixins](https://www.npmjs.com/package/ayin-lessmixins)

For details of how to use Less, please check [less documentation](https://less.bootcss.com/)

The most useful thing about this library is that it calls some common CSS snippets via short code.

For example `.bd(@wh)` is actually `border:1px solid #fff;`

e.g. `.bgc(@bk)` actually `background-color:#0000;`

e.g. `.absoluteCenter` is actually `position: absolute; top:50%; left:50%; transform: translateX(-50%) translateY(-50%) @plus;`

-----

## Usage

This mixin library, which can be used in any project

Install from the NPM server

`npm i ayin-lessmixins --save`

Then introduce it globally or separately by doing the following



**Global introduction in vue.config.js**

```js
pluginOptions: {
    'style-resources-loader': {
        preProcessor: 'less',
            patterns: [
                path.resolve(__dirname, ". /node_modules/ayin-lessmixins/ayin-lessmixins.less")
            ]
    }
},
```



**Global introduction in  vite.config.js**

``` js
css: {
    preprocessorOptions: {
      less: {
        javascriptEnabled: true,
        additionalData:`
          @import "${path.resolve(__dirname, '. /node_modules/ayin-lessmixins/ayin-lessmixins.less')}";
          `
      }
    }
  },
```

It is recommended to use global introductions in your project, so that the definitions in mixins can be easily called in all components without each file being introduced separately.
