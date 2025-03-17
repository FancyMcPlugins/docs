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

You can find the JavaDoc [here](https://repo.fancyplugins.de/javadoc/releases/de/oliver/FancyHolograms/latest)

## Create a new hologram

FancyHolograms offers builders to create new holograms. There is one builder for each hologram type.

Creating a text hologram with some modified attributes:

```java
Hologram hologram = TextHologramBuilder.create("MyTextHologram", new Location(Bukkit.getWorld("world"), 50, 100, 50))
    .text("<red>Hello World!</red>", "<green>How are you?</green>")
    .background(Color.ORANGE)
    .textShadow(true)
    .billboard(Display.Billboard.FIXED)
    .buildAndRegister();
```

This code will create the hologram and register it. By registering it to the HologramsRegistry, 
FancyHolograms will take care of the visibility (when to show or hide the hologram to players).  
If you want to control this by yourself, you can choose to only build and not register.

If you want to create an item or block hologram, simply use the builders for them:

```java
Hologram hologram = ItemHologramBuilder.create("MyItemHologram", new Location(Bukkit.getWorld("world"), 0, 111, 0))
    .item(new ItemStack(Material.DIAMOND))
    .buildAndRegister();
```

```java
Hologram hologram = BlockHologramBuilder.create("MyBlockHologram", new Location(Bukkit.getWorld("world"), 0, 235, 0))
    .block(Material.GOLD_BLOCK)
    .buildAndRegister();
```

## Modify an existing hologram

## The registry

## The controller

## Using FancyHolograms events

## Help about the API

<tip>
If you need help with the API, you can join our <a href="https://discord.gg/ZUgYCEJUEx">Discord</a> and ask in the #holograms-dev channel.
</tip>
