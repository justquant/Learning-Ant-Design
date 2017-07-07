为什么要使用dva？dva的作者给出了令人信服的答案。

学习一个新框架的最好方式，就是用它写代码。dva提供了非常好的[新手教程](https://github.com/dvajs/dva/blob/master/docs/GettingStarted.md)。

按照这篇教程，一步步的下来，体验不错。但是开发过程中跳了两个坑。

第一个坑：默认css module支持是被关掉的。需要编辑.roadhogrc，设置 "disableCSSModules": false
第二个坑：我一步小心写错了一个变量名，结果悲剧了。不像typescript，在编译器没有任何错误报告，但是在运行时可以在console看到错误。
```
function delay(timout) { //不小心把timeout 写成 timout，结果不会被触发，但是编译期不报错
  return new Promise(resolve => {
    setTimeout(resolve, timeout);
  })
}
```
第三个坑：作者说keymaster会在保存文件时被自动下载，但是我的环境里没有。只能手工运行

    npm install --save keymaster

## 参考资料

* [dva新手起步](https://github.com/dvajs/dva/blob/master/docs/GettingStarted.md)
* [Why dva](https://github.com/dvajs/dva/issues/1)
* [支付宝前端应用架构的发展](https://github.com/sorrycc/blog/issues/6)
