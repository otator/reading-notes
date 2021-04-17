# Spring
spring is a java framework to handle web pages

[Spring MVC](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html) In a typical Spring MVC application, @Controller classes are responsible for preparing a model map with data and selecting a view to be rendered. This model map allows for the complete abstraction of the view technology and, in the case of Thymeleaf, it is transformed into a Thymeleaf context object (part of the Thymeleaf template execution context) that makes all the defined variables available to expressions executed in templates.

[Thymeleaf](https://www.thymeleaf.org/) is a modern server-side Java template engine for both web and standalone environments.

Thymeleaf's main goal is to bring elegant natural templates to your development workflow — HTML that can be correctly displayed in browsers and also work as static prototypes, allowing for stronger collaboration in development teams.

With modules for Spring Framework, a host of integrations with your favourite tools, and the ability to plug in your own functionality, Thymeleaf is ideal for modern-day HTML5 JVM web development — although there is much more it can do.

### Create a simple web page using spring
to create simple project navigate to [start Spring Project](https://start.spring.io/) click generate then unzip the file that had been downloaded then open it using your IDE (IntelliJ for example)

create class called GreetingComtroller.java 
and add the following code inside it.

```java
package com.example.servingwebcontent;


import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

@Controller
public class GreetingController {

    @GetMapping("/greeting")
    public String greeting(@RequestParam(name="name", required=false, defaultValue="World") String name, Model model) {
        model.addAttribute("name", name);
        return "greeting";
    }

}
```
this class will handle the `/greeting`  when ever it requested with a single parameter `name` and if the name parameter not passed default parameter will be set which is *World*.

and to add html pages navigate to `recources` then `templates` and add html file called `greeting.html`with the following code in side it 

```html
<!DOCTYPE HTML>
<html xmlns:th="http://www.thymeleaf.org">
<head>
    <title>Getting Started: Serving Web Content</title>
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
</head>
<body>
<p th:text="'Hello, ' + ${name} + '!'"></p>
</body>
```

Now to run the web page do the following:
* build the project using `./gradlew build`
* after build is done a jar file will be created inside the `build/libs/` directory, to run this file use this command `java -jar build/libs/serving-web-content-0.0.1-SNAPSHOT.jar` make sure that the file name of jar is the same name, else change it accordingle to yours.
* now the code server is runing open your browser and type `http://localhost:8080/greeting`, a page with text *Hello, World!* will be opened

to change the "World" word add name parameter with the value you want as this `http://localhost:8080/greeting?name=AbdalQader` and the text will changed to *Hello, AbdalQader!*.
