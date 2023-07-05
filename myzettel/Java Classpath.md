---
template: note
parent: [[Java]]
tags: 
aliases: []
source: 
---
![tp.web.random_picture](https://images.unsplash.com/photo-1532450786476-9101e8007628?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=300&ixid=MnwxfDB8MXxyYW5kb218MHx8dHJlZSxsYW5kc2NhcGUsd2F0ZXIsbW91bnRhaW58fHx8fHwxNjU4ODMwMjIz&ixlib=rb-1.2.1&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=900)

(date:: 2022-07-26) | (time:: 15:40) | (weather:: Vadodara: 🌦   +31°C →16km/h)

# Java Classpath
- The `PATH` and `CLASSPATH` are the two most important **environment variables** of the Java environment which are used to find the JDK binaries.
- The most common cause of dreaded error like `java.lang.NoClassDefFoundError` and `java.lang.ClassNotFoundException` is either incorrect or misconfigured `CLASSPATH` in Java.
- `PATH` is an environment variable that is used to locate [[Java Development Kit(JDK)|JDK]] binaries like the `java` or `javac`.
- `CLASSPATH`, an environment variable is used by System or Application [[ClassLoader]] to locate and load compile Java bytecodes stored in the `.class` file.
- In order to set `PATH` in Java, you need to include the `JDK_HOME/bin` directory in the `PATH` environment variable.
- In order to set `CLASSPATH` in Java, you need to include all those directories where you have put either your `.class` file or JAR file which is required by your Java application.
- `PATH` can not be overridden by any Java settings
- `CLASSPATH` can be overridden by providing the command-line option `-classpath` or `-cp` to both `java` and `javac` commands or by using the `Class-Path` attribute in the `Manifest` file inside the JAR archive.
- The `PATH` environment variable is used by the operating system to find any binary or command typed in the shell, this is true for both Windows and Linux environments while `CLASSPATH` is only used by Java ClassLoaders to load class files.


## 📚 References
- https://stackoverflow.com/questions/2396493/what-is-a-classpath-and-how-do-i-set-it
- https://www.java67.com/2012/08/what-is-path-and-classpath-in-java-difference.html


---
#### Internal Links
[[2022-07-26]], [[Java]]