# Commands

This page provides detailed information about the various commands available in FancyNpcs, allowing you to make the
most out of its features.

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

- **Syntax**:  `/npc fix (npc)`
- **Permissions**: `fancynpcs.command.npc.fix`

### `/npc glowing`

Changes glowing state and color of the NPC.

- **Syntax**:  `/npc glowing (npc) [disabled | color]`
- **Permissions**: `fancynpcs.command.npc.glowing`

### `/npc help`

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

### `/npc message`

``add`` - Adds a new message to the list.

``set`` - Sets a message at a specific index.

``remove`` - Removes a message at a specific index.

``clear`` - Clears all messages.

``list`` - Lists all messages.

``send_randomly`` - Changes the order of messages to be sent randomly.

Messages are shown to players when they interact with the NPC.

PlaceholderAPI and MiniPlaceholders are supported.

- **Syntax**: `/npc message (npc) (add | set | remove | clear | list | send_randmly)`
- **Permissions**: `fancynpcs.command.npc.message.(sub)`
- Empty message placeholder is `@none`.

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

### `/npc player_command`

``add`` - Adds a new player command to the list.

``set`` - Sets a player command at a specific index.

``remove`` - Removes a player command at a specific index.

``clear`` - Clears all player commands.

``list`` - Lists all player commands.

Player commands are executed by the player when players interact with the NPC.

PlaceholderAPI and MiniPlaceholders are supported.

- **Syntax**: `/npc player_command (npc) (add | set | remove | clear | list)`
- **Permissions**: `fancynpcs.command.npc.player_command.(sub)`

### `/npc remove`

- **Syntax**: `/npc remove (npc)`
- **Permissions**: `fancynpcs.command.npc.remove`

### `/npc server_command`

``add`` - Adds a new server command to the list.

``set`` - Sets a server command at a specific index.

``remove`` - Removes a server command at a specific index.

``clear`` - Clears all server commands.

``list`` - Lists all server commands.

Server commands are executed by the console, when players interact with the NPC.

PlaceholderAPI and MiniPlaceholders are supported.

- **Syntax**: `/npc server_command (npc) (add | set | remove | clear | list)`
- **Permissions**: `fancynpcs.command.npc.server_command.(sub)`

### `/npc show_in_tab`

Changes whether the NPC is shown in the player-list. This works only on NPCs of PLAYER type.

Re-connecting to the server might be required for changes to take effect.

- **Syntax**:  `/npc show_in_tab (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.show_in_tab`

### `/npc skin`

Changes skin of the NPC.

``@none`` - Removes skin.

``@mirror`` - Mirrors the skin of the player viewing the npc.

``name`` - Changes skin to the specified player's skin.

``url`` - Changes skin to the specified URL.

- **Syntax**:  `/npc skin (npc) (@none | @mirror | name | url)`
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