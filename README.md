# controller-class-learning
初学者写着当笔记的，如错误严重还请谅解，如能指出感激不尽
## Controller 类的作用
Controller类是MVC的经典架构中负责处理来自客户端的请求，通过解析请求中的参数后，调用Service层的方法，最后将结果返回给客户端。
在Springboot里面，一般Controller方法会包含注解@RestController 和@RequestMapping来映射HTTP请求到具体方法上。
## @RestController注解

## @RequestMapping注解
@RestController是一个复合注解，结合了@Controller和@ResponseBody注解。它用于标注一个类是一个Spring MVC的控制器，并且该控制器中的所有方法都默认会把返回值转换成JSON或者XML格式的响应体（基于内容协商机制）。

使用@RestController后，所有方法的返回值默认都直接**写入HTTP响应体**，而无需在每个方法上都添加@ResponseBody注解。
## @RequestMapping注解
用于将**HTTP请求映射到控制器的方法或类上**。它可以应用于类和方法上，提供更灵活和详细的URL映射规则。
路径映射：可以使用路径模式指定请求路径。
HTTP方法：可以限制映射到特定的HTTP方法（**GET, POST, PUT, DELETE**等）。

- 类级别：标注在类上，定义基础路径。
- 方法级别：标注在方法上，定义相对路径。
- 
Spring 还提供了许多专用的映射注解，这些注解是@RequestMapping的简化形式，并且更具语义性，比如：

   -  @GetMapping：用于映射HTTP GET请求。
   -  @PostMapping：用于映射HTTP POST请求。
   -  @PutMapping：用于映射HTTP PUT请求。
   -  @DeleteMapping：用于映射HTTP DELETE请求。
## RESTful API特点
1.资源标识（Resource Identification）：
        每个资源有唯一的URI，例如http://api.example.com/users 标识用户资源。

2.HTTP动词（HTTP Verbs）：
        GET：获取资源。例如，GET /users/1获取ID为1的用户信息。
        POST：创建资源。例如，POST /users添加新的用户。
        PUT：更新资源。例如，PUT /users/1更新ID为1的用户信息。
        DELETE：删除资源。例如，DELETE /users/1删除ID为1的用户。

3.表示（Representations）：
        资源可以有多种表示形式，例如JSON、XML等。客户端可以指定请求表示形式的首选项，例如使用HTTP头部Accept来请求JSON格式：Accept: application/json。

4.无状态交互（Stateless Interactions）：
        每个请求都是独立的，不依赖于上一请求。

5.自描述消息（Self-descriptive Messages）：
        HTTP请求和响应消息包括足够的信息以使其自描述，例如状态代码（HTTP 状态码）、头部信息（Headers）等。
## 什么是REST架构


    1.资源（Resources）：
        在REST中，所有的内容都被视为资源。资源可以是文档、图像、数据对象、服务等。
        每个资源都有一个唯一的URI（Uniform Resource Identifier）。

    2.无状态（Statelessness）：
        每个请求都包含所有的信息，因此服务器不需要在请求之间保留任何客户端状态。
        这使得服务更加简单和可靠，因为不需要在服务器端保存状态信息。

    3.客户端-服务器（Client-Server）：
        客户端和服务器职责分离。客户端负责用户界面和用户交互，服务器负责数据存储和业务逻辑处理。
        这种分离允许两者独立开发和扩展。

    4.统一接口（Uniform Interface）：
        REST使用通用的接口来简化和分离客户端和服务器，这些接口基于HTTP动词（GET、POST、PUT、DELETE等）。
        典型的约定包括：GET用于获取资源，POST用于创建资源，PUT用于更新资源，DELETE用于删除资源。

    5.可缓存（Cacheable）：
        服务器响应必须明示自身是否是可缓存的，以改善客户端的性能。

    6.分层系统（Layered System）：
        通过在中间层添加代理服务器、负载均衡器等，可以提高系统的可伸缩性和安全性。

