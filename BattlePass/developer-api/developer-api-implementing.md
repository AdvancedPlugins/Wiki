# Implementing API

The API must be implemented through a local JAR file at the moment. There is no external repository. Here are two ways of doing so:

## Implementing using Gradle:

```gradle
dependencies {
    compileOnly files('path/to/file.jar')
}
```

## Implementing using Maven

```xml
<dependencies>
    <dependency>
        <groupId>io.github.battlepass</groupId>
        <artifactId>BattlePass</artifactId>
        <version>LATEST</version>
        <scope>system</scope>
        <systemPath>${project.basedir}/path/to/file.jar</systemPath>
    </dependency>
</dependencies>
```

---

You may also want to read:

* [Developer API - Creating Your Own Quest Types](developer-api-creating-your-own-quest-types.md)
* [Developer API - General API Methods](developer-api-general-api-methods.md)
