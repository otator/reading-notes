# Call Stcak and Debugging

### Call Stack
A call stack is a mechanism for an interpreter (like the JavaScript interpreter in a web browser) to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function, etc. [link](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack).

* When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
* Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
* When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
* If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.
 [link](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack).



 ### Debugging
[link](https://otator.github.io/reading-notes/class-10)

Running javascript code for the first time could result some errors, and not always we expect the output we want.<br>
for checking your code status in some place to know where the logical error occurs, this is called **debugging**.<br>

when you run the code, if javascript statement generates an error the interpreter will look for the line of code that generates  that error and looks if this line handled the exception, if not and it was inside a function scope, the interpreter will continue looking for the line that called this function and check if it handled the exception or not, if not it will keeping doing the process until the line that handled that exception, or it will generates an error object if it gets to the global scope and the exception did not get handled.<br>
javascript error object has the following:<br>
name: type of execution
message: description
fileNumber: file name of javascript file
lineNumber: line number of the error.
<br>
there are 7 types of errors: <br>

| Object | Description |
|------- |:-----------:|
|Error   | Generic error, all errors based on this object|
|SyntaxError| if the javascript syntax(rules) hasn't been followed|
|ReferrenceError| trying to use variable from within another scope|
|TypeError| when an unexpected data type that can not be coerced|
|RangeError| number not in acceptable range|
|URIError| encodeURI() and decodeURI() used incorrectly|
|EvalError| eval() function used incorrectly|

<br><br>

There are two ways of solving the errors:<br>
**Debugging** and **handling** errors.<br>
for debugging method many steps need to follow:<br>
* Look at the error message, it tells about the script name, the number line  and the type of that error.
* logging to the console a message to know how many times the script runs.
* use breakpoints where the errors occurs, it lets you pause the execution, and inspects values within variables.

in order of logging message to the console, use the following methods:<br>
* console.info(message); _used for general information_.
* console.warn(message); _used for warning_.
* console.error(message); _can be used to hold errors_

each of these methods used for logging to the console with different colors, all beside the console.log(message) method.<br>
<br>

for handling exceptions:<br>
if you know that the error might fail, use the try, catch and finally.<br>
each one of them has its own block of code, where the try blocks has the suspicious code within, the catch block will be executed once the code in try block fail, and the finally block will run in both ways, if the code of try block successfully run or not.<br>

```javascript
function division(){
  var n1 = prompt('Enter a number');
  var n2 = prompt('Enter another number for division');
  var result = 0;
  try{
    result = n1 / n2;
  }catch(e){
    console.log('error message: ' + e.name + e.message);
  }finally{
    return result;
  }
}
console.log(division());
```

 

