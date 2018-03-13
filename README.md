# RocketMQ源码解读

**RocketMQ**是由阿里团队贡献的apache的开源项目。

* 官网地址: [https://rocketmq.apache.org](https://rocketmq.apache.org)

* 10分钟入门: [http://jm.taobao.org/2017/01/12/rocketmq-quick-start-in-10-minutes/](http://jm.taobao.org/2017/01/12/rocketmq-quick-start-in-10-minutes/)

这篇文章主要讲解rocketmq的源码的结构和功能，便于大家认识mq的结构和了解rocketmq的实现原理，同时也作为个人读源码的一个成果。

源码中用到了很多开源组件（比如netty、序列化等），不需要大家先去了解，大家看到相关章节后如果想深一步了解可以百度或者谷歌（翻墙）。

关于rocketmq的特征和使用等请参考上面两个网址，有比较详细的讲解。

整个文章分为3个部分：

1.  开始部分会简单介绍每个模块都包含哪些功能，形成一个初步认识
2. 最后会根据消息处理每个场景（过程）详细介绍如何实现。
3. 最后会实现几个简单的例子。



最后，文章未写完，入坑需谨慎。



