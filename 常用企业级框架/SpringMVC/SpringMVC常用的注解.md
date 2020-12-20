#### SpringMVC常用的注解

@RequestMapping：用于处理请求 url 映射的注解，可用于类或方法上。用于类上，则表示类中的所有响应请求的方法都是以该地址作为父路径。

@RequestBody：注解实现接收http请求的json数据，将json转换为java对象。

@ResponseBody：注解实现将conreoller方法返回对象转化为json对象响应给客户。

@RequestParam，将请求的参数绑定到方法中的参数上  @RequestParam(value = "name", required = false) String name

@PathVariable，用于对应restful风格url中的参数   @RequestMapping(value="/happy/{dayid}") findPet(@PathVariable String dayid)