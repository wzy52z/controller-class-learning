# controller-class-learning
初学者写着当笔记的，如错误严重还请谅解，如能指出感激不尽
## Controller 类的作用
Controller类是MVC的经典架构中负责处理来自客户端的请求，通过解析请求中的参数后，调用Service层的方法，最后将结果返回给客户端。
在Springboot里面，一般Controller方法会包含注解@RestController 和@RequestMapping来映射HTTP请求到具体方法上。
## @RestController注解

## @RequestMapping注解
@RestController是一个复合注解，结合了@Controller和@ResponseBody注解。它用于标注一个类是一个Spring MVC的控制器，并且该控制器中的所有方法都默认会把返回值转换成JSON或者XML格式的响应体（基于内容协商机制）。
使用@RestController后，所有方法的返回值默认都直接*写入HTTP响应体*，而无需在每个方法上都添加@ResponseBody注解。
