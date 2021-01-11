# HTML
## Tables in HTML
tables are display method, some data need to be display in a grid view, this why we use tables in html.<br>
using the **table** tag will create empty table, to add rows to table, use the **tr** tag (table row), where the **td** tag (table data) used to create table columns.<br>
in order to add heading to the table, use the **th** tag (table heading), where you need to specify it *scope* attribute, which controls the display of headed of being column heading or row heading.<br>
For Example the following code will display the marks o 3 student for 3 courses.
```html
<!--Inside the body tag-->
<table>
    <tr>
      <th></th>
      <th scope="col">Math</th>
      <th scope="col">C++</th>
      <th scope="col">physics</th>
    </tr>
    <tr>
      <th scope="row">Ahmed</th>
      <td>85</td>
      <td>91</td>
      <td>71</td>
    </tr>

    <tr>
      <th scope="row">Rami</th>
      <td>95</td>
      <td>99</td>
      <td>94</td>
    </tr>

    <tr>
      <th scope="row">Anas</th>
      <td>74</td>
      <td>84</td>
      <td>65</td>
    </tr>
</table>
```
This will be the result: 
<table>
    <tr>
      <th></th>
      <th scope="col">Math</th>
      <th scope="col">C++</th>
      <th scope="col">physics</th>
    </tr>
    <tr>
      <th scope="row">Ahmed</th>
      <td>85</td>
      <td>91</td>
      <td>71</td>
    </tr>
    <tr>
      <th scope="row">Rami</th>
      <td>95</td>
      <td>99</td>
      <td>94</td>
    </tr>
    <tr>
      <th scope="row">Anas</th>
      <td>74</td>
      <td>84</td>
      <td>65</td>
    </tr>
  </table>

<br><br>
some times some columns or rows require to be single cell and this can be achieved by using the *colspan* attribute with **td** or **tr**.<br>

**thead**, **tbody** and **tfoot** are used in case of long tables to separate the heading of the table from the content and to show if there are any values in the footer of the tables.<br>

<br><br>

# JavaScript

## JavaScript Objects and Constructors
another way to create an object is by using the object constructor notation rather than using the literal notation in javascript, this is done by using the **new** keyword then the Object constructor:<br>

```javascript
//create student object
var student = new Object();
//adding some properties to this object
student.name = 'Rami';
student.average = 96;
```
and to update an object property simply do the following:<br>

```javascript
student.average = 98;
```
what if we have more than one student in a class? which is true!<br>
we can create object constructor that can creates as many as object we want:<br>
```javascript
function Student(name, average){
  //this keyword refers to the object
  //and this.name refers to the object property which is 'name'
  this.name = name;
  this.average = average;
}
//later we can use this function to create student objects as desired
var student1 = Student('Anas', 74.3);
var student2 = Student('Ahmed', 82.3);
```

## Built-in JavaScripts Objects
1. Browser Object Model *BOM*
2. Document Object Model *DOM*
3. Global JavaScript Objects

In BOM there is the window object, which represented the current browser window or tab opened.<br>
this objects container other objects that tell about the browser.<br>
window.innerHeight is one of these objects that tells about the window height, and window.location refers to the current window url or file path.<br>

In DOM there is the document object, which is a tree of html page tags, this object allow javascipt to access, modify and update the html structure from with javascripts.<br>
one of the methods of the document object is documentgetElementById('tagId'), which points to the element that has that id within parenthesis.<br>

Global Javascript Objects such as string which has many methods and properties within like length property which tells how long the string is, toUpperCase() method which converts a string to upper case letters.
and all the other data types along with the string are global javascript objects.<br>
another example of the global objects of javascript is the Math object, 
this objects contains all the necessary methods and properties for using in case.<br>
property example is Math.pi, which return the value of pi in decimal.<br>
method example is Math.random(), which generates a random number between 0 and 1.<br>
