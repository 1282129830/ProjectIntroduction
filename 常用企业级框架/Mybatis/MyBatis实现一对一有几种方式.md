#### MyBatis实现一对一有几种方式

有联合查询和嵌套查询,联合查询是几个表联合查询,只查询一次, 通过在resultMap里面配置association(额搜A新)节点配置一对一的类就可以完成；

嵌套查询是先查一个表，根据这个表里面的结果的 外键id，去再另外一个表里面查询数据,也是通过association(额搜A新)配置，但另外一个表的查询通过select属性配置。