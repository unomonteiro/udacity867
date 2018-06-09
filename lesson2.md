# lesson 2

### feedback
2\. and 3. repeated links for gradle plugins lessons 2. and 3.

9\. Quiz: Java Task Dependencies
it's not clear where to find a relation from assemble and executed classes
however executing: gradle assemble -i
we can actually see which tasks are executed or even up-to-date

14\. Declaring Dependencies  
compile is deprecated

### notes
`apply plugin: 'java'`  
[Using Gradle Plugins](https://docs.gradle.org/current/userguide/plugins.html)  

### 5. Applying the Java Plugin
no windows commands!

- https://guides.gradle.org/performance/  
- https://docs.gradle.org/current/userguide/userguide.html#getting-started  
[Improving the Performance of Gradle Builds](https://guides.gradle.org/performance/)  

### 7. Conventions and Configuration  
- [Gradle user guide](https://docs.gradle.org/current/userguide/java_plugin.html#N11FD1)  
- [Java base plugin](https://docs.gradle.org/current/userguide/standard_plugins.html#N11F3E)  
- [Gradle DSL reference](https://docs.gradle.org/current/dsl/org.gradle.api.tasks.SourceSet.html)  

### 8. Java Plugin Documentation  
- [Java quick start guide](https://docs.gradle.org/current/userguide/tutorial_java_projects.html)  
- [*The Java Plugin*](https://docs.gradle.org/current/userguide/java_plugin.html)  

### 10. Quiz: Configure the Java Plugin
- [Gradle DSL - jar](https://docs.gradle.org/current/dsl/org.gradle.api.tasks.bundling.Jar.html)  

### 11. Dependency Management
- [Dependency Management](https://docs.gradle.org/current/userguide/introduction_dependency_management.html#gsc.tab=0)  
- [scans.gradle.com](https://scans.gradle.com/)  

Most popular repositories:
**mavenCentral()** and **jcenter()**.

### 13. Working with Repositories
- [2.04](2.04-Demo-WorkingWithRepositories/build.gradle)  
- [Dependency Management for Java Projects
](https://docs.gradle.org/current/userguide/dependency_management_for_java_projects.html)  
- [Full article Dependency Management](https://docs.gradle.org/current/userguide/introduction_dependency_management.html)

### 14. Declaring Dependencies
now that we configured our  `Repositories` we can define `Dependencies` on `Artifacts` contained in those repositories.

`External module Dependencies`: Dependencies that resolve from repositories

Dependencies are assigned to configurations/ groups of related dependencies

dependencies are added to implementation configuration
```
dependencies {
    compile 'com.google.guava:18.0'
}
```
`'com.google.guava:18.0'` -  dependency notation  
that we add to  
`compile` name of the configuration

- [DependencyHandler](https://docs.gradle.org/current/dsl/org.gradle.api.artifacts.dsl.DependencyHandler.html)

### 15. Declare Dependencies
- [2.06](2.06-Exercise-DeclareARepositoryAndDependencies/build.gradle)  
```
task printDependencies {
    doLast {
        configurations.compile.each {
            println it.name
        }
    }
}
```  
`$ gradle printDependencies`  
`$ gradle dependencyInsight --dependency commons-logging`

### 17. Configurations
[2.08]()

### 18 Quiz: Create a Custom Configuration
- [Create custom configuration](https://docs.gradle.org/current/dsl/org.gradle.api.artifacts.Configuration.html)

### 20. Java Unit Testing
- [the java plugin - testing](https://docs.gradle.org/current/userguide/java_plugin.html#sec:java_test)  
- [tests report: build/reports/tests/test/classes/*.html ](build/reports/tests/test/classes/com.udacity.gradle.test.PersonTest.html)

### 22. Finding Gradle plugins
- [Gradle user guide Gradle plugins](https://docs.gradle.org/current/userguide/standard_plugins.html)  
- [Plugin Portal](https://plugins.gradle.org/)  

### 23. Advanced Gradle Wrapper
- [Gradle Wrapper chapter of the Gradle user guide](https://docs.gradle.org/current/userguide/gradle_wrapper.html)  
