# Webpages Desing Parts
## Text in HTMl
-html offers many heading tags in order to arrange the content and makes it easier to follow. <br>
-The heading  are arranged from the biggest which is **h1** to the smallest **h2**.<br>

-In order to have a long text or an article there is the **p** tag which stands for *paragraph*.<br>
for text styling html has two tags related to this, **b** tag the makes the content within **bold**, and the **i**
tag that makes it *italic*.<br>
for mathematics and chemistry html has two special tags for these subjects.
* sub tag is used to have text sub text for example: H<sub>2</sub>O.
* sup tag is used to have text super text for example: X<sup>3</sup> + 2X<sup>2</sup> + 4x + 1
<br>

white spaces is being ignored in html by the browser, new line is supported by using **br** tag.
also there is horizontal break line like the line below:
<hr>

Html has many other tags to manipulate text and modify it.
* s tag to put a line over text which means the items is <s>no longer accurate or relevant</s> like a price of something.
* ins tag <ins> to that the piece of text that was inserted inside a text.

## CSS Style
css stands for cascading style sheets.<br>
css used to add styles to html tags. 
and this could be done by adding inline style for example.<br>


```html
<h1 style="font-family:cursive;">This is h1 has different font from default</h1>
```
and there is internal style for html pages by adding **style** tag inside the **head** tag in order to changes have effects.
There is also another way, which is having css folder and the css files come inside it.<br>

there are three main types of changing style in css by using selector and description method.<br>
* selection by tag name, for example.<br>


```css
p{
    font-family: cursive;
    font-size: 22px;
    color: black;
}
```
it can also be more than on tag to style, and this is done by adding the desired tags separated by commas. For example<br>


```css
h1, h2, h3{
    color:red;
    font-family: fantasy;
}
```
* selection by class name, the requires to have the attribute class inside the tags that need to be modified. for example
```html
<p class = "main-paragraph"> This is the main paragraph in the page</p>
```
and the css for it.
```css
.main-paragraph{
    font-family: cursive;
    font-size: 22px;
    color: black;
}
```
in this method the same style can be applied to many tags as desired.

* selection by id, this is can be applied for only one tag, since tags must be unique across the website.
and this method also requires to have additional attribute inside the tag which is id attribute.
for example
```html
    <h5 id="h5-footer">contact us on email shown below.<h5>
```
css code will be
```css
#h5-footer{
    font-family: monospace;;
    color: black;
}
```
in order to have the effect of the external css code, it is a must to have the code path in html page.<br>
where need to add **link** to the **head** tag as follow:<br>
```css
<link href="css/example.css" type="text/css"
rel="stylesheet" />
```
where the href holds the path of the css file.<br>

## Instructions in JavaScript
### Variables in JavaScript
javascript is dynamically typed language, which means there is NO need to specify what the variable datatype is
string, booleans, or even numbers. since the interpreter will make the decision of the variable type as its value.<br>
but what is the variable?<br>
variable is just place in a memory that holds data, and it is being names to refer to this place in memory later in code and use or update its value. <br>
to declare a variable in javascript the word **var** is being used in the front of the variable name to specify that this is a variable.
for example.
```javascript
var pi;
```
to assign a value to a variable equal sign (**=**) is being used, for example
```javascript
var pi = 3.14;
```
Every programming language has its own rules of naming variables.<br>
for example variables in javascript **must only** start with letter, $ sign or underscore _ .<br>
no spaces allowed in the variable name not dots.<br>
reserved words like **var, for, if** can not be used as a variable name.<br>
but do variables allowed to have more than one value at the same time?<br>
for normal variable this is impossible, but programming languages have their ways to do this.<br>
**Arrays** in java scripts allow to have many values inside them for example:
```javascript
var days = ['Sunday', 'Monday', 'Thursday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
```
to get a certain value inside an array, it needs to mention its index, for example 
Monday has the index 1 while Sunday has index 0.<br>
```javascript
var days = ['Sunday', 'Monday', 'Thursday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
console.log(days[6]); // this line will logs Saturday.
```
but what if iterating over all the elements is required, for or while loops can used for this job, 
where must have the iterator variable starts from 0 to the end of the array.<br>
expression can be done when declaring a variable:
```javascript
var pi = 22/7 ;
```
String concatenation can be done by simply adds the + sign for example
```javascript
var greeting = "Hello";
var name = "AbdalQader";
var result = greeting + name;
console.log(result); // this will log Hello AbdalQader

```
### Conditions in JavaScript
what if a specific line of codes need to be executed only when a condition met?<br>
javascript is great language and it offers the **if** statement, to do this job.<br>
Simply if statement has a punch of lines (at least on line) inside it, and those won't be execute unless the condition will meet.<br>
double equal signs **==** are used to compare between to variables to test the condition.<br>
For example:
```javascript
var mark = prompt("enter a number");
if(mark >= 50 && mark<=100>){
    alert("Passed!");
}
```
In the above example if the user enters a mark more than or equals 50, the browser will show him that he passed.<br>
but what if the user entered a mark less than 50, what will happen?<br>
Absolutely no thing, since the condition did not meet, the code after the closing curly bracket **}** will be executed.<br>
What if wanted to show fail if the user enters a number less than 50?<br>
this can be done by adding another if statement to check the mark is less than 50 and show fail in the browser.<br>
also adding else statement will work, where else statement code will be executed if the condition if statements evolves to false.<br>
For example
```javascript
var mark = prompt("enter a number");
if(mark >= 50 && mark<=100>){
    alert("Passed!");
}else{
    alert("failed");
}
```