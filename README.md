# SSMDemo
个人搭建Spring+SpringMVC+MyBatis框架


1、maven引入spring支持
    三步走：a.引入架包（使用pom.xml，spring版本选择spring4，具体根据个人喜好，我这里选用4.3.3.RELEASE）;b.创建配置文件;c.加载配置文件
2、maven引入mybatis支持
    四步走：a.引入mybatis核心包、mybatis插件;b.创建配置文件;c.加载配置文件;d.引入mysql-connector-java.jar和数据源，目前常见的数据源主要有                     druid(alibaba)、c3p0(开源)、dbcp(apache)、proxool(Sourceforge)、jBoss DataSource(JBoss)，druid是目前在功能、性能、扩展方面都是最好             的数据库连接池，数据源选择随意您嘞
            druid能够做什么？(监控数据库访问性能，druid内置功能强大的StatFilter插件，能详细统计SQL的执行性能；SQL执行日志，druid提供不同的                 LogFilter。能够支持Common-Logging、Log4j和JdkLog;扩展JDBC)
      
3、配置文件说明
   spring.xml--- Service层的Bean管理
   spring-mvc.xml--- MVC实现视图、模型、控制分层，主要控制层的Bean管理、视图模式配置等
   spring-mybatis.xml---整合spring和mybatis，主要功能是自动扫描，自动注入，配置数据库等
   gengeratorConfig.xml---利用mybatis-generator自动生成数据库代码的配置文件
   web.xml---web容器配置启动加载的配置文件，设置SpringMVC拦截请求在web.xml文件中元素的加载顺序与它们在 web.xml 文件中的先后顺序无关。加载的顺序是：              context-param->listener -> filter -> servlet，具体详情参照https://blog.csdn.net/oh_mourinho/article/details/51426622
