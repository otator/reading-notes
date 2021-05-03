# Spring Authorization

[Authorization](https://economictimes.indiatimes.com/definition/authorization) is a security mechanism to determine access levels or user/client privileges related to system resources including files, services, computer programs, data and application features. This is the process of granting or denying access to a network resource which allows the user access to various resources based on the user's identity.

Spring boot gives us the ability to specify what access control a user has(what can he do/see), this is done by implementing the `WebSecurityConfigurerAdapter`,overrides its `configure` method and implement it the way you want for authorize users as shown in the code below:

```java
  @SpringBootApplication
  @RestController
  public class SocialApplication extends WebSecurityConfigurerAdapter {
    
      @Override
      protected void configure(HttpSecurity http) throws Exception {
        // @formatter:off
          http
              .authorizeRequests(a -> a
                  .antMatchers("/", "/error", "/webjars/**").permitAll()
                  .anyRequest().authenticated()
              )
              .exceptionHandling(e -> e
                  .authenticationEntryPoint(new HttpStatusEntryPoint(HttpStatus.UNAUTHORIZED))
              )
              .oauth2Login();
          // @formatter:on
      }
  }
```

inside the `authorizeRequests()` method are the routes that we allow for any user to see/do since they are permitted for all using the `permitAll()` 

**/** home/main route for the website and this route must be authorized so that the users can know what the website is about.
**/error** this route is for the errors that could happen throught the process of browsing the allowed routes.
__/webjars/**__ this route is for the javascript codes and css style, since we need them to be executed for all users.

In addition for the above three routes (**/signup**, and **/login** routes should also be permitted so that the users can signup or login)

`.anyRequest().authenticated()` these two chained methods mean that every other route needs an authorized user in order to access it.


