# JavaScript
## Objects in JavaScript.
**Objects in javascripts is like a container, that has variables and function inside.**<br>
Variables called *properties* if they are inside an object and the *functions* become methods.<br>
to create an object in javascript, first the name of the object, the curly brackets to determine the object block, 
then the properties which are written as key-value, and then the methods.<br>
**values can NOT have more than one key, since the key is unique and it is used to get the value within, but the key can have more than one value, arrays for example.**<br>

Example:<br>

```javascript
student{
    name:'AbdalQader Mhemed',
    age: 24,
    GPA: 3.6,
    programming_langs=['C++', 'java', 'python', 'javascript'],
    getName: function(){
        return name;
    }
}
```

to access object content of properties and method, simply use the object name then a dot the property/method key:<br>

```javascript
var avergae = student.GPA;
```
another way is using square brackets with the key inside to get the value:<br>

```javascript
var age = student['age'];
```

## Document Object Model (*DOM*).
DOM is responsible of creating an object of the html page, so that it can be accessed and modify it by javascript in the browser window.<br>

*DOM is not javascript nor html, it is stand alone rules.*<br>
### DOM Tree
when browser load a webpage it creates a model for that page, it called dom tree.<br>
once the model is created and cached in the browser memory, javascript can access this model to update the html page by using the methods in the document object, for example to create a new paragraph inside an element that has an id equals to 'main', the code will be:<br>

```javascript
var main = document.getElementById('main');
var paragraph = document.createElement('p');

//change the paragraph content
paragraph.textContent = 'this is the main paragraph';
//adding the paragraph to the parent tag which is main
main.addChild(paragraph);
```

there are many method to deal with the document(html page) for example,
to get all the li tags, instead of getting them by ids which could take for ever, the dom has the magic method call *getElement**s**ByTagName*:<br>
```javascript
AlllistItems = document.getElementsByTagName('li');
```
using class name:<br>

```javascript
AlllistItems = document.getElementsByClassName('menu');
```

to remove an element form the dom tree, first we need to get the element using any method such as *getElementById* or 'getElementsByTagName' and specify which element to choose using index, then get the parent node using the *parentNode* property, and finally run the method *removeChild* on the parent element passing it the child element as below:<br>

```javascript
//get the 5th list item in document
var listItem5 = document.getElementsByTagName('li')[4];
//find the parent node
var parent = listItem5.parentNode;
//remove the list item from the parent node
parent.removeChild(listItem5);
```

attributes in html such as *class*, *height*, *style** ... etc. can also be used in javascript, in order to change the attribute value of update it:<bt>
```javascript
var container = document.getElementById('main').getAttribute('class');
```
change and update attributes:<br>

```javascript
//if there is footer tag that has class called 'footer' and we want to 
//change its class name to something else describes it better for example
var el = document.getElementById('footer');
//change the class name for the element
el.className = 'footer-class';

//if there is an element that has no class attribute and we want to add one
//simply do this during javascript at run time using the following
//find element
var header1 = getElementByTagName('h1');
//add 'main-header' class to this element
header1.setAttribute('class', 'main-header');
```