# JavaScript
## Expressions
java scripts uses the **var** keyword to assign values to a variable. For example,
*var pi = 3.14*<br>
it also allows operations to be done while assigning a variable. For example *var pi = 22/7* <br>
javascript also has comparison operators which return true or false where they can be used as a conditions
for **if** and **while** statements.<br>
mathematical operators are also defined in java, where you can add, subtract, increment, or even to obtaining the modulus<br>

strings in javascript can be added *(concatenated)* by using the + sign. For example *var h = 'hello '*, and *var w = 'world'*
you can simply concatenate the tow word like this *h+w* an the result will be 'hello world'. <br>

## Functions in Javascript
a function is a punch of serialized statements the perform specific task, they are you to reduce the code by calling 
the function itself instead of repeating the code over and over.<br>
to define a function, must start with **function** keyword then the name of the function and two parentheses, where you can pass parameters for the function and the start block bracket then the statements of the function. For example <br>

function getCircleArea(radius){
    var pi = 22 /7;
    var area = pi * radius * radius;
    return area;
}
to call this function, you don't need to rewrite the statements again, just the name of the function. For example<br>
var r = 2;
var circleArea = getCircleArea(r); when the return statements in the function will return the area to store it in circleArea variable.

