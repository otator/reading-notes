# Local Storage For Web Applications.
storage for native web applications is given by the operating system as an abstraction layer for the application to store and retrieve specific data like preferences or run time status.<br>

in the early of web's history, cookies war invented(type of storing data), they can be used to store persistent data, but they had some dealbreaking downsides such tat cookies are included in each http request, which leads to transmitting the same data over and over, in addition to that the data is transmitted unencrypted, and cookies are limited to 4KB of data, which slows down the application.<br>

### storage before html5:
in the past where there was only internet explorer, where it came with the userData method which allows web pages to store up to 64 KB for each domain.


### html5 storage:
html storage is a way for webpages to store named key/value pairs locally, within the client web browser, and this data can be retrieved after you close the website and open it again, you will find the progress of a game for example the same as last time you opened the page.<br>

html5 storage can be accessed from within javascript code, using the localStorage object, but first you need to check if the browser supports the html5 storage by adding the following code:<br>

```javascript
function checkHtml5Support(){
  try{
    return 'localStorage' in window && window['localStorage'] !== null;

  }catch(ex){
    return false;
  }
}

```

since html5 storage store the data as key/value pairs, you can retreive the data using the key to get its value.<br>
*the key is always string, but the data could be any javascript data type, such as strings, booleans, integers and floats, but the values are actually store as strings, so that once you retrieve an integer for example you need to convert it from string to integer using the method parseInt().* <br>

localStorage is just a javascript object, you can deal with it as an array, for example:<br>
```javascript
//to get value from localStorage with the key 'token'
var token = localStorage['token'];
//to store value within the localStorage using the key 'password'
localStorage['password'] = password;
```

and you can add, remove or delete all the local storage content for the page.