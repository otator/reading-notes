# CSS
## CSS Layouts
positioning in css is about putting elements where ever we want to, so the web page will look attractive and professional.<br>
css treats each html element as if it is has his own box.<br>
*There are many ways for element positioning:*
1. **position: static**
    in this way (*normal flow*) each element sits on the top of the next element, and this is the default way for positioning elements that browsers follow, so no need to use css property for this.
2. **position: relative**
  in this way moves the element where if it is in normal flow:<br>
  ```css
  p{
    /*set the position property to relative first*/
    position: relative;
    /*then move the element as desire, in this case 20 px to right*/
    left: 20px;
    /*also you can change the other properties such top.*/
    top: 20px;
  }
  ```
3. **position: absolute** 
  after setting the position to absolute, the box is get out of normal flow, and it no longer affects the positioning of the other element.
  using left, right, top, and bottom properties to tell where the box would be inside its container.
  ```css
  p{
    /*set the position property to absolute first*/
    position: absolute;
    /*change the right and the bottom offset of the element inside its container*/
    right: 50px;
    bottom:20px;
  }
  ```
5. **position: fixed** 
  its type of absolute positioning, which requires fixed position property, and it fix the element in its position when you scroll down. In the below example the heading will stick at the top of the page when you scroll down

  ```css
  h1{
    /*set the position property to fixed first*/
    position: fixed;
    top: 0px;
    left:50%;
    right:50%
  }
  ```

sometimes some elements need to show over other elements, css offers this ability using **z-index** property which its value is a number, and the element that has a value number bigger than another element, it overlaps it.<br>

using **float** property allows us to float element right and left as desired .<br>

use **clear** property to make elements within a container to a way from touching the left and right sides, and its value could be right, left, both or none of them.<br>

### Screen Size
a live website could be open using laptop, pc, tablet or mobile phone, and the website must look the same on all the screens.<br>

### Screen Resolution
resolution means how many pixels there are per inch. And the resolution varies from device to another, which could affect the appearance of the website on that device.<br>

#### Fixed width Layout vs. Liquid Layout
in fixed layout the designers can control the elements better than liquid layout, and setting values to pixels is more accurate. But if the user screen is higher resolution than the designers one, it will make the page look smaller, and text could be harder to read.<br>

in liquid layout method, designers use the percentage approach **%** control the page when increasing and decreasing the browser window. If the user screen vary wide it will end up with very long line of text which is hard to read.<br>


### multi style sheets 
if html page the designer can link more than one style file to control the look of the page.