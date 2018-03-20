# Java NIO Buffer

NIO Buffers 用于和 NIO Channels进行数据传递. 就如大家所知的一样，读取信息，从channel读数据到buffer，或者从buffer写数据到channel

A buffer is essentially a block of memory into which you can write data, which you can then later read again. This memory block is wrapped in a NIO Buffer object, which provides a set of methods that makes it easier to work with the memory block.

