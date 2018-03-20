# Java NIO Buffer

NIO Buffers 用于和 NIO Channels进行数据传递. 就如大家所知的一样，读取信息，从channel读数据到buffer，或者从buffer写数据到channel

NIO Buffer本质上是一块内存区域，可以进行数据写入然后读取。为了简化操作，Java把对这块区域的操作封装到NIO Buffer 对象中。

## 基本使用方法

1. 写数据到buffer
2. 调用buffer.flip\(\)  切换到读取模式
3. 从buffer读数据
4. 调用buffer.clear 或者`buffer.compact()`切换到写入模式

demo



