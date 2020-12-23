# swagger2无侵入jar包源码
原swagger2配置弊端是需要在启动类上添加注解、在上下文中配置swagger配置类、配置类中还需要拷贝别人的代码然后改成自己的代码，所以上述步骤在本项目中可以完全忽略，只需要有本项目打包成的jar包，添加依赖即可。

## 1.在pom.xml 添加maven依赖

这里需要说明一下,因为我还没有上传中央存储库,所以,直接依赖是找不到的,所以,你就clone到本地, 然后进入我的这个项目根目录`mvn clean install` 一下,输入下面这个依赖就可以了

```xml
<dependency>
    <groupId>com.vip</groupId>
    <artifactId>vip-swagger</artifactId>
    <version>1.0.0</version>
</dependency>
```

## 2.配置

在这里我给大家提供了很多自由化的配置了,当然你也可以不用配置,因为所有的选项都是可选的

注意:如果你要进行自定义配置的话,需要默认加上前缀:`swagger.`来配置属性,给个demo吧,配置的地方是`application.properties`或者`application.yml`,参数那么多,我就不一个个来了哈,可以自己配置来看看效果,其实,我都没配置完过,哈哈,要是有问题的话,请大家及时指出,以便即时更正.

```xml
swagger.title = Swagger API Demo
swagger.description = This is swagger api describle demo
swagger.version = 1.1.1
```

**配置参数**

1. title(可选)  接口的标题,具体就不多说了吧,可以自己试着玩,默认是`Swagger Restful API`
2. description(可选) 接口的描述,默认是`This is a swagger api desc`
3. version(可选) 接口的版本,默认是`1.0.0`
4. groupName(可选) 接口所属的组,默认没有,当然,你可以自己写下试试
5. basePackage(可选) 扫描的包路径,默认没有,扫描下面的所有的@Controller和@RequestMapping的映射
6. termsOfService(可选) 服务条款的地址,默认没有
7. contactName(可选)  联系人,默认没有
8. contactUrl(可选) 联系的url,默认没有
9. contactEmail(可选)  联系的email,默认没有
10. licenseName(可选) 证书名,默认没有
11. licenseUrl(可选) 证书的url,默认没有

## 3.启动和使用

启动的话,和前面没什么区别,使用也是和前面的那种方法是一样的,打开浏览器访问 

`http://localhost:端口号/swagger-ui.html`

