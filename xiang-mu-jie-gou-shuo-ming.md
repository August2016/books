# REMOTING

remoting被所有模块依赖，主要提供了以下功能：

1. netty服务器
2. netty客户端
3. 序列化
4. 异常
5. 远程工具类

![](/assets/remoting-1.png)

remoting包下包含4的package:

1. annotation: 允许空/非空注解
2. common: 通用工具类
3. exception: 远程访问异常
4. netty: netty server及netty 客户端
5. protocol: 接口数据接口及序列化

接口：

1. ChannelEventListener: 通道事件监听接口（监听远程接口的情况） 
2. CommandCustomHeader: 客户端指令header检查接口
3. InvokeCallback: 远程调用后回调接口
4. RemotingClient: 客户端接口
5. RemotingServer: 服务端接口
6. RPCHook: 远程调用钩子（切面）接口，请求前和返回后处理



