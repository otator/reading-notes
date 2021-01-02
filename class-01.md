# Webpages Design parts

## HTMl
HTML pretty much like documents in real life such as newspapers or insurance forms.<br>

### HTML Structure
In order to have a web page written using html, it is a must to follow the rules of the language, like main tags, what tag to use 
inside other tags and which not. <br>
in html, the main page must have at least the html tag, the body tag and the doc tag that tells the browser what html version the webpage uses. For example
```html
    <!DOCTYPE html>
    <html>
        <body>
        </body>
    </html>
```
The head tag is used to have the title of the page with, and it also contains meta tags that tell the search engines what to do with page, like show it or not in the search results, or even caching it to local servers to enhance the speed of loading the page.<br>

The body tag has all the content that will be shown in the browser main window.<br>
There are main three tags that must come within the body tag for better structure:<br>
* header 
* main
* footer
<br>
the header tag points to the top part of the page where the navigation menu and the name or the logo of the page must be there. <br>
the main tag has all the main content the comes between the header and the footer, and this is the main content of the page.<br>
the footer tag where come the contact info or the links of social media accounts.<br>
*Both header and footer must not change along with the other pages.*
<br>
There is also many tags that responsible of the division of the page, like div, section, article, aside, figure...<br>


## Javascritpt
Is the behavior layer of the page, its usage to handle the interaction of the users with page, like when a button is clicked, certain function in javascript will be executed to serve the click. <br>
*Simple example of javascript inside html.*<br>

```javascript
<html>
    <body>
        <script>
        var day = new Date();
        var hour = day.getHours();
        if(hour < 12){
            alert("AM");
        }
        else{
            alert("PM");
        }
        </script>
    </body>
</html>
```
the above example is used javascript within html tags.<br>
javascript is also can stand in a separated folder and separate file, and it can be referred to using the following tag.<br>
```javascript
<script src="js/app.js"></script>
```
where js is the folder that contains the javascript code, and app.js is the javascript code itself. <br>
