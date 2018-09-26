# FlyGo_HellowWord
maven HelloWord学习

# 创建工程

1、右键`新建` -> 选择`New`选项 -> `Project...`选项。

![新建Maven项目图1](https://www.flygo520.com/uploads/maven/images/m_9ad636ecd2b6d58cd5a817e16816f725_r.png)

2、选择`Maven Project`选项 -> `下一步`

![新建Maven项目图2](https://www.flygo520.com/uploads/maven/images/m_88713029c882847f11a003aaabd18638_r.png)

3、勾选`Create a simple project  (skip archetype selection)`-> 选择`下一步`

![新建Maven项目图3](https://www.flygo520.com/uploads/maven/images/m_42e6d7c19a19a58cad4de1b8f053018a_r.png)

>[info] 勾选了`Create a simple project  (skip archetype selection)`，创建简洁的空Maven项目，不带任何模板。如果没有勾选，会弹出选择Maven相关的模板项目选择。

没有勾选`Create a simple project  (skip archetype selection)`，出现选择模板Maven项目界面。
![模板Maven项目](https://www.flygo520.com/uploads/maven/images/m_e1bba382dbac46dab465d9928b637681_r.png)

4、Maven项目相关信息

![新建Maven项目图4](https://www.flygo520.com/uploads/maven/images/m_c36ebeacf02730cabe03f458421ff9d3_r.png)

- 所有的 POM 文件要项目元素必须有三个必填字段: `groupId`，`artifactId`，`version`
- 在库中的项目符号是：`groupId:artifactId:version`
- pom.xml 的根元素是 `project`，它有三个主要的子节点
- Packaging 分为 `jar`、`war` 和 `pom`
>[info] jar : 为Java项目
war : 为web项目
pom： 为逻辑父项目

关键元素说明

|<center>元素节点</center>|<center>节点说明</center>|
|:----    |:---|
|Group Id |公司名.公司网址倒写。例如：`com.flygo520`  |
|Artifact Id |项目名。例如：`demo`  |
|Version |版本号。例如：`1.0`  |
| Packaging|项目打包类型。例如：`jar`、`war` 和 `pom`  |
| Name|项目名称  |
| Description|项目描述 |

# Maven 目录结构 (Jar项目)

![Jar项目 Maven目录结构](https://www.flygo520.com/uploads/maven/images/m_5398e0176283c9c4a4ab79a33ff562fa_r.png)

目录结构

|<center>目录名称</center>|<center>目录说明</center>|
|:----    |:---|
|src/main/java |真实目录的快捷目录,写java代码  |
|src/main/resources |快捷目录，存放配置文件. 虽然看见resources但是里面所有配置文件最终会被编辑放入到classes类路径. |
|src/test/java |写测试java代码 |
|src/text/resources |测试的配置文件夹 |
|spom.xml |maven的配置文件，当前项目所依赖的其他项目或jar或插件等 |

# pom.xml 引入依赖Jar包

在项目工程的pom.xml配置文件引入依赖的jar包。
以引入 spring-core 为例，在中央仓库 `http://mvnrepository.com` 搜索需要引入的包选择一个版本，添加相关的依赖配置到`pom.xml`文件中即可。

![搜索出来的各个版本的Jar](https://www.flygo520.com/uploads/maven/images/m_53b93749f49eb908de57167a04604e58_r.png)

![选择的版本配置信息](https://www.flygo520.com/uploads/maven/images/m_27a059f6cd2d59f378e477f8998edea3_r.png)

```bash
<dependencies>
	<!-- https://mvnrepository.com/artifact/org.springframework/spring-core -->
	<dependency>
	<groupId>org.springframework</groupId>
	<artifactId>spring-core</artifactId>
	<version>5.1.0.RELEASE</version>
	</dependency>
</dependencies>
```
添加完配置依赖配置文件后，Maven自动从中央仓库下载Jar包，缓存到本地仓库。

![工程添加的依赖包](https://www.flygo520.com/uploads/maven/images/m_1446233c01d4647267a050a42229e586_r.png)

# 演示Demo源码地址

https://github.com/jxaufang168/FlyGo_HellowWord

