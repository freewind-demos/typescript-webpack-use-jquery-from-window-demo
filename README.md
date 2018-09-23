TypeScript Webpack Use JQuery From Window Demo
==============================================

如何让typescript编译之后的js代码不包含`jquery`代码，而是使用浏览器通过`<script src=...`导入的jquery?

关键点就是`webpack.config.js`中需要有：

```
externals: ['jquery']
```

```
npm install
npm run dev
```

![demo](./images/demo.jpg)

注意看生成的`bundle.js`文件，只有几K。如果包含了jquery，应该有快2M。
