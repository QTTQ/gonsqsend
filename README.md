# gonsqsend
nsq 生产端




# 介绍
topic的作用
topic的作用就和收发快递选哪个快递一样，你选择顺丰，选择圆通。收快件(消费消息)的时候都用这个topic，应该没人收顺丰快递跑到圆通的网点吧。

channel的作用
消息复制
channel是用大作用的，主要体现在消息复制上。你想实现一条消息两个业务都收到。这里做法就需要用到channel，在同一样topic下面创建两个channel，ch1和ch2。生产者发一条hello nsq，这时候两个业务都会收到hello nsq。(下面给代码验证这个结论)
默认用法
如不需消息复制，就一个topic，一个channel就完事。
