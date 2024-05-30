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

DisplayHologramData displayData = DisplayHologramData.getDefault(location);
displayData.setBillboard(Display.Billboard.FIXED);
// set more general data here

TextHologramData textData = TextHologramData.getDefault("hologram_name"); // or create BlockHologramData / ItemHologramData
textData.setBackground(TextColor.color(100, 255, 79));
// set more type-specific data here

HologramData data = new HologramData("hologram_name", displayData, HologramType.TEXT, textData);
Hologram hologram = manager.create(data);

manager.addHologram(hologram); // registers the hologram (FancyHolograms will save and load it)

hologram.createHologram();
hologram.showHologram(Bukkit.getOnlinePlayers());
```

## Modify an existing hologram

```java
HologramManager manager = FancyHologramsPlugin.get().getHologramManager();

Hologram holo = manager.getHologram("hologram_name").orElse(null);
if (holo == null) {
    // hologram not found
    return;
}

holo.getData().getDisplayData().setBillboard(Display.Billboard.CENTER);

if (holo.getData().getTypeData() instanceof TextHologramData textData) {
    textData.setTextAlignment(TextDisplay.TextAlignment.LEFT);
}

// apply the changes
holo.updateHologram();

// refresh the hologram for all players
holo.refreshHologram(Bukkit.getOnlinePlayers());

// if refreshing did not work, try to respawn the hologram
holo.hideHologram(Bukkit.getOnlinePlayers());
holo.showHologram(Bukkit.getOnlinePlayers());
```

## Help about the API

<tip>
If you need help with the API, you can join our <a href="https://discord.gg/ZUgYCEJUEx">Discord</a> and ask in the #holograms-dev channel.
</tip>
