# Android Tasks and the Back Stack

A task is simply a stack where where activities are pushed into, once you open the application, the main activity is push to this task(back stack), if you navigate to another activity, the new activity is pushed to the top of the stack and whenever the back button is clicked it will pop the stack and bring back the first activity.

if another application is open the current application will be in the background, and when ever the luncher icon of this application is clicked or the application chosen from the open applications menu it will put back in the foreground.

To open an activity in your application use Intent as shown in the code below:

```java 
   Intent intent = new Intent(CurrentActivity.this, OtherActivity.class);
   startActivity(intent);
```

you can use `putExtra()` and `getExtras()` to transfere data between activites.




# Android Shared Preferences

android platform offers a simple way to save small key-value data which is shared preferences

to use shared preferences in your application, create an object of it and pass it the context(the activity).

```java
 SharedPreferences sharedPreferences = PreferenceManager.getDefaultSharedPreferences(this);
 SharedPreferences.Editor editor = sharedPreferences.edit();
```

now the shared prefernece is ready to pass it key-value data 

```java
   editor.putString("name", "AbdalQader");
```

to read the data from the shared preference, use the `getString()` and pass it the key and the default value in order to use if the key is not found.

```java
 SharedPreferences sharedPreferences = PreferenceManager.getDefaultSharedPreferences(this);
 String name = sharedPreferences.getString("name", "No name");
```



