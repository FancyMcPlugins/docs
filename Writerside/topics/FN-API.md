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
    compileOnly("de.oliver:FancyNpcs:version")
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
    <artifactId>FancyNpcs</artifactId>
    <version>VERSION</version>
    <scope>provided</scope>
</dependency>

```

## JavaDoc

You can find the JavaDoc [here](https://repo.fancyplugins.de/javadoc/releases/de/oliver/FancyNpcs/latest)

## List of all events

### NpcCreateEvent

Is fired when a new NPC is being created

### NpcRemoveEvent

Is fired when a NPC is being removed

### NpcSpawnEvent

Is fired when a NPC is being spawned

### NpcModifyEvent

Is fired when a NPC is being modified

### NpcInteractEvent

Is fired when a player interacts with a NPC

### NpcStartLookingEvent

Is fired when NPC starts looking at a player

### NpcStopLookingEvent

Is fired when NPC stops looking at a player

## Creating a NPC

```java
NpcData data = new NpcData("myNpc", creatorUUID, location);
data.setSkin("OliverHD"); // use skin of the player OliverHD
data.setDisplayName("<red>cool displayname</red>");

Npc npc = FancyNpcsPlugin.get().getNpcAdapter().apply(data);
FancyNpcsPlugin.get().getNpcManager().registerNpc(npc);
npc.create();
npc.spawnForAll();
```

## Modify a NPC

```java
Npc npc = FancyNpcsPlugin.get().getNpcManager().getNpc("myNpc");
npc.getData().setDisplayName("New cool display name");

npc.updateForAll();

// for some modifications you need to respawn the npc
npc.removeForAll();
npc.spawnForAll();
```

## Remove a NPC

```java
Npc npc = FancyNpcsPlugin.get().getNpcManager().getNpc("myNpc");
npc.removeForAll();

FancyNpcsPlugin.get().getNpcManager().removeNpc(npc);
```

## Help about the API

<tip>
If you need help with the API, you can join our <a href="https://discord.gg/ZUgYCEJUEx">Discord</a> and ask in the #npcs-dev channel.
</tip>

