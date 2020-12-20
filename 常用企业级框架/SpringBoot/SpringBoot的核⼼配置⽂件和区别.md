#### SpringBoot的核⼼配置⽂件和区别

Spring Boot 的核心配置文件是 application 和 bootstrap 配置文件。 

>配置文件的区别

application 配置文件这个容易理解，主要用于 Spring Boot 项目的自动化配置。 

bootstrap 配置文件有以下几个应用场景： 

使用 Spring Cloud Config 配置中心时，这时需要在 bootstrap 配置文件中添加连接到配置中心的配置属性来加载外部配置中心的配置信息。

一些固定的不能被覆盖的属性。

一些加密/解密的场景。