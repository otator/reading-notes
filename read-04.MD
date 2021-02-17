# Grid and RegEx

### Grid
grid is styling way in css for containers.<br>
to use grid you need to assign the value *grid* to the property *display*.<br>

```css
  .conatiner{
    display: grid;
  }
```

to assign the number of rows or columns in a grid, you need to use the *grid-template-columns* or *grid-template-rows*.<br>
and assigning them values of the number of rows and columns.<br>
```css
  .conatiner{
    display: grid;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 25% 25% 25% 25%;
  }
```
**the above styling makes 2 rows with 4 columns in each.** <br>

to add gab to columns, rows or both use the following
* grid-column-gap: for adding gaps between columns and its value is a number of pixels.
* grid-row-gap: for adding gaps between rows and its value is a number of pixels.
* grid-gab: for adding gaps between rows and columns and its value is a number of pixels.

### RegEx
regular expression or regex is a way of searching and exttracting data from text (string).<br>

to create regular expression object you need to put your text in between tow forward slashes.<br>
and also you can creat regex object by passing your text as argument in RegExp function.<br>

```javascript
  let text = "hello" // this is a string
  let text2 = /hello/ //this is regex object
  let text3 = RegExp(text); //this is regext object
```

some patterns in RegEx: <br>
* /^H/  matches any word that starts with H letter;
* /\d{3}/  matches any 3 digits.
* /B$/  matches any word that ends with B.
* /the/  matches any word that has *the* in it.
