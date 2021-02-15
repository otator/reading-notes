# Mustache and FlexBox
## Mustache
Mustache is a template that has less logic and it used to deal with HTML. <br>
it has no for loops or if-else clauses, only **tags**.<br>
Mustache uses placeholder concept, and for a placeholder, it used {{placeholder}}.<br>
and it will replace whatever inside the double braces with an object value.<br>
```javascript
  let date = new Date();
  Mustache.render('year is: {{year}}', {year: date.getFullYear()});
```

## FlexBox
flex boxing is a positioning method, its use to position elements within the page.<br>
to make an element has the flexbox property, *display: flex;* property is added for the selected element.<br>

**some properties**.<br>
* flex-direction: which its values are row, row-reverse, column, and column-reverse.<br>
it changes the direction of the elements within the container to row or column.
* order: which its value is a number of the elements that need to change their order among other elements.<br>
* justify-content: which has many values
    * center: to center the content within the container.
    * flex-start and flex-end: to set the content to the beginning or the end of the container.
    * space-between: to separate the elements with a space between them only.
    * space-around: to add a space around the elements.
* align-items: its values are flex-start and flex-end to set elements to the top or the bottom of the container.<br>
and center for centering the elements vertically within the container.
* align-content: it is pretty much the same as the align-items property but it has extra values which are<br>
space-around and space-between to add space around or between the elements.<br>




 