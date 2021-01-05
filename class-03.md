# HTML
## Lists In HTML
Html offers 3 types of lists to use in case:
* Ordered Lists
* Unordered Lists
* Definition lists

### Ordered Lists
In order to create *ordered lists* the **ol** tag, and the elements are created using **li** tag as shown below:<br>

```html
<ol>
    <li>Item1</li>
    <li>Item2</li>
    <li>Item3</li>
</ol>
```

### Unordered Lists
To create *unordered lists*, the **ul** tag is being used, and the **li** to create list items as shown below:<br>

```html
<ul>
    <li>Item1</li>
    <li>Item2</li>
    <li>Item3</li>
</ul>
```
### Definition Lists
This kind of lists is created using the **dl** tag, dl is a bit different from ol and ul.<br>
since dl define the term-definition method. create terms with **dt** tag, and for the definition **dd** tag is used.<br>

```html
<dl>
    <dt>Mansaf</dt>
    <dd>
    Jordanian main food, the main ingredients are meat, rice and jameed.
    </dd>

    <dt>Magloubah</dt>
    <dd>
    Palestinian food, the main ingredients are chicken, rice, cauliflower, and potato.
    </dd>

    <dt>Tappoulah</dt>
    <dd>
    Syrian food, it is pretty much a kind of salad with groats.
    </dd>
</dl>
```
**Lists can be nested inside each other.**



## Boxes In HTML
each block element in html has a box surrounding it, to see that clearly, the tag background must be changed into another color than white.<br>
The boxes size is being auto resized according to the content within.<br>
Also the size can be changed as desired. To change the box size, width and height attributes are used.<br>
there three ways or units to describe the box size.<br>
* Px is used when the size of the screen is known.
* Percentage **%** this makes the box size relevant to other box size.
* em used to resize the box according to a text within.

the percentage and the em are used more than px since web developers have to deal with different screen sized, where the design must 
be responsive to these screens.<br>

Border, padding and margin are all styling to change the box appearance.<br>


# JavaScript
## Switch statement

if there are many values for a condition to check, many if statement can be used for this case, but this way is slow and 
even if a condition met, all of the other if statements will be checked as well.<br>
javascript offers a better and fasters solution, which is using switch statement, the structure of switch statements shown below, it has as many cases as desired and a default case the will be executed if none of the cases matches, if a case matches, the switch statement will stop executing and checking the others cases, which is done by using break keyword. For example:<br>

```javascript
    var mark = prompt('Enter your degree').toUpperCase();
    switch(mark){
        case 'A':
            alert('Excellent');
            break;
        case 'B':
            alert('Very Good');
            break;
        case 'C':
            alert('Good');
            break;
        case 'D' :
            alert('Passed');
            break;
        case 'F':
            alert('failed');
            break;
        default:
            alert('Invalid mark');
    }

```