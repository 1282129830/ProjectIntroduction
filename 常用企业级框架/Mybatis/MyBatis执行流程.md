#### MyBatis执行流程

> 加载配置文件并初始化(SqlSession)

配置文件来源于两个地方，一个是配置文件(主配置文件conf.xml,mapper文件*.xml)，一个是java代码中的注释，将sql的配置信息加载成为一个mappedstatement对象，存储在内存之中（包括传入参数的映射配置，结果映射配置，执行的sql语句）。

> 接收调用请求

调用mybatis提供的api，传入的参数为sql的id（有namespase和具体sql的id组成）和sql语句的参数对象，mybatis将调用请求交给请求处理层。

> 处理请求

根据sql的id找到对应的mappedstatament对象。

根据传入参数解析mappedstatement对象，得到最终要执行的sql。

获取数据库连接，执行sql，得到执行结果

Mappedstatement对象中的结果映射对执行结果进行转换处理，并得到最终的处理结果。

释放连接资源

> 返回处理结果