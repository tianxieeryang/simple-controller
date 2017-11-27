# simple-controller


1.	搭建 Java Web 开发环境(Eclipse, JDK, Tomcat) 
 
2.	新建 Java 工程 SimpleController ，在该工程下新建源码包
sc.ustc.controller，并在此包中新建 HttpServlet 子类 SimpleController，使用 RequestDispatcher 实现 SimpleController 类的功能如下：    
2.1 实现 doPost()方法，能够将 Http 请求默认响应输出为： 
  
2.2	实现 doGet()方法，调用 doPost() 
2.3	将 SimpleController 工程打包导出为 simple-controller.jar 
 
3.	新建 Java Web 工程 UseSC 
   3.1 将步骤 2 中的 simple-controller.jar 放入到 UseSC 工程的 lib 库中    3.2 在 UseSC 工程的配置文件 web.xml 中，定义 servlet 结点名称为 sc，
将其 servlet-class 指向 sc.ustc.controller.SimpleController，如下： 
  
3.3	在 UseSC 工程的配置文件 web.xml 中，定义 servlet-mapping 结点，将其 servlet-name 指向 sc，声名 url-pattern 为/*，如下： 
  
3.4	在 UseSC 工程中定义 welcome.html 并设置为该工程的欢迎页面 
 
4.	将 UseSC 工程打包为.war，并部署在 Tomcat 中。部署完成后，启动 Tomcat，并在浏览器输入：http://host:port/UseSC，观察页面是否为“欢
迎使用 SimpleController!”，如果否，调试代码，直到出现该结果 
