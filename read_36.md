# Cognito

to add amplify to the android app its dependencies in the `gradle.build` file

```java
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.17.4'
}
```

run the following command from the console to start provisioning auth resources in the backend

`amplify add auth`

add the following when it prompts:

? Do you want to use the default authentication and security configuration?

  `Default configuration`

? How do you want users to be able to sign in?

  `Username`

? Do you want to configure advanced settings?

  `No, I am done.`


to push the changes you done to the cloud, execute the following command

`amplify push`

add the plugins using the following code before start the configuration

```java
  // Add this line, to include the Auth plugin.
  Amplify.addPlugin(new AWSCognitoAuthPlugin());
  Amplify.configure(getApplicationContext());
```


check the current session using the following code:

```java
  Amplify.Auth.fetchAuthSession(
      result -> Log.i("AmplifyQuickstart", result.toString()),
      error -> Log.e("AmplifyQuickstart", error.toString())
  );
```