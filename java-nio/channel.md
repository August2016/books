# Channel

Java Channel有如下几个特点:

* 一个channel支持同时读写
* channel支持异步读写
* channel总是同buffer配合进行读写

![](/assets/channel-and-buffer.png)

## Channel的实现

Java NIO中比较重要的几种channe实现如下:

* FileChannel
* DatagramChannel
* SocketChannel
* ServerSocketChannel



