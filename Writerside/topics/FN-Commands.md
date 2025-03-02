# Commands

This page provides detailed information about the various commands available in FancyNpcs, allowing you to make the
most out of its features.

### Commands for /fancynpcs

### `/fancynpcs feature_flags`

- **Syntax**:  `/fancynpcs feature_flags`
- **Permissions**: `fancynpcs.command.fancynpcs.feature_flags`

### `/fancynpcs reload`

- **Syntax**:  `/fancynpcs reload`
- **Permissions**: `fancynpcs.command.fancynpcs.reload`

### `/fancynpcs save`

- **Syntax**:  `/fancynpcs save`
- **Permissions**: `fancynpcs.command.fancynpcs.save`

### `/fancynpcs version`

- **Syntax**:  `/fancynpcs version`
- **Permissions**: `fancynpcs.command.fancynpcs.version`

### Commadns for /npc

### `/npc attribute`

Sets an attribute of the NPC.

- **Syntax**:  `/npc attribute (npc) (set | list)`
- **Permissions**: `fancynpcs.command.npc.attribute.(sub)`

### `/npc collidable`

Changes whether the NPC can collide with other entities.

- **Syntax**:  `/npc collidable (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.collidable`

### `/npc copy`

Copies (duplicates) specified NPC.

- **Syntax**: `/npc copy (npc) (new_name)`
- **Permissions**: `fancynpcs.command.npc.copy`
- Name check is now more strict and only allows `A-Z a-z 0-9 _ - /` characters.

### `/npc create`

Creates a new NPC. Can be customized with flags.

- **Syntax**: `/npc create (name) [--position (x y z)] [--world (world)] [--type (type)]`
- **Permissions**: `fancynpcs.command.npc.create`
- Name check is now more strict and only allows `A-Z a-z 0-9 _ - /` characters.

### `/npc displayname`

Changes displayname of the NPC. Supports MiniMessage, PlaceholderAPI and MiniPlaceholders.

- **Syntax**:  `/npc displayname (npc) (@none | name)`
- **Permissions**: `fancynpcs.command.npc.displayname`
- Empty message placeholder is `@none`

### `/npc equipment`

``set`` - Sets equipment slot of the NPC to item currently held in main hand, none or a specific item type.

``clear`` - Clears equipment slot of the NPC.

``list`` - Lists all equipment slots of the NPC.

- **Syntax**: `/npc equipment (npc) (set | clear | list)`
- **Permissions**: `fancynpcs.command.npc.equipment.(sub)`
- Accepts either `@none`, `@hand` or valid item type as an argument.

### `/npc fix`

Fixes the NPC if it's not working properly.

