# 该代码来自GitHub
```
@RequestMapping("/admin/menu")
@Controller
public class MenuController {
  	@RequestMapping(value="/edit",method=RequestMethod.GET)
	public String eidt(Model model,@RequestParam(name="id",required=true)Long id){
		List<Menu> findAll = menuService.findAll();
		model.addAttribute("title","菜单列表");
		model.addAttribute("topMenus",MenuUtil.getTopMenus(findAll));
		model.addAttribute("secondMenus",MenuUtil.getSecondMenus(findAll));
		model.addAttribute("menu",menuService.find(id));
		return "admin/menu/edit";
	}
}
```
 ## @Controller注解
  @Controller是一个用于标识Spring MVC控制器类的注解，表示该类中的方法是处理HTTP请求的。它本身并不提供自动将返回值转换为HTTP响应体的功能。
## 映射概念
  映射是指将HTTP请求的URL路径与处理这些请求的控制器方法关联起来的过程。
  
1. 代码第一段指明这个HTTP请求表示在类上，其基础路径在admin/menu下
2. 
3.









  
