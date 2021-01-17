# HTML and CSS
## Images
controlling an image by changing its size can be done by using css, by setting the width and height property in css to the desired values.<br>

images can be aligned to right or left using the float property, and by setting its value to left or right, the image will to left side or right side of screen respectively.<br>

to center an image has a class 'img-1' in css:<br>
```css
.img--1{
  display: block;
  margin: 0px auto;
}
```

if you wanted to change the background of an element, simply use the background-image property which its value will be the image name and the directory contains it being passed to url() as show below:<br>
```css 
body{
  background-image: url("https://www.tanikal.com/wp-content/uploads/2017/10/rami_malek_in_mr_robot_4k-wide-1024x640.jpg");
}
```
and it is possible to have more that one background image, by separating the urls by comma.<br>

the background-repeat property is doing pretty much as its name, since its values can be one of the following:<br>
* repeat-x it repeats the image horizontally..
* repeat-y it repeats the image vertically
* repeat it repeats the image in both dimensions.
* no-repeat show the image only once, which is default.

while the background-attachment value *fixed* sticks the image in the same position, the scroll value will make the image scroll up and down as the user scrolls.<br>

when the image need to be positioned in a specific position like top center, the property background-position can have this done by assigning the desired value.


## SEO
Search Engine Optimization<br>
if you want to have your website ranking in top result of search, you need to specify some things in order to have done this:<br>
1. The page title: which appears at the top of the browser window.
2. Url / web address: the name of the file is a part of the url, where is possible, use the keywords in the file name where possible.
3. Headings: if the keywords are in the **hn** tag then a search engine will know that this page is all about that subject and give it a greater weight than other text.
4. Text: it helps to repeat the text in the main body.
5. Links Text: use keywords in the text that creates links between pages, rather using click here to open another page.
6. Images Alt Text: the text within alt attribute, have search engines relying on when it accurately describes the image, which makes the image show up in the search result. 
7. Page Description: the description also inside the head element, and it is specified by using the **meta** tag, the content is not shown in the browser, it is only for the search engines in order to archive the page and show in the search results.

keywords can be identified during these steps:
* brainstorm: list all the words that comes in your mind that someone might type them in search engine search filed to find your website.
* organize: grouping the keywords into separate lists, and subcategories.
* research: use a tool to suggest more related keywords to yours.

for google search engine, use the analytic tool to know: How many people are coming to your website, What are your visitors looking at and where are your visitors coming from.

to put your site on the web, you need to get domain name and web hosting.

## videos and audios
an audio can be add to the page simply by using the audio tag which has some attributes with to use:
1. controls, this attribute used to show control panel, so that you can volume up or down, play pause and stop the video.
2. autoplay, which plays the audio once the page opened or reloaded.
3. mute, to mute the audio
4. volume, to set the volume with a value from 0.0 to 1.0;
<br><br>
for video it is pretty much the same of an audio with some different attributes such as poster which shows an image that has been loaded before the video start playing.<br>
the following code will show the video that below it:<br>

```css
<video src="video_1.mp4" controls></video>
```
<video src="video_1.mp4" controls></video>