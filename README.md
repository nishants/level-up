



# About Gradle

- build tool for java
- general purpose buid tool
- supports maven and ivy dependencies
- uses acyclic directed graph representation of tasks, and exectes a path
- so any build can be defined as such graph



**Gradle build scripts**

- build scripts in three phases 
  - **Initialization**
    - setup of build environment
    - select project to take part in it
  - **Configuration**
    - constcuts the task graph for the build
    - hence find which taks and there order to run  
  - **Execution**
    - Runs the selected tasks

Customising and extending gradle 
- we can use plenty of **existing plugins** from maven centra, or
- we can **create our own task type**
- source file for custom task should be kept in **buildSrc directory**
- we can add custom task logic, using fucntions **Task.doFirst() and task.doLast()**
- **Define custom conventions**

Configure for JUNIT
```
apply plugin: 'java'

repositories {
    mavenCentral()
}

dependencies {
    testCompile('org.junit.jupiter:junit-jupiter-api:5.4.0')
    testRuntime('org.junit.jupiter:junit-jupiter-engine:5.4.0')
}
```




**Search dependecies path**

- Dependencies: <https://search.maven.org/artifact/org.hibernate/hibernate-core/3.6.7.Final/jar>

- Plugins <https://plugins.gradle.org/>
