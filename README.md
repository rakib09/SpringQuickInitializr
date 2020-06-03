# SpringQuickInitializr
Spring Quick Initializr

This repository configures a Spring Initializr instance with a custom UI running at https://start.spring.io.

##### Building from Source
You need Java 1.8 and a bash-like shell.


##### Custom Dependency
```
- name: Custom Tools
      content:
        - name: Greetings Framework
          id: custom-module
          groupId: com.extremecoder
          artifactId: custom-modules
          version: 1.0-SNAPSHOT
          description: Greeting Modules
          repository: custom-module-repo
          links:
            - rel: source
              href: https://github.com/rakib09/custom-module
              description: The open-source code repository on GitHub
  env:
    repositories:
      custom-module-repo:
        name: custom-module
        url: https://github.com/rakib09/custom-module
```

##### Building
Invoke the build at the root of the project


```
$ ./mvnw clean install 
```

After running application we can create a project using intelijj.
![project creation](files/Spring_Quick_Initializer.png)

Dependency selection
![Dependency](files/dependancy_selection.png)

##### Created sample project
https://github.com/rakib09/spring-boot-app


##### Reference: 
[spring.io](https://docs.spring.io/initializr/docs/current/reference/html/)
