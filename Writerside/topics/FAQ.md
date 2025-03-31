# FAQ

> The documentation has been moved to [https://docs.fancyplugins.de/](https://docs.fancyplugins.de/)
> This documentation might be outdated and will not be updated anymore.
{style="warning"}

This faq contains answers to common questions about FancyPlugins.

## General

The following questions are valid for both FancyNpcs and FancyHolograms.

**How to use colors?**
- All fancy plugins do primary support [MiniMessages](https://docs.advntr.dev/minimessage/format.html)
- Official documentation: [https://docs.advntr.dev/minimessage/format.html](https://docs.advntr.dev/minimessage/format.html)
- Web-Viewer: [https://webui.advntr.dev/](https://webui.advntr.dev/)

**Is ViaVersion / ViaBackwards supported?**

- No ViaVersion and ViaBackwards are not supported
- FancyPlugins only supports the scenario, where the player client version is the server version
- Additionally, display entities and other features don't even exist on older Minecraft versions
- (generally ViaVersion / ViaBackwards should work, try to always use the latest version)

**Is bedrock edition / geyser supported?**

- No, only Minecraft Java edition is supported
- The plugin may not work properly with Geyser as it is not officially supported
- Additionally, display entities and other features don't even exist on Bedrock Edition

**Is Spigot supported?**

- No only Paper and Folia (a fork of Paper) is supported
- Paper has generally a better performance and gives us developers a better experience developing plugins

**I get a "UnsupportedClassVersionError" exception when starting the server**

- All fancy plugins require Java 21 or newer
- Make sure your server is running Java 21 or newer

**The plugin is not loading**

- Make sure to use the latest version of the plugin
- Make sure to use the latest build of Paper / Folia
- Make sure the Minecraft version is supported by the plugin

**Are there converters to convert npcs / holograms from other popular plugins?**

- Converters are currently not available for fancy plugins.
- You will need to manually convert your data

## FancyNpcs

**Official download pages and docs:**

- Documentation: [https://fancyplugins.de/docs/fancynpcs.html](https://fancyplugins.de/docs/fancynpcs.html)
- GitHub: [https://github.com/FancyMcPlugins/FancyNpcs](https://github.com/FancyMcPlugins/FancyNpcs)
- Modrinth: [https://modrinth.com/plugin/fancynpcs](https://modrinth.com/plugin/fancynpcs)
- Hangar: [https://hangar.papermc.io/Oliver/FancyNpcs](https://hangar.papermc.io/Oliver/FancyNpcs)

**Can npcs have multiple lines as displayname?**

- See [here](<https://fancyplugins.de/docs/fn-multiple-lines.html>) on how to make an NPC name have multiple lines.

**Does FancyNpcs support Shopkeepers?**

- There is no official integration or addon for Shopkeepers
- But you can use the "/shopkeeper remote" as console_command actions
- Example `/npc action MY_NPC any_click add console_command shopkeeper remote SHOPKEEPER_ID {player}`
- SHOPKEEPER_ID: the display name of the shopkeeper

## FancyHolograms

**Official download pages and docs:**

- Documentation: [https://fancyplugins.de/docs/fancyholograms.html](https://fancyplugins.de/docs/fancyholograms.html)
- GitHub: [https://github.com/FancyMcPlugins/FancyHolograms](https://github.com/FancyMcPlugins/FancyHolograms)
- Modrinth: [https://modrinth.com/plugin/fancyholograms](https://modrinth.com/plugin/fancyholograms)
- Hangar: [https://hangar.papermc.io/Oliver/FancyHolograms](https://hangar.papermc.io/Oliver/FancyHolograms)

**How to modify each line in a hologram?**

- Per-line settings (such as scale or background) are not supported in FancyHolograms due to a limitation with display entities
- A separate hologram will need to be created for each line

**How to add a blank line?**

- To add a blank line in a hologram, use `<r>` on a new line.

**How to make holograms clickable?**

- Holograms currently aren't clickable themselves, but [here's](<https://fancyplugins.de/docs/fh-clickable-holograms.html>) a workaround

**How to make the hologram not to rotate?**

- To make a hologram not rotate, the billboarding must be set to FIXED
- Example: `/holo edit <hologram> billboard FIXED`
- Once complete, you must set the hologram's rotation with the `rotate` and `rotatepitch` commands

**How to edit the holograms via the data file?**

1. Run `/fancyholograms save`
2. Back up the `holograms.yml` file in case something goes wrong
3. Edit your `holograms.yml` file as desired
4. Run `/fancyholograms reload` after saving the file