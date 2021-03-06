---
layout:     post
title:      shim和polyfill有什么区别?
date:       2016-03-14 18:12:00
summary:    在JavaScript的世界里,有两个词经常被提到,shim和polyfill.它们指的都是什么,又有什么区别?
categories: linux
---

在JavaScript的世界里,有两个词经常被提到,shim和polyfill.它们指的都是什么,又有什么区别?

##### 1.Shim

一个shim是一个库,它将一个新的API引入到一个旧的环境中,而且仅靠旧环境中已有的手段实现.

译者注:有时候也称为shiv,比如https://github.com/aFarkas/html5shiv

##### 2.Polyfill

在2010年10月份的时候,Remy Sharp在博客上发表了一篇关于术语"polyfill"的文章,

一个polyfill是一段代码(或者插件),提供了那些开发者们希望浏览器原生提供支持的功能.

因此,一个polyfill就是一个用在浏览器API上的shim.我们通常的做法是先检查当前浏览器是否支持某个API,如果不支持的话就加载对应的polyfill.然后新旧浏览器就都可以使用这个API了.术语polyfill来自于一个家装产品Polyfilla:

Polyfilla是一个英国产品,在美国称之为Spackling Paste(译者注:刮墙的,在中国称为腻子).记住这一点就行:把旧的浏览器想象成为一面有了裂缝的墙.这些polyfill会帮助我们把这面墙的裂缝抹平,还我们一个更好的光滑的墙壁(浏览器)


##### 3.例子

1. Paul Irish发布过一个Polyfill的总结页面“HTML5 Cross Browser Polyfills”.

2. es5-shim是一个shim,而不是polyfill.因为它是在ECMAScript 3的引擎上实现了ECMAScript 5的新特性,而且在Node.js上和在浏览器上有完全相同的表现(译者注:作者的意思是因为它能在Node.js上使用,不光浏览器上,所以它不是polyfill).

译者注:按照作者的解释,"polyfill是专门兼容浏览器API的shim,shim的范围更大些".照我看来,这个解释并不正确.但对这样两个连母语是英语的人们也很难理解的词,我也无能为力了.希望真正理解的朋友给讲下.

至于翻译,我觉的就不需要翻译了(类似bug这样的词).如果担心读者不懂,可以用脚注的方式说明一下.或者直接翻译成"兼容代码",再或"模拟该API的代码"等短语也可以吧.
