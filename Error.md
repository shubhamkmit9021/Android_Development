# when create a new project and run it then getting error in this

## Solution is compileSdk 33 to compileSdk 34
```
android {
    namespace 'com.shubhamkmit.myapplication'
    compileSdk 33    ---> increase this value like compileSdk 34

    defaultConfig {
        applicationId "com.shubhamkmit.myapplication"
        minSdk 16
        targetSdk 33
        versionCode 1
        versionName "1.0"

        testInstrumentationRunner "androidx.test.runner.AndroidJUnitRunner"
    }
```
**This is the issue getting**
```
An issue was found when checking AAR metadata:

  1.  Dependency 'androidx.activity:activity:1.8.0' requires libraries and applications that
      depend on it to compile against version 34 or later of the
      Android APIs.

      :app is currently compiled against android-33.

      Also, the maximum recommended compile SDK version for Android Gradle
      plugin 7.4.2 is 33.

      Recommended action: Update this project's version of the Android Gradle
      plugin to one that supports 34, then update this project to use
      compileSdkVerion of at least 34.

      Note that updating a library or application's compileSdkVersion (which
      allows newer APIs to be used) can be done separately from updating
      targetSdkVersion (which opts the app in to new runtime behavior) and
      minSdkVersion (which determines which devices the app can be installed
      on).
```


# Getting Error During Development

### Duplicate class error
````
 Duplicate class androidx.lifecycle.ViewModelLazy found in modules lifecycle-viewmodel-2.4.0-runtime (androidx.lifecycle:lifecycle-viewmodel:2.4.0) and lifecycle-viewmodel-ktx-2.3.1-runtime (androidx.lifecycle:lifecycle-viewmodel-ktx:2.3.1)

Add below dependency
In Gradle Scripts file -> build.gradle (Module:app) -> dependencies -> 

def lifecycle_version = "2.4.0"
implementation "androidx.lifecycle:lifecycle-viewmodel:$lifecycle_version"
implementation "androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version"

````
