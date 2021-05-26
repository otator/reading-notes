# Android Tasks and the Back Stack

A task is simply a stack where activities are pushed into, once you open the application, the main activity is pushed to this task(back stack), if you navigate to another activity, the new activity is pushed to the top of the stack and whenever the back button is clicked it will pop the stack and bring back the first activity.

if another application is opened, the current application will be put in the background, and whenever the launcher icon of this application is clicked or the application was chosen from the opened applications menu it will put it back in the foreground.

<div style="display: flex; flex-wrap: wrap; margin: 100px 0 100px 0">
<p style="width: 30%">When the current activity starts another, the new activity is pushed on the top of the stack and takes focus. The previous activity remains in the stack, but is stopped. When an activity stops, the system retains the current state of its user interface. When the user presses the Back button, the current activity is popped from the top of the stack (the activity is destroyed) and the previous activity resumes (the previous state of its UI is restored). Activities in the stack are never rearranged, only pushed and popped from the stack—pushed onto the stack when started by the current activity and popped off when the user leaves it using the Back button. As such, the back stack operates as a "last in, first out" object structure. Figure 1 visualizes this behavior with a timeline showing the progress between activities along with the current back stack at each point in time. [link](https://developer.android.com/guide/components/activities/tasks-and-back-stack)</p>

<img src="https://developer.android.com/images/fundamentals/diagram_backstack.png">

</div>

<div style="display: flex; justify-content: space-between; flex-wrap: wrap; margin: 100px 0 100px 0">
<p style="width: 50%">Because the activities in the back stack are never rearranged, if your app allows users to start a particular activity from more than one activity, a new instance of that activity is created and pushed onto the stack (rather than bringing any previous instance of the activity to the top). As such, one activity in your app might be instantiated multiple times (even from different tasks), as shown in figure 3. As such, if the user navigates backward using the Back button, each instance of the activity is revealed in the order they were opened (each with their own UI state). However, you can modify this behavior if you do not want an activity to be instantiated more than once. How to do so is discussed in the later section about Managing Tasks.</p>
<img src="https://developer.android.com/images/fundamentals/diagram_multiple_instances.png">

</div>




To open an activity in your application use Intent as shown in the code below:

```java 
   Intent intent = new Intent(CurrentActivity.this, OtherActivity.class);
   startActivity(intent);
```

you can use `putExtra()` and `getExtras()` to transfer data between activities.




# Android Shared Preferences

android platform offers a simple way to save small key-value data which is shared preferences

to use shared preferences in your application, create an object of it and pass it the context(the activity).

```java
 SharedPreferences sharedPreferences = PreferenceManager.getDefaultSharedPreferences(this);
 SharedPreferences.Editor editor = sharedPreferences.edit();
```

now the shared preference is ready to pass it key-value data 

```java
   editor.putString("name", "AbdalQader");
```

to read the data from the shared preference, use the `getString()` and pass it the key and the default value in order to use if the key is not found.

```java
 SharedPreferences sharedPreferences = PreferenceManager.getDefaultSharedPreferences(this);
 String name = sharedPreferences.getString("name", "No name");
```



