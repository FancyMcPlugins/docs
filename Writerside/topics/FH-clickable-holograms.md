# Clickable holograms

> The documentation has been moved to [https://docs.fancyplugins.de/](https://docs.fancyplugins.de/)
> This documentation might be outdated and will not be updated anymore.
{style="warning"}

Interactions with holograms is not a feature of FancyHolograms yet, but there is a workaround for this.

1. Create your hologram with the text you want.
2. Install [FancyNpcs](https://fancyplugins.de/FancyNpcs/download/)
3. Create a new npc and set the type to "INTERACTION" (`/npc type (npc name) INTERACTION`)
4. Remove the name tag of the npc (`/npc displayName (npc name) <empty>`)
5. Position the npc to the same location as the hologram (press F3+B to see the hitbox)
6. Modify the size of the hitbox to fit the hologram (`/npc attributes (npc name) (width/height) (size)`)
7. Add an interaction action to the
   npc ([message, playerCommand, serverCommand](https://fancyplugins.de/docs/fn-commands.html#message))