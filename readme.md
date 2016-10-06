# EasyPropertiesUtils 项目简介

---------------


EasyPropertiesUtils 是 EasyCommons 项目组下的 properties 文件操作组件。

> [EasyCommons](https://github.com/ushelp/EasyCommons "EasyCommons") 一个针对Java开发领域提供通用开发组件的项目。旨在为Java项目开发领域并不完善的一些方面，提供一些组件级的解决方案。
> 该项目有多个子项目，会不断收集相关组件，也欢迎有新的组件加入。



EasyPropertiesUtils is EasyCommons project group properties file operations component. 

>  [EasyCommons](https://github.com/ushelp/EasyCommons "EasyCommons") is a development component to provide a common field for Java development projects. Java is designed to develop programs in the field of some aspects of the project is not perfect, some component-level solutions.
>  The project has multiple sub-projects, will continue to collect related components, also welcomed the new components added.



## 中文

Java提供的 `java.util.Properties` 不仅仅在设计上存在问题，并且功能异常简陋，一般除了读，在写上不具备实用性（会导致文件原格式和注释丢失）。在维护或写properties文件时必须自行实现写方案。

EasyPropertiesUtils 核心：

1. **EasyProperties**： 用来代替 `java.util.Properties` 的 properties 文件类， 扩展了 `java.util.Properties`，提供了内容合并（`merge`: 增, 删, 改）和修改（`modify`: 增,改）功能，修改属性时不影响原格式；支持 `#comment` 注释，`#newLine` 添加换行。<br/>
 **适合场景**：任何需要对 properties 文件进行读写操作的场景，不影响文件原格式。 

2. **EasyPropertiesUtils**： 直接修改 Properties 文件的工具类，提供原格式写功能，包括保留注释，支持内容合并（`merge`: 增, 删, 改）和修改（`modify`: 增,改）；并提供基于正则的文件内容匹配删除；支持 `#comment` 注释，`#newLine` 添加换行。<br/>
 **适合场景**：对 properties 文件进行修改操作，又不影响原格式的情况。


[EasyPropertiesUtils API - 中文](doc/API-zh.md "EasyPropertiesUtils API")

[官方主页](http://www.easyproject.cn/easycommons/zh-cn/index.jsp '官方主页')

[留言评论](http://www.easyproject.cn/easycommons/zh-cn/index.jsp#donation '留言评论')

如果您有更好意见，建议或想法，请联系我。


## English

The `Java.util.Properties` not only the existence of problems in the design and function of abnormal primitive, usually in addition to reading and writing not practical in the (original file format and can lead to loss of the comment). When maintenance or write properties file must be self-fulfilling to write programs.

**EasyPropertiesUtils core：**

Properties file with projects under EasyCommons tools. Comprising the following components:

1. **EasyProperties**: Instead of `java.util.Properties`, extends java.util.Properties, provides content merge (`merge`: add, delete, change) and modifications (`modify`: add, change ) function, modify the property does not affect the original format; support `#comment` comment, `#newLine` add newline.

 **Scene** : properties require any scene file read and write operations, without affecting the original file format.

2. **EasyPropertiesUtils**: Properties file directly modify the tools to provide the original format write functions, including a comment, support is incorporated (`merge`: add, delete, change) and modifications (`modify`: add, change); and suport use regular matches deleted file content; support `#comment` comment, `#newLine` add newline.

 **Scene** : properties files to modify the operation, without prejudice to the original format.

[EasyPropertiesUtils API - English](doc/API-en.md "EasyPropertiesUtils API")

[The official home page](http://www.easyproject.cn/easycommons/en/index.jsp 'The official home page')

[Comments](http://www.easyproject.cn/easycommons/en/index.jsp#donation 'Comments')

If you have more comments, suggestions or ideas, please contact me.


## Maven
```XML
<!-- EasyPropertiesUtils -->
<dependency>
	<groupId>cn.easyproject</groupId>
	<artifactId>easycommons-properties</artifactId>
	<version>2.0.0-RELEASE</version>
</dependency>
```

## End

[官方主页](http://www.easyproject.cn/easycommons/zh-cn/index.jsp '官方主页')

[留言评论](http://www.easyproject.cn/easycommons/zh-cn/index.jsp#donation '留言评论')

[The official home page](http://www.easyproject.cn/easycommons/en/index.jsp The official home page')

[Comments](http://www.easyproject.cn/easycommons/en/index.jsp#donation 'Comments')

如果您有更好意见，建议或想法，请联系我。

If you have more comments, suggestions or ideas, please contact me.



Email：<inthinkcolor@gmail.com>

[http://www.easyproject.cn](http://www.easyproject.cn "EasyProject Home")


**支付宝钱包扫一扫捐助：**

我们相信，每个人的点滴贡献，都将是推动产生更多、更好免费开源产品的一大步。

**感谢慷慨捐助，以支持服务器运行和鼓励更多社区成员。**

<img alt="支付宝钱包扫一扫捐助" src="http://www.easyproject.cn/images/s.png"  title="支付宝钱包扫一扫捐助"  height="256" width="256"></img>



We believe that the contribution of each bit by bit, will be driven to produce more and better free and open source products a big step.

**Thank you donation to support the server running and encourage more community members.**

[![PayPal](http://www.easyproject.cn/images/paypaldonation5.jpg)](https://www.paypal.me/easyproject/10 "Make payments with PayPal - it's fast, free and secure!")



