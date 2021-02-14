# JQuery
JQuery is JavaScript library that uses the selection rules of css to get html elements into javacode and perform some tasks on them.<br>

first to link the jQuery library paste the following line of code into the head of the main html page.<br>

```html
  <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
```

the **$** operator is used to select an element followed by the css selecting rule and once the elements selected many jQuery methods can be applied on it<br>
```javascript
  $('p').text('This text added using the jQuery method text()')
```

**what if the jQuery code had executed before the html page loaded or before some elements loaded?**<br>
this will cause an error.<br>
so make sure that the jQuery code will be executed after the page loads, we use the following code. <br>
```javascript
  $(document).ready(function(){
  //here the code the will be executed once the page loaded
});
```
and since the above code used each time jQuery used, a shortest way has been added.<br>
```javascript
  $(function(){
    //here the code the will be executed once the page loaded
  });
```
**Some jQuery methods** <br>
* html() to add an html code to the selected element.
* hide() to hide an element.
* before() and after() they are used to insert content before and after the selected element.
* val() is used to get or set the selected element content such as forms fields and other inputs.
<br>

example:<br>

```javascript
  $('#main-container').html('<h2>Section 1</h2>');
  $('.section3').hide();
  $('div').after('<p>in this section we will talk about...</p>');
  let userName = $('#username').val();
```

**Events** <br>
The events are being handled with jQuery using the click method on selectd elements.<br>
This method takes a function as an argument, and this function has the code to be executed once the event occured.<br>
```javascript
  $(function(){
    $('#show-name').click(function(){
      alert($('#name').text());
    })
  });
```
To add more than one event on an element, the **on** keyword used, it takes two arguments.<br>
The first is the events sepearated by space as string and the other argumenst is the event handler which is the function to be executed.<br>

```javascript
  $(function(){
    $('show-button').on('click dblclick', function(){
      alert('button clicked');
      //remove the event listener
      $('show-button').off('click dblclick');
    });
  });
```
To remove an event listener form an element the **off** method is used that takes the event/s as an argument.<br>
**The event handler function could have an event as an argument to used once the event occured**

## Animation
JQuery gives the ability to add animation on selected elements.<br>
some animation methods:<br>
* hide() to hide an element.
* show() to show an element.
* toggle(), fadeToggle() and slideToggle() to toggle between showing and hiding the element.
the above methods has some arguments that do stuff, the first argument is the time in *meliseconds* that the animation will take.<br>
and callback function to be executed once the animation is done.<br>

example:<br>

```javascript
    $(function () {
    //asiging the selected element to variable to use later in code.
    let header2 = $('h2');
    header2.css('color', 'red');
    header2.click(function () {
      header2.fadeToggle(3000, function () {
        header2.show(4000);
      });
    });
  });
```
<br>

<script src="https://code.jquery.com/jquery-3.1.1.js"></script>
<h2>Click me</h2>
<script>
  $(function () {
    //asiging the selected element to variable to use later in code.
    let header2 = $('h2');
    header2.css('color', 'red');
    header2.click(function () {
      header2.fadeToggle(3000, function () {
        header2.show(4000);
      });
    });
  });
</script>
</script>