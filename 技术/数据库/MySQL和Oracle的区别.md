#### MySQL和Oracle的区别

1. Oracle是大型数据库而Mysql是中小型数据库，Oracle市场占有率达40%，Mysql只有20%左右，同时Mysql是开源的而Oracle价格非常高。

​     2. Oracle支持大并发，大访问量，是OLTP最好的工具。

​     3. Oracle与Mysql操作上的一些区别

​         ①主键 Mysql一般使用自动增长类型，在创建表时只要指定表的主键为auto increment，插入记录时，不需要再指定该记录的主键值，Mysql将自动增长；Oracle没有自动增长类型，主键一般使用的序列，插入记录时将序列号的下一个值付给该字段即可；只是ORM框架是只要是native主键生成策略即可。

​         ②单引号的处理 MYSQL里可以用双引号包起字符串，ORACLE里只可以用单引号包起字符串。在插入和修改字符串前必须做单引号的替换：把所有出现的一个单引号替换成两个单引号。

​     4. MySQL的分页关键词limit，Oracle的分页rownum。