# API

## Including the API into your project

### Gradle

```gradle
repositories {
    maven("https://repo.fancyplugins.de/releases")
    ...
}
```

```gradle
dependencies {
    compileOnly("de.oliver:FancyHolograms:version")
    ...
}
```

### Maven

```maven
<repository>
    <id>fancyplugins-releases</id>
    <name>FancyPlugins Repository</name>
    <url>https://repo.fancyplugins.de/releases</url>
</repository>
```

```maven
<dependency>
    <groupId>de.oliver</groupId>
    <artifactId>FancyHolograms</artifactId>
    <version>VERSION</version>
</dependency>

```