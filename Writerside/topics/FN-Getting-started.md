# Getting started

## Installation

<procedure title="Download" type="choices">
    <p>You can download FancyNpcs at the following places:</p>
    <step><a href="https://modrinth.com/plugin/fancynpcs/versions">Modrinth</a></step>
    <step><a href="https://hangar.papermc.io/Oliver/FancyNpcs/versions">Hangar</a></step>
    <step><a href="https://github.com/FancyMcPlugins/FancyNpcs/releases">GitHub</a></step>
    <step><a href="https://jenkins.fancyplugins.de/job/FancyNpcs/">Development Builds</a></step>
</procedure>

<procedure title="Plugins folder">
    <p>Put the downloaded file into the plugins folder of your server.</p>
</procedure>

<warning>Be aware, that only Paper is supported, but the plugin should work on any of its forks (like <a href="https://github.com/PaperMC/Folia">Folia</a> or <a href="https://github.com/PurpurMC/Purpur">Purpur</a>). Spigot or Bukkit is not supported.</warning>

<procedure title="Restart server">
    <p>Restart your server.</p>
    <step>Run "/stop" in the server console.</step>
    <step>Start the server again.</step>
</procedure>

<procedure title="Checking plugin">
    <p>To make sure the plugin is loaded correctly, run the following command:</p>
    <step>/fancynpcs version</step>
    <step>It should output the version of the plugin.</step>
</procedure>

## Create your first NPC

<procedure title="Create NPC">
    <p>Run the following commands to create your first NPC:</p>
    <step>/npc create myNpc</step>
    <step>A npc with the name "myNpc" should appear.</step>
</procedure>

<procedure title="Modify NPCs display name">
    <p>Run the following command to modify the NPCs display name:</p>
    <step>/npc displayname myNpc New display name!</step>
    <step>The NPCs display name should now be "New display name".</step>
</procedure>

<procedure title="Move the NPC to you">
    <p>Run the following command to move the NPC to you:</p>
    <step>/npc move_here myNpc</step>
    <step>The NPC should now be at your location.</step>
</procedure>

<procedure title="Move the NPC to a specific location">
    <p>Run the following command to move the NPC to specific coordinates:</p>
    <step>/npc teleport myNpc 127 61 347</step>
    <step>The NPC should now be at the coordinates x=127 y=61 z=347</step>
</procedure>

<procedure title="Modify NPCs skin">
    <p>Run the following command to modify the NPCs skin:</p>
    <step>/npc skin myNpc Notch</step>
    <step>The NPCs skin should now be Notch's skin.</step>
</procedure>

<tip title="More commands.">You can find more commands in the <a href="FN-Commands.md">commands page</a>.</tip>