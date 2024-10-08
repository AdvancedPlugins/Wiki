# Implementing API

The API must be implemented through a local JAR file at the moment. There is no external repository. Here are two ways of doing so:

Implementing using Gradle:

```
dependencies {
    compileOnly files('path/to/file.jar')
}
```

You may also want to read:

* [Developer API - Creating Your Own Quest Types](developer-api-creating-your-own-quest-types.md)
* [Developer API - General API Methods](developer-api-general-api-methods.md)
