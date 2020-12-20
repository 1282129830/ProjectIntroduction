#### JWT和Shiro区别

Shiro是一套权限管理框架.包括认证,授权等,在使用时候写响应的接口就行,已经把底层的处理都写好了,而JWT是一种生成token的机制,所有的逻辑还需要自己编写。

当我们要把服务器做成无状态时（即服务器端不会保存session）,这里我们就可以用到[JWT](https://blog.csdn.net/qq_40081976/article/details/79046825)。Shiro就是基于session保持回话，我们可以将session换成token的形式。