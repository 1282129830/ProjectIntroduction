#### 如何解决token注销问题

JWT的缺陷是token生成后无法修改，因此无法让token失效。只能采用其它方案来弥补，基本思路如下：

 1）适当减短token有效期，让token尽快失效
 2）删除客户端cookie​
 3）服务端对失效token进行标记，形成黑名单，虽然有违无状态特性，但是因为token有效期短，因此标记时间也比较短。服务器压力会比较小