# SMACSS and Floats

### SMACSS
SMACSS stands for Scalable and Modular Architecture for Cascading Style Sheets.

it is a way to divide the css code in some files following some rules to increase readability of the code and to make it easier to edit or add more styling.

these files are:

1. base.css
2. layout.css
3. modules.css
4. state.css
5. theme.css

each of the above files has his own rules for the css properties to be added.

for the **base.css** it has only the element selectors such ass *main*, *body*, *section* etc.. and it must not have any id or class selectors.

the **layout.css** it has the minor layout parts of the page that need positioing such as *#footer*, *#header* etc..

the **modules.css** it has the styling for class selectors only, where the small modules such as list items added inside it.

the **state.css** it has mixed rules form the layout and the modules.

the **theme.css** it has the colors for texts and the background colors.

### Floats
float is css positioing property.

to set the positioning for element to be float shown below:

```css
  nav ul li{
    float: right;
  }
```
after appplying the above code the element li will be floating to the right of the parent element.

adding float property to an element will makes it float either to right or left.

adding clear property with one of its values will make sure that the other floats will be cleared 
clear value are left, right, both or none.

```css
  footer{
    clear: both;
  }
```

after applying the above styling the other float in the page won't affect the footer and will make neneath of the other element.