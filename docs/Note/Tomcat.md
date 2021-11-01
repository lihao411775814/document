## Tomcat原理

```javascript
- 为什么需要Web.xml？  告诉Web容器，浏览器的url和业务对象进行一个关联，相当于一个注册的作用。
- 为什么需要继承Servlet？ Java本身面向接口语言， 继承了对象可以解决了动态强制转型问题，（新标准面向注解编程），这也是一种设计模式，模板模式
- 为什么要重写doPost/doGet 方法？用于扩展自己的核心业务，用来填空
- HttpRequest和HttpResponse从哪里来？实际是是socket的封装，HTTP协议都是给予TCPIP协议之上的，InputStream 对应 HttpRequest，OutputStream 对应 HttpResponse
- 浏览器输入url如何掉用java方法  ServletMapping Map键值对，键就是url，值就是Servlet对象，通过servlet映射+
```


## 五种IO模型
```javascript
以上tomcat为简单的bio模式，也可以支持nio模式和aio模式。bio为同步的形式，nio为异步形式，aio为服务端主动回调形式（websocket）。但是具体怎么通过后台代码管理请求，让请求走异步或者使用websocket还是不清楚。继续往下可能会关联到Netty，还是先把tomcat完善，可以使用nio和aio，再了解Netty应该会很简单。了解之后可以再完善Tomcat，接下来需要考虑多线程和并发问题。

1. BIO java.io inputStream OutputStream 同步阻塞IO

2. 一定要有线程池处理多端请求（60个线程，其余的进入等待队列）

    解决不了根本问题，线程切换耗费资

3. JDK1.4之前     bio方式

   JDK1.4之后    java.nio.*  解决阻塞问题   Non-Blocking IO 同步非阻塞IO

4. IO是否阻塞，刚Java代码没有直接关系

   IO本质（Java）应用程序和操作系统内核进行数据交互

   （用户空间）程序本身无法直接操作操作系统，由内核空间来操作（操作系统提供给用户空间特权）通过磁盘控制器来读取磁盘文件，读取到内核空间的缓冲器然后返回

5. Input 从外接设备读取数据到应用程序（磁盘，显示器，网卡）

   Output 把数据写入外接设备或者数据库

6. 轮询 不断监听每个客户端的链接，是否需要进一步IO操作（多路复用）

   Selector 多路复用器、Channel多路复用通道（Channel、Server、Client）
```

## Socket 
```java
Socket
```
## JVM 
```java
JVM
```

