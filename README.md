Akari.biliScript
================

> あかり 【名】 
>
> 1. 灯
> 2. 希望，光明

Akari.biliScript是一个针对BiliPlayer的开源弹幕艺术辅助框架。这个辅助框架根据设计允许进度条跳转，并会将内容自动匹配到播放器窗口上。

原repo[akaza-akari/Akari.biliScript](https://github.com/akaza-akari/Akari.biliScript)

我Fork这个repo的可能目的：

>1. 创建一个较为平易近人的引导教程文档。
>2. 针对于自身的制作需求，对一些相关组件进行扩展。(没错，在毕业前，我还想开坑，预定于10月)

什么是弹幕艺术？
----

[百度百科的解释](http://baike.baidu.com/view/8938455.htm)

如何使用
----
下载`BuildOutput/Akari.min.biliScript`

把它的内容发送到第0秒（或者你认为的起始时刻）就行了。

然后在其他需要使用此辅助框架的弹幕代码开头，进行以下声明。

```js
// Fetch a global reference for Akari
var Akari = Global._get( "__akari" );
Akari.stop();
// Import namespaces by extending this closure
Akari.Utilities.Factory.extend( this, Akari.Utilities );
Factory.extend( this, Akari.Display );
Factory.extend( this, Akari.Animation );
```

简单例程
----
访问`Samples/`


Akari.biliScript并不能……
------------------------

* 把它贴上你的弹幕艺术就变厉害了。
  
  这是根本不可能的，尽管加上那个全屏、宽屏的匹配功能挺容易，但仅仅是匹配屏幕没有什么意义，人们更在意你的内容。

* 在你准备往屏幕上扔一坨.lrc的时候助你一臂之力。

  尽管这事真能干，这根本就是多此一举。Akari.biliScript就其设计而言是用于展示非常复杂的弹幕艺术，更理想的是用于覆盖整个画面的纯色屏视频上。如果你就拿它做一些简单的东西，那些声明式的合成和层描述还有表达式这些玩意都会来碍你的事——尽管做一些复杂的东西的时候这些都很有用。这些琐事用内建的指令API去解决就行了。

* 用老版本播放器的那个不安全的漏洞来加速执行，让它和AS一样快——我刚才说了AS？

  还是不了，Akari.biliScript并不也并不打算且不会使用这些东西来加快执行。保持清白既可以提升生产力，也能让你的作品活的久一点。

* 一起来玩弹幕游戏吧！

  Akari.biliScript是做来展现预先设计好的内容的，压根就没打算支持交互性元素。一旦你把你的MainComposition放上去，修改它只能给你添麻烦。

* 一个用来炒你的版本的某个无聊的冷饭的快速工具。

  你可以，不过你给我个面子吧，还是别了。

参与
----

你完全可以对Akari.*这些命名空间做出你自己的改进，或者写你自己的扩展命名空间，送一个新的样例或者教程，什么都行！不过最好：

1. 保持Akari.*命名空间的通用性。

   这些命名空间应该只包括最基本的，最通用的东西。那些复杂的或者稀奇古怪的特效之类的东西应该被放在它们自己，或者你的个人命名空间里。这是为了让一个“基本”的版本干净利落而且短一点（就算是现在它也够长的了！）

2. 保持连续性。

   多写点注释没坏处：这样使用者和其他的参与者就知道你的脚本在干什么了，这样用起来或者改进起来也更容易。另外这也使得脚本看起来更具整体性，也更美观，权当是普及一下文化知识吧。

许可
-------

Akari.biliScript根据GNU GPLv3进行许可。详细的请读Akari.Template.biliScript吧。

