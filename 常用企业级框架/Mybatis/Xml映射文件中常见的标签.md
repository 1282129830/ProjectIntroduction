#### Xml映射文件中常见的标签

> <resultMap>

手动封装标签，用于实体类和数据库字段不一致时进行手动封装

><parameterMap>（没用过）

表示将查询结果集中列值的类型一一映射到Java对象属性的类型上

> <resultType>

表示直接将查询结果列值类型自动对应到java对象属性类型上

> <sql>

SQL片段，复用

> <include>

引入SQL片段

> <selectKey>

不支持自增主键生成策略的标签