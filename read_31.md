# Espresso

[Espresso](https://developer.android.com/studio/test/espresso-test-recorder) is a testing framework designed to provide a fluent API to write concise and reliable UI tests

Some methods in the  Espresso framework:

* `withId()` return matcher after evaluating the id of a view
* `onView()` this method gets the view that needs to tests and takes argument of type matcher which returns from the `withId()` method
* `perform()` takes many arguments to be performed such as `click()`, `typeText()`,  `replaceText` etc...
* `click()` to click on a view 
* `check()` to check whether a view matches a matcher

To start with Espresso, first you need to add its dependincies in the `gradle.build` file 

```java
  androidTestImplementation 'androidx.test.espresso:espresso-core:3.1.0'
  androidTestImplementation 'androidx.test:runner:1.1.0'
  androidTestImplementation 'androidx.test:rules:1.1.0'
```

then you will be able to add the tests you want for the UI.

The following code is to test if a username entered in another activity and checks if it displayed in the main activity

```java
 @Test
  public void checkUsername(){
      // this line to find a button by its id that opens settings activity and clickit 
      onView(withId(R.id.settingBtn)).perform(click());
      // find input field where a username needs to be entered and enter a username then closes the keyborad
      onView(withId(R.id.usernameEditText2)).perform(replaceText("AbdalQader"), closeSoftKeyboard());
      // find a button called save and clicked, this button save the input username and return to the previous activity (MainActivity)
      onView(withId(R.id.saveBtn)).perform(click());
      //check if the username entered in the previuos lines exists in the main activity and it has a specific text
      onView(withId(R.id.usernameTextView)).check(matches(withText("AbdalQader's tasks")));
  }

```

But what if the view that needs to be tested needs some time to be displayed?

Espresso framework will wait until the following synchronization conditions are met:

* The message queue is empty.
* There are no instances of AsyncTask currently executing a task. (if you have a thread that fetching data from an API for example, the test will not start until this thread finishes its working in the background)
* All developer-defined idling resources are idle.

Espresso comes with GUI to make the tests

Under the `Run` menu in android studio, you find an option called `Record Espresso Test`, this option lets you add tests while using the application, it allows you to add assertions, checks and performing some tests.

But the Record Espresso Test is limited, so if you might need to add some of the tests manually.
