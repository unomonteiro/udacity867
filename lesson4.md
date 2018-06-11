# Lesson 4 Advanced Android Builds

### feedback
#### 9. Quiz: Create an Android Library
I could not find anything was found on `build/outputs/aar`

### general notes


### 3. Library Overview
`jar` Java Library
- java general
- easy to move to android specific

`aar` Android Library
- Android Specific
- hard to move to `jar`

### 5. Multi-Project Builds
[Authoring Multi-Project Builds](https://docs.gradle.org/current/userguide/multi_project_builds.html)

### 6. Creating a Java Library
[4.01](4.01) exercise was already completed.
`sourceCompatibility = 1.7` on `app/build.gradle`

### 7. Quiz Create Java Libraries
Exercise [4.02](4.02)  
great hands on job exercise pushing skills a little bit further than previous  
step 9 is repeated twice!

### 9. Quiz: Create an Android Library
things changed

### 13. Wizard App signing
Exercise [4.05](4.05)  
See also [gradle signing plugin](https://docs.gradle.org/current/userguide/signing_plugin.html)  
[app-signing#secure-key](https://developer.android.com/studio/publish/app-signing#secure-key)

Right click on `app directory` and selected `"Open Module Settings"`

>[stackoverflow: get home path](https://stackoverflow.com/questions/20441609/referencing-the-users-home-directory-in-a-gradle-script?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)  
`def homePath = System.properties['user.home']`

### 14. Multidex Support
Exercise [4.07]()

`app/build.gradle:`
```
android {
    defaultConfig {
        multiDexEnabled true
```

### 15. Configuring Proguard
Exercise [4.08]() Proguard  

http://proguard.sourceforge.net/  
http://developer.android.com/tools/help/proguard.html  
http://tools.android.com/tech-docs/new-build-system/resource-shrinking  

Configuring proguard
4.08-Demo-ConfiguringProguard folder

18. Set up Android testing
4.10-Exercise-SetUpUnitTestingfolder

19. Congratulations
Links about more Gradle

5
.3 update the gradle wrapper
Change gradle wrapper from -bin to -all

.4 gradle versions plugin.
