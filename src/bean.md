# Spring中bean默认为单例,那么是如何保证线程安全的呢?



## 1.spring中bean的spoce(作用域)

1)singleton:单例，默认作用域。

2)prototype:原型，每次创建一个新对象。

3)request:请求，每次Http请求创建一个新对象，适用于WebApplicationContext环境下。

4)session:会话，同一个会话共享一个实例，不同会话使用不用的实例。

5)global-session:全局会话，所有会话共享一个实例。

spring中默认为1 单例. 而引申出线程安全这个问题的要分别从单例以及原型分别说明:

