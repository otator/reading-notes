# HTML
## Links
to create link in html, we use anchor **a** tag.<br>
### Types of Links
* Links to other websites.
* Links to other pages.
* links to other parts in the same page.
<br>

Links to other websites like [Google](https://www.google.com).
The link is a value for the *href* attribute, and the **a** tag has another attribute *target* that specify where to open the new 
website in the same window or in a new window:

```html
<a href="https://www.google.com"  target="_blank">
```
Link to other pages in the same website, we should use the directory of the page that need to open, 
if the two files in the same level, just use the name of the file. For example: <br>

```html
<ul>
    <li><a href ="about-us.html">About Us</a></li>
</ul>
```
Link to other part in the same page, here we need to use the id of the part the needed to go to:<br>

```html
<ul>
    <li><a href="#container">Home</a></li>
</ul>
<div id = "container">
.
.
.
</div>
```
also we can go to specific part of another page using the same technique as shown below:<br>

```html
<h3><a href="about-us.html#bottom">Contact us</a></h3>
```

## Layout


# JavaScript
## Functions and Methods
function is a set of statements that can written inside a block to use later in code, it reduce code repetition and make code more easy to follow.<br>

To declare a **function** keyword must be used first, then the name of the function as desired, and the parenthesis where it allows to pass parameters to the function to use, as shown below:<br>

```javascript
function getCircleArea(radius){
    return Math.pi * radius* radius;
}
```
to use (*call*) the function above, just type its name and pass an argument for it:<br>
```javascript
var circleArea = getCircleArea(2);
```
functions don't necessarily need parameters or return values, for example shown below, function takes no parameters and returns no thing:<br>
```javascript
function generateRandom(){
    //this function generate random number in range (1,10)
    var rand = Math.random() * 9 + 1 ;
    //display the value as header 2 in html document
    document.write('<h2>' + rand + '</h2>');
}
```
**variable that are defined inside a function, they can not be used out side of it, because of the variable scope, where they are known only inside the function block**

