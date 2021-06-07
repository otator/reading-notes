# Location

One of Google play sevices  APIs is the location, you can use this api to get the last known location.

to start, first add google play location service dependency in `gradle.build` 

```java
  implementation 'com.google.android.gms:play-services-location:18.0.0'
```

to get the location, you must add the permission of reading permissions in the `Manifest.xml` file:

```xml
  <manifest>
  <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
  <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
  <manifest>
```

since you can't get user's location without his permission, so you need to ask for the permission in the run time to do so, do the following:

* check if the permission is already granted
* if the permission is not granted, show the user a dialog to grant or reject the permission at run time

  ```java
  if (ContextCompat.checkSelfPermission(this, Manifest.permission.ACCESS_FINE_LOCATION) == PackageManager.PERMISSION_GRANTED){
    // get the location here
  }else{
    // the permissions that the user needs to grant or reject
    // Note: you may ask for coarse location as well
    String[] permissions = {Manifest.Manifest.permission.ACCESS_FINE_LOCATION, 1};
    ActivityCompat.requestPermission(this, permissions);
    // check if the user granted the permission
    if(ContextCompat.checkSelfPermission(this, permissions[0]) == PackageManager.PERMISSION_GRANTED)){
      //TODO: get the location here
    }
  }
  ```


Create location services client

```java
  private FusedLocationProviderClient fusedLocationClient;

// ..

@Override
protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}
```

Get the latest know location using `getLastLocation()` method

```java
  fusedLocationClient.getLastLocation()
        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });
```

you need to check if the location is null be cause this may happen in the following scenarios:
* location turned off in the device
* if it has not recorded a location(new device, or after factory reset)
* if the service restarted, and did not called yet.

sometimes you may need the best estimation of the location, do so by apply the following: 

* Check whether the location retrieved is significantly newer than the previously fetched location.
* Check whether the accuracy claimed by the location is better or worse than that of the previous estimate.
* Check the provider that's associated with the new location. Decide whether you trust this provider more than the one used in your app's cached location.
