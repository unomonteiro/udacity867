# gradle for Android

### feedback
#### 5. Quiz: Import a Java Project
the solution doesn't actually say how we get there.
If we open the documentation, at [Tasks](https://docs.gradle.org/current/userguide/application_plugin.html#sec:application_tasks) we will actually find that `run`  depends only on `classes` which confused me even more.
On the other side inside the Gradle toolbar, executing Tasks\application\run we can actually confirm the solution for the Quiz on the run log
```
[time_stamp]: Executing task 'run'...

Executing tasks: [run]

Configuration on demand is an incubating feature.
:compileJava
:processResources NO-SOURCE
:classes
:run FAILED
```
#### 9. Quiz: Android Plugin Functionality
>You can find the more detailed Android Gradle plugin user guide here.  

The link is deprecated and repeated on point 10.

### 12. Configuring Build Types
Quiz and exercise 3.05 don't match  
Quiz is to disable debug and exercise 3.05 is to configure applicationIdSuffix.

### general notes
`apply plugin: 'java'`

DAC - [developer.android.com](developer.android.com)

### 4. Importing Gradle Projects
`$ chmod +x gradlew` we might need to add execution permission.

### 5. Quiz: Import a Java Project
```
apply plugin: 'java'
apply plugin: 'application'
```

### 7. Android Build Scripts
[3.03-Demo](../3.03-Demo-TheDefaultAndroidBuildScripts)

`apply plugin: 'com.android.application'` fetched from jcenter.  
`compileSdkVersion` and - `buildToolsVersion` are essential.  
`defaultConfig` block configures attributes of the
Android Manifest.  
`dependencies` this declares compile time
dependencies on every JAR in the `libs` directory, and on the Android support
library

### 8. Android Gradle Plugin Update
[migration to Android Gradle Plugin 3.0.0](https://developer.android.com/studio/build/gradle-plugin-3-0-0-migration.html)  
>The specified Android SDK Build Tools version (23.0.2) is ignored, as it is below the minimum supported version (25.0.0) for Android Gradle Plugin 3.0.0-beta4.
>
>Android SDK Build Tools 26.0.0 will be used.
>
>To suppress this warning, remove "buildToolsVersion '23.0.2'" from your build.gradle file, as each version of the Android Gradle Plugin now has a default version of the build tools.  

**Solution**: Update the buildToolsVersion to the minimum required by the Android Gradle Plugin or later. Alternatively, click on `Update Build Tools` to let Android Studio update it for you.

>All flavors must now belong to a named flavor dimension.

**Solution**: [Add dimensions to build.gradle](https://developer.android.com/studio/build/gradle-plugin-3-0-0-migration.html?utm_source=android-studio#variant_aware)  

>Failed to resolve: com.android.support:appcompat-v7:26.0.1

**Solution**:  [Add Google maven repository](https://developer.android.com/studio/build/gradle-plugin-3-0-0-migration.html?utm_source=android-studio#apply_plugin). Alternatively, click on `Install Repository and sync project` to let Android Studio update it for you.

>Execution failed for task ':app:processFreeDebugManifest'. > Manifest merger failed : uses-sdk:minSdkVersion 10 cannot be smaller than version 14 declared in library [com.android.support:appcompat-v7:26.0.1] /Users/user/.gradle/caches/transforms-1/files-1.1/appcompat-v7-26.0.1.aar/dab71...cddc/AndroidManifest.xml as the library might be using APIs not available in 10 Suggestion: use a compatible library with a minSdk of at most 10, or increase this project's minSdk version to at least 14, or use tools:overrideLibrary="android.support.v7.appcompat" to force usage (may lead to runtime failures)  

**Solution**: Update minSDK to 14 or higher. Note that targeting API 26 is not compatible with supporting SDK versions lower than 14.

### 9. Quiz: Android Plugin Functionality
[Configure your build](https://developer.android.com/studio/build/)  

### 10. Build Types, Flavors, and Variants
![Build Types, Product Flavors, and Variants](notes\build-variants.png)

### 11. Configuring Build Types
Gradle toolbar  
Build Variants toolbar

### 12. Configuring Build Types
```
/*
To use our solution, uncomment the following line.
*/

// apply from:"solution.gradle"
```
