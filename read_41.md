# Intent-Filters

If your application has an activity that could be used from outside the application

Let's say that you have built a social media application, this application allows users to send a file(image, videos, etc..) from within the application itself, but what if you want to use one of the activities(chatting activity for example) from outside, well this is possible using intent-filters.

intent filters allow your activity to show up as an option when the user hits the sharing button on an image from the studio for example.

and when the user chooses your activity to share the image, and it is sent, then let the user go back to the activity he was using.

```xml
 <activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
  </activity>
```

The above code snippet is the intent-filter that must be added to the `Manifest.xml` file in order to show your application as one of the options in case of sharing an image or a text file.

change the `mimeType` to the type that you want your activity to handle.

`action.SEND` is to specify that your activity will show up as an option to perform sending whenever the `ACTION_SEND` is fired and if the type matches the `mimeType`


### What will happen if the user choses your activity?

well, you need to hanlde the intent that sent to your activity

to get the intent that sent to your activity use `getIntent()` method, and to get the data from the intent use `getIntent().getData()`

and you decide what to do after that...

the code below shows the handled activity and decide what action to take according to the data type

```java
  @Override
  protected void onCreate(Bundle savedInstanceState) {
      super.onCreate(savedInstanceState);

      setContentView(R.layout.main);

      // Get the intent that started this activity
      Intent intent = getIntent();
      Uri data = intent.getData();

      // Figure out what to do based on the intent type
      if (intent.getType().indexOf("image/") != -1) {
          // Handle intents with image data ...
      } else if (intent.getType().equals("text/plain")) {
          // Handle intents with text ...
      }
  }
```

if you want to return sort of result to the activity that invokes yours, use the `setResult()` method, and call the method `finish()` to return the user to that activity after the action is done.

```java
  // Create intent to deliver some kind of result data
  Intent result = new Intent("com.example.RESULT_ACTION", Uri.parse("content://result_uri"));
  setResult(Activity.RESULT_OK, result);
  finish();
```

as shown in the above code, you can send back result using an intent, the  `setResult()` method here to tell if the action is completed be returning `RESULT_OK` , you can return `RESULT_CANCELED` to tell that the action is canceled but this is the default behavior(when the user clicks the back button or you did not send the result)