(Currently it's only respawning the NPC)

- **Syntax**:  `/npc fix (npc)`
- **Permissions**: `fancynpcs.command.npc.fix`

### `/npc glowing`

Changes glowing state and color of the NPC.

- **Syntax**:  `/npc glowing (npc) [disabled | color]`
- **Permissions**: `fancynpcs.command.npc.glowing`

### `/npc help`

Shows help about all commands.

- **Syntax**:  `/npc help [page]`
- **Permissions**: `fancynpcs.command.npc.help`

### `/npc info`

Shows information about specified NPC.

- **Syntax**:  `/npc info (npc)`
- **Permissions**: `fancynpcs.command.npc.info`

### `/npc interaction_cooldown`

Changes duration between interactions (cooldown) of the NPC.

- **Syntax**:  `/npc interaction_cooldown (npc) (disabled | cooldown)`
- **Permissions**: `fancynpcs.command.npc.interaction_cooldown`
- Formerly known as `/npc interactionCooldown`.
- Uses time duration instead of a number of seconds eg. `2min`. Supported units:
    - milliseconds: `ms`
    - seconds: `s`
    - minutes: `min`
    - hours: `h`
    - days: `d`
    - months: `mo`
    - years: `y`

### `/npc list`

Lists all NPCs in all worlds. Can be filtered and sorted.

- **Syntax**:  `/npc list [--type (type)] [--sort (sort)]`
- **Permissions**: `fancynpcs.command.npc.list`

### `/npc move_here`

Teleports specified NPC to your location.

- **Syntax**:  `/npc move_here (npc)`
- **Permissions**: `fancynpcs.command.npc.move_to`

### `/npc move_to`

Teleports NPC to specified location.

- **Syntax**:  `/npc move_to (npc) (x) (y) (z) [world] [--look-in-my-direction]`
- **Permissions**: `fancynpcs.command.npc.move_to`

### `/npc nearby`

Lists all NPCs in your world. Can be filtered and sorted.

- **Syntax**:  `/npc nearby [--radius (radius)] [--type (type)] [--sort (sort)]`
- **Permissions**: `fancynpcs.command.npc.nearby`

### `/npc remove`

Removes the specified NPC.

- **Syntax**: `/npc remove (npc)`
- **Permissions**: `fancynpcs.command.npc.remove`

### `/npc show_in_tab`

Changes whether the NPC is shown in the player-list. This works only on NPCs of PLAYER type.

Re-connecting to the server might be required for changes to take effect.

- **Syntax**:  `/npc show_in_tab (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.show_in_tab`

### `/npc skin`

Changes skin of the NPC.

- **Syntax**:  `/npc skin (npc) (@none | @mirror | name | url | file name) [--slim]`

``@none`` - Removes skin.

``@mirror`` - Mirrors the skin of the player viewing the npc.

``name`` / ``uuid`` - Changes skin to the specified player's skin.

``url`` - Changes skin to the specified URL. The URL must point to a valid skin-image.

``file name`` - Changes skin to the specified image. The image must be located in the ``plugins/FancyNpcs/skins`` directory. Please only provide the file name (e. g. "cool-skin.png"). 

``--slim`` - Only works for skins set by an URL or file.

- **Permissions**: `fancynpcs.command.npc.skin`

### `/npc teleport`

Teleports you to the specified NPC.

- **Syntax**:  `/npc teleport (npc)`
- **Permissions**: `fancynpcs.command.npc.teleport`
- Now **teleports sender** to the NPC. Teleportng **the NPC** to specified location is now handled by `/npc move_to`
  command.

### `/npc turn_to_player`

Changes whether the NPC should turn to the player when in range.

- **Syntax**:  `/npc turn_to_player (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.turn_to_player`

### `/npc type`

Changes the type of the NPC.

- **Syntax**:  `/npc type (npc) (type)`
- **Permissions**: `fancynpcs.command.npc.type`

### `/npc scale (npc) (factor)`

Changes the scale of the size of the NPC.

- **Syntax**:  `/npc scale (npc) (factor)`
- **Permissions**: `fancynpcs.command.npc.scale`

### `Add action`

Adds an action to the specified NPC's trigger.

- **Syntax**: `/npc action (npc) (trigger) add (actionType) [value]`
- **Permissions**: `fancynpcs.command.npc.action.add`

### `Add action before`

Adds an action before the specified index in the NPC's action list for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) add_before (index) (actionType) [value]`
- **Permissions**: `fancynpcs.command.npc.action.addBefore`

### `Add action after`

Adds an action after the specified index in the NPC's action list for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) add_after (index) (actionType) [value]`
- **Permissions**: `fancynpcs.command.npc.action.addAfter`

### `Set action`

Sets an action at the specified number in the NPC's action list for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) set (number) (actionType) [value]`
- **Permissions**: `fancynpcs.command.npc.action.set`

### `Remove action`

Removes an action from the NPC's action list based on the specified number for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) remove (number)`
- **Permissions**: `fancynpcs.command.npc.action.remove`

### `Move action up`

Moves the action at the specified number up in the NPC's action list for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) move_up (number)`
- **Permissions**: `fancynpcs.command.npc.action.moveUp`

### `Move action down`

Moves the action at the specified number down in the NPC's action list for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) move_down (number)`
- **Permissions**: `fancynpcs.command.npc.action.moveDown`

### `Clear actions`

Clears all actions from the NPC for the given trigger.

- **Syntax**: `/npc action (npc) (trigger) clear`
- **Permissions**: `fancynpcs.command.npc.action.clear`

### `List actions`

Lists all actions for the specified NPC and trigger.

- **Syntax**: `/npc action (npc) (trigger) list`
- **Permissions**: `fancynpcs.command.npc.action.list`