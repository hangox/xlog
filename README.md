# xlog
Log Helper in Android
----

XLog 是一个帮助Android开发打印的调试信息的工具类
1. 自动填充TAG(格式为类名+函数名+方法名+行号)
2. 无需考虑print string为null的事情
3. 一个方法取消所有打印

平常使用 Log
```java
    Log.i(TAG,print string);
```
我们需要构建TAG，并且还要防止 print string 为null 这种情况

在xlog,不需要考虑这些
```java
    XLog.i(print object);
```
不需要tag ，自动默认的tag就是当前调用的类和行数，打印的是object.toString()内容，不需要把基本类型弄成
string，自动判断是否为空，为空时，会打印报空的问题。

```java
    XLog.setLogState(false);
```
关闭所有的debug
也可以单独关闭每一个
```java
    XLog.allowI = false;
```

#Thanks for 
[xutils][1] 一个开源框架，xLog参考了其中LogUtils大部分的思路,改进了流程


  [1]: https://github.com/wyouflf/xUtils
