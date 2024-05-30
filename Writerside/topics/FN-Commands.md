# Commands

This page provides detailed information about the various commands available in FancyNpcs, allowing you to make the
most out of its features.

## FancyNpcs Commands

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

- **Syntax**:  `/npc attribute (npc) (set | list)`
- **Permissions**: `fancynpcs.command.npc.attribute.(sub)`

### `/npc collidable`

- **Syntax**:  `/npc collidable (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.collidable`

### `/npc copy`

- **Syntax**: `/npc copy (npc) (new_name)`
- **Permissions**: `fancynpcs.command.npc.copy`
- Name check is now more strict and only allows `A-Z a-z 0-9 _ - /` characters.

### `/npc create`

- **Syntax**: `/npc create (name) [--position (x y z)] [--world (world)] [--type (type)]`
- **Permissions**: `fancynpcs.command.npc.create`
- Name check is now more strict and only allows `A-Z a-z 0-9 _ - /` characters.

### `/npc displayname`

- **Syntax**:  `/npc displayname (npc) (@none | name)`
- **Permissions**: `fancynpcs.command.npc.displayname`
- Empty message placeholder is `@none`

### `/npc equipment`

- **Syntax**: `/npc equipment (npc) (set | clear | list)`
- **Permissions**: `fancynpcs.command.npc.equipment.(sub)`
- Accepts either `@none`, `@hand` or valid item type as an argument.

### `/npc fix`

- **Syntax**:  `/npc fix (npc)`
- **Permissions**: `fancynpcs.command.npc.fix`

### `/npc glowing`

- **Syntax**:  `/npc glowing (npc) [disabled | color]`
- **Permissions**: `fancynpcs.command.npc.glowing`

### `/npc help`

- **Syntax**:  `/npc help [page]`
- **Permissions**: `fancynpcs.command.npc.help`

### `/npc info`

- **Syntax**:  `/npc info (npc)`
- **Permissions**: `fancynpcs.command.npc.info`

### `/npc interaction_cooldown`

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

- **Syntax**:  `/npc list [--type (type)] [--sort (sort)]`
- **Permissions**: `fancynpcs.command.npc.list`

### `/npc message`

- **Syntax**: `/npc message (npc) (add | set | remove | clear | list | send_randmly)`
- **Permissions**: `fancynpcs.command.npc.message.(sub)`
- Empty message placeholder is `@none`.

### `/npc move_here`

- **Syntax**:  `/npc move_here (npc)`
- **Permissions**: `fancynpcs.command.npc.move_to`

### `/npc move_to`

- **Syntax**:  `/npc move_to (npc) (x) (y) (z) [world] [--look-in-my-direction]`
- **Permissions**: `fancynpcs.command.npc.move_to`

### `/npc nearby`

- **Syntax**:  `/npc nearby [--radius (radius)] [--type (type)] [--sort (sort)]`
- **Permissions**: `fancynpcs.command.npc.nearby`

### `/npc player_command`

- **Syntax**: `/npc player_command (npc) (add | set | remove | clear | list)`
- **Permissions**: `fancynpcs.command.npc.player_command.(sub)`

### `/npc remove`

- **Syntax**: `/npc remove (npc)`
- **Permissions**: `fancynpcs.command.npc.remove`

### `/npc server_command`

- **Syntax**: `/npc server_command (npc) (add | set | remove | clear | list)`
- **Permissions**: `fancynpcs.command.npc.server_command.(sub)`

### `/npc show_in_tab`

- **Syntax**:  `/npc show_in_tab (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.show_in_tab`

### `/npc skin`

- **Syntax**:  `/npc skin (npc) (@none | @mirror | name | url)`
- **Permissions**: `fancynpcs.command.npc.skin`

### `/npc teleport`

- **Syntax**:  `/npc teleport (npc)`
- **Permissions**: `fancynpcs.command.npc.teleport`
- Now **teleports sender** to the NPC. Teleportng **the NPC** to specified location is now handled by `/npc move_to`
  command.

### `/npc turn_to_player`

- **Syntax**:  `/npc turn_to_player (npc) [state]`
- **Permissions**: `fancynpcs.command.npc.turn_to_player`

### `/npc type`

- **Syntax**:  `/npc type (npc) (type)`
- **Permissions**: `fancynpcs.command.npc.type`
