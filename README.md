# G-mall
#### 商城实战项目

1、创建parent和api包；

parent中的pom.xml说明：dependencyManagement里只是声明依赖，并不实现引入，因此子项目需要显示的声明需要用的依赖。如果不在子项目中声明依赖，是不会从父项目中继承下来的；只有在子项目中写了该依赖项，并且没有指定具体版本，才会从父项目中继承该项，并且version和scope都读取自父pom;另外如果子项目中指定了版本号，那么会使用子项目中指定的jar版本。

2、抽取utils工程；

```
1 项目中的通用框架，是所有应用工程需要引入的包
例如：springboot、common-langs、common-beanutils

2 基于soa的架构理念，项目分为web前端controller(webUtil)
Jsp、thymeleaf、cookie工具类
加入commonUtil

3 基于soa的架构理念，项目分为web后端service(serviceUtil)
Mybatis、mysql、redis
加入commonUtil
```



