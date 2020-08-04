## 为开发配置服务，在这里记录看阿波罗代码时的思路

### apollo-biz
这个包放着小应用
grayReleaseRule和灰度相关
repository是Boot的Data接口
entity定义了数据表的格式

### apollo-assembly
server的入口，SpringApplication
引用别的包的代码。
这也是为啥这个包下没多少代码，但在IDEA的Spring面板能看到这么多的Controller，实际上，这些Controller都是别的包的代码（有点啰嗦了我）
![image](https://user-images.githubusercontent.com/24750337/89251374-6db8b680-d649-11ea-9fca-ce9ca9a05027.png)

### apollo-configservice
配置服务，被assembly引用

### apollo-portal
作为client端的SDK集成到别的应用中，依赖 `apollo-openapi`请求接口（HTTP)