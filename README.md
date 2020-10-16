## tornado源码解析


### tornado的核心之一：协程，主要是通过asyncio实现的，如果想要更加了解tornado,先要了解asyncio这个包，下面先简单说明一下
* future: 这个类实现协程的基础中的基础，一个iterable类（注意 iterable与iterator的区别），使用yield保存上下文
* task: future的子类（与tornado无关，是asyncio的一个重要概念）,激活future，放到eventloop队列
* eventloop: 事件循环 (epoll\pool\selector: 异步网络通讯机制) 实现
