# API

## Including the API into your project

### Gradle

```Kotlin
repositories {
    maven("https://repo.fancyplugins.de/releases")
    ...
}
```

```Kotlin
dependencies {
    compileOnly("de.oliver:FancyHolograms:version")
    ...
}
```

### Maven

```Markup
<repository>
    <id>fancyplugins-releases</id>
    <name>FancyPlugins Repository</name>
    <url>https://repo.fancyplugins.de/releases</url>
</repository>
```

```Markup
<dependency>
    <groupId>de.oliver</groupId>
    <artifactId>FancyHolograms</artifactId>
    <version>VERSION</version>
    <scope>provided</scope>
</dependency>
```

## JavaDoc

You can find the JavaDoc [here](https://fancyplugins.de/javadocs/fancyholograms/)

## Create a new hologram

```java
HologramManager manager = FancyHologramsPlugin.get().getHologramManager();

TextHologramData hologramData = new TextHologramData("hologram_name", location); // or create BlockHologramData / ItemHologramData
// Adjust the Hologram Data (Optional)
hologramData.setBackground(TextColor.color(100, 255, 79));
hologramData.setBillboard(Display.Billboard.FIXED);

Hologram hologram = manager.create(data);

// Register the hologram to the HologramManager (FancyHolograms will display, save and load the hologram)
// Use HologramData#setPersistent to stop the hologram from being saved
manager.addHologram(hologram); 
```

## Modify an existing hologram

```java
HologramManager manager = FancyHologramsPlugin.get().getHologramManager();

Hologram hologram = manager.getHologram("hologram_name").orElse(null);
if (hologram == null) {
    // hologram not found
    return;
}

HologramData hologramData = hologram.getData();
hologramData.setBillboard(Display.Billboard.CENTER);

if (hologramData instanceof TextHologramData textData) {
    textData.setTextAlignment(TextDisplay.TextAlignment.LEFT);
}
```

## Help about the API

<tip>
If you need help with the API, you can join our <a href="https://discord.gg/ZUgYCEJUEx">Discord</a> and ask in the #holograms-dev channel.
</tip>
