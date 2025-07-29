- This creates:
hello-lib/
├── pom.xml
└── src/
    ├── main/
    │   └── java/com/example/hello/App.java
    └── test/
        └── java/com/example/hello/AppTest.java

```bash
mvn archetype:generate -DgroupId=com.example.hello  -DartifactId=hello-lib  -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

- It compiles the project and creates a JAR file: target/hello-lib-1.0-SNAPSHOT.jar
```bash
mvn clean package
```

- This installs it to your local .m2 repository: ~/.m2/repository/com/example/hello/hello-lib/1.0-SNAPSHOT/
```bash
mvn install
```

- Add this to the pom.xml of another project:
```xml
<dependency>
  <groupId>com.example.hello</groupId>
  <artifactId>hello-lib</artifactId>
  <version>1.0-SNAPSHOT</version>
</dependency>
```