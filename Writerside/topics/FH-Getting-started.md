# Getting started

## Installation

<procedure title="Download" type="choices">
    <p>You can download FancyHolograms at the following places:</p>
    <step><a href="https://modrinth.com/plugin/fancyholograms/versions">Modrinth</a></step>
    <step><a href="https://hangar.papermc.io/Oliver/FancyHolograms/versions">Hangar</a></step>
    <step><a href="https://github.com/FancyMcPlugins/FancyHolograms/releases">GitHub</a></step>
    <step><a href="https://jenkins.fancyplugins.de/job/FancyHolograms/">Development Builds</a></step>
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
    <step>/fancyholograms version</step>
    <step>It should output the version of the plugin.</step>
</procedure>

## Create your first hologram

<procedure title="Create text hologram">
    <p>Run the following commands to create your first hologram:</p>
    <step>/hologram create text myHologram</step>
    <step>A hologram with the name "myHologram" should appear.</step>
</procedure>

<procedure title="Modify hologram text">
    <p>Run the following command to modify the hologram text:</p>
    <step>/hologram edit myHologram addLine this is the second line</step>
    <step>A second line should appear with the text "this is the second line"</step>
    <step>Set the text of a line with: /hologram edit myHologram setLine 1 first line</step>
    <step>The first line should now have the text "first line"</step>
    <step>Remove a line with: /hologram edit myHologram removeLine 2</step>
    <step>The second line should now be removed.</step>
</procedure>

<procedure title="Move the hologram to you">
    <p>Run the following command to move the hologram to you:</p>
    <step>/hologram edit myHologram moveHere</step>
    <step>The hologram should now be at your location.</step>
</procedure>

<procedure title="Move the hologram to a specific location">
    <p>Run the following command to move the hologram to specific coordinates:</p>
    <step>/hologram edit myHologram moveTo 127 61 347</step>
    <step>The hologram should now be at the coordinates x=127 y=61 z=347</step>
</procedure>

<procedure title="Modify hologram background">
    <p>Run the following command to modify the hologram background:</p>
    <step>/hologram edit myHologram background green</step>
    <step>The hologram background should now be green.</step>
</procedure>

<tip title="More commands.">You can find more commands in the <a href="FH-Commands.md">commands page</a>.</tip>