# 2.开发流程

博客参考：

#### [https://blog.csdn.net/bieleyang/article/details/77862042](https://blog.csdn.net/bieleyang/article/details/77862042)

#### 具体流程如下：

1.设计数据库

2.编写实体类：定义对象属性

3.写Mapper.xml（Mybatis），其中定义你的功能，对应要对数据库进行的那些操作，比如 insert、selectAll、selectByKey、delete、update等。

4.写Mapper.java，将Mapper.xml中的操作按照id映射成Java函数。

5.写Service接口，然后写Service.java实现接口，为控制层提供服务，接受控制层的参数，完成相应的功能，并返回给控制层。

6.写Controller.java，连接页面请求和服务层，获取页面请求的参数，通过自动装配，映射不同的URL到相应的处理函数，并获取参数，对参数进行处理，之后传给服务层。

7.写JSP页面调用，请求哪些参数，需要获取什么数据。

大致文件编写流程如下：

DataBase ===&gt; Entity ===&gt; Mapper.xml ===&gt; Mapper.Java ===&gt; （Service接口--&gt;）Service.java ===&gt; Controller.java ===&gt; Jsp.

而SSM框架运行流程如下：

![](http://img.blog.csdn.net/20151118190949363?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

