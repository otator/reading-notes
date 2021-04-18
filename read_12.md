# Spring RESTful Routing & Static Files
one of the most important annotations is `@RequestMapping`

the following code snippets are from [Baeldung](https://www.baeldung.com/spring-requestmapping) website
example make a route /ex/foos, and get it using `GET` method.

```java
  @RequestMapping(value = "/ex/foos", method = RequestMethod.GET)
  //this annotation to not maps with templates and shows error
  @ResponseBody
  public String getFoosBySimplePath() {
      return "Get some Foos";
  }
```

the same route using `POST` method

```java
  @RequestMapping(value = "/ex/foos", method = POST)
  @ResponseBody
  public String postFoos() {
      return "Post some Foos";
}
```

to send headers with the request see example below:

```java 
  @RequestMapping(value = "/ex/foos", headers = "key=val", method = GET)
  @ResponseBody
  public String getFoosWithHeader() {
      return "Get some Foos with Header";
  }
```

add path variables to request 

```java
  @RequestMapping(value = "/ex/foos/{id}", method = GET)
  @ResponseBody
  public String getFoosBySimplePathWithPathVariable(
    @PathVariable("id") long id) {
      return "Get a specific Foo with id=" + id;
  }
```