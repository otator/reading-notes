# HTML Images, Colors, Text
## Images
adding images in the right way to a web page it will make it look attractive  and professional.<br>
to add images to web page, **img** tag is used. *NOTE: __img__ tag has no content, so that it does not need closing tag.* <br>
There are more than one way to add an image:<br>
* adding images from public website.
```html
<img src = "https://picsum.photos/536/354" alt = "lake with building view"/>
```
*src* is used to have the url within, while the *alt* should have the description, in case of any error of loading the image.

* adding images in the web page files.
```html
<img src = "img/image1.jpg" alt = "lake with building view"/>
```
the name of the image must contain the extension of the image.<br>

*width* and *height* properties are used to control the size of the image.<br>


## Colors
colors can be applied for the text or the background of an element.<br>
colors is changes using css, inline or using selectors.<br>
* Foreground colors.

to change text color, use the color property in css. As shown below:<br>

``` html
<h2 style = "color:red">Warning!</h2>
```
* Background colors.

to change background color, use the background-color property in css. As shown below:<br>

```html
    <body style="background-color:gray">
    .
    .
    .
    </body>
```
since color are limited by their names, css offers many ways to specify colors.<br>
* Hexadecimal colors, each color consists of 6 digits starting with # sign. For example:<br>
to color h1 text with green.<br>

```css
h1{
    color:#00ff00;
}
```
* Red-Green-Blue __RGB__ to choose color, you need to specify each color with value from 0 to 255 as shown below:<br>
```css
h1{
    color: rgb(0,255,0);
}
```
there is another property it is pretty much the same as RGB but with opacity, which its value between 0 to 1:<br>
```css
h1{
    color: rgba(0,255,0, 0.5);
}
```

* Hue Saturation Lightness __HSL__:

in this method each part need id different in specifying the colors, for example
the *hue* represents the color as an angle with values range from 0 to 360.<br>
the *saturation* represents colors as percentage.<br>
the *lightness* also use percentage to specify color, where 0% is white, 50% is normal and 100% is black.<br>

```css
h1{
    background-color: hsl(128, 100%, 50%);
}
```

there is also similar property to hsl with transparency which is hsla where the value ranges form 0 to 1:<br>


```css
h2{
    background-color: hsla(128, 100%, 50%, 0.5);
}
```


## Text
css offers plenty properties to style texts.<br>
to change the text font, use *font-family* property. NOTE: the font of this page will changes to cursive by changing the text font in body,
and since markdown supports html, the text font will change.<br>

html 
<body style="font-family:cursive">
</body>

*font-weight* will change the appearance of the text, to be bold, *font-style* to choose which from style (italic, normal, oblique) to choose, and the *font-size* will change the text size as desired. For example:<br>
```css
h1{
    font-weight: bold;
    font-style: italic;
    font-size: 36px;
}
```
to change the text to capital or to small, use *text-transform*, with either uppercase or lowercase values, and text-align property aligns the text as desired in the page. For example to make all the text inside h1 capital and centered in the middle of the page:<br>
```css
h1{
    text-transform: uppercase;
    text-align: center;
}
```

another interesting property to style text is text-shadow property, to see how the effect id please visit this link [Shoes Factory](https://otator.github.io/webpages/page_01), and see the website name and the prices.<br>
