# HTML
## HTML Forms
forms are the ways used to collect information, the most famous form is google form that used to get information from people.<br>
a form has many filed to get data such as:
* text fields: to input plain text such as username or email
* password field: to enter password, where the characters show as starts so that no one can see the password.
* drop down menu: to choose a value among specific values.<br>

and many other.

### Forms Work
once the submit button for the form clicked, all the data is sent to a server, where this data is being processed using a programming language, and this data could be store in databases.<br>

to create a form in html use the **form** tag, this tag has two attributes need to specify them, first the *action* attribute which its value is the url for the page on server that will receive the information form once it submitted. And the other attribute is the *method* attribute which specify the way that data will send use, and its value could be get for unencrypted information and post for encrypted information.<br>

### Example of Form Input Fields
1. input text **input**.

```html
<!-- since input fields has no content, you must specify to the user-->
<!--what to write in this filed, use paragraph tag for example -->
<p>Username</p>
<!--the type is used to specify what the input filed will be for--><br>
<!--change it to password for password input field--><br>
<!-- the name used to identify the filed and link its dat with it--> <br> <!--it must be unique a cross the page -->
<input type="text" name="username_filed">
```
**Login Example**
<p>username <input type="text" name="username_field"></p>
<p>password  <input type="password" name="password_field"></p>

2. input field **radio button**


```html
<p>Choose color</p>
<input type="radio" name="red_color" value="red">
<input type="radio" name="blue_color" value="blue">
<input type="radio" name="green_color" value="green">
```

*checked is used to check the default value.*<br>

<p>Choose color</p>
Red
<input type="radio" name="red_color" value="red" checked="checked">
Blue
<input type="radio" name="blue_color" value="blue">
Green
<input type="radio" name="green_color" value="green">
</div>

3. Drop down menu list
uses to choose a value among many values, use the **option** tag within the **select** tag to add option to the menu.<br>

```html
<p>choose the read you want
<select name ="reads">
<option value="read1">Read1<option>
<option value="read2">Read2<option>
<option value="read3">Read3<option>
</p>
```

<p>choose the read you want
<select name ="reads">
<option value="read1">Read1<option>
<option value="read2">Read2<option>
<option value="read3">Read2<option>
</select>
</p>
<br>

there are many other fields such as file fields to upload a file to the form, and submit button to submit the form once the user clicks on the enter key.<br>

### Form Validation
html5 added validation to the input fields so that it shows warning message to the user if he forget to fill a filed, and the form won't be submitted if the field is requires input. to achieve that add the *require* attribute with 'attribute' value to the required fiele.<br>

html5 also added validation for the input filed to be email, or url, and the form won't be submitted until valid email or url entered.<br>

```html
<p>Enter Your Email: <input type="email" name="email_filed">
<input type="submit" value="Submit">
```
Try it: by typing random text<br>
hover the mouse over the input filed, it will show a message to tell that you must enter email.
<p>Enter Your Email: <input type="email" name="email_filed">
<input type="submit" value="Submit">
<br><br>

## Lists, Tables and Forms

coming soon...

# JavaScript

coming soon...