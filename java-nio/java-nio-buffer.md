# Java NIO Buffer

NIO Buffers 用于和 NIO Channels进行数据传递. 就如大家所知的一样，读取信息，从channel读数据到buffer，或者从buffer写数据到channel

NIO Buffer本质上是一块内存区域，可以进行数据写入然后读取。为了简化操作，Java把对这块区域的操作封装到NIO Buffer 对象中。

## 基本使用方法

1. 写数据到buffer
2. 调用buffer.flip\(\)  切换到读取模式
3. 从buffer读数据
4. 调用buffer.clear 或者`buffer.compact()`切换到写入模式

例子:

```
RandomAccessFile aFile = new RandomAccessFile("data/nio-data.txt", "rw");
FileChannel inChannel = aFile.getChannel();

ByteBuffer buf = ByteBuffer.allocate(48);

int bytesRead = inChannel.read(buf); 
while (bytesRead != -1) {
  buf.flip();//设置为读取模式

  while(buf.hasRemaining()){
      System.out.print((char) buf.get());
  }

  buf.clear();//设置为写入模式
  bytesRead = inChannel.read(buf);
}
aFile.close();
```

## Buffer Capacity, Position and Limit

Buffer中有3个属性需要掌握:

* capacity
* position
* limit

capacity是指申请的buffer空间大小，可以认为是固定不变的，但是position和limit会根据读写模式进行变化。

![](/assets/java-nio-buffer-mode.png)

### Capacity

Buffer固定的内存块大小。当数据存储满后   需求清空才能继续存储。

### Position

写入模式下position从0开始，总是对应下一个写入的位置。
读取模式下position对应下一个读取的位置。

### Limit




