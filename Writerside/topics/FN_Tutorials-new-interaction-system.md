# New Interaction System

The **NPC Action System** in FancyNPCs allows server administrators to create interactive and engaging NPCs by assigning
actions that trigger based on player interactions or custom events. This article explains the general concept of the
system and provides a guide on how server admins can leverage it through commands.

## How the NPC Action System Works

In FancyNPCs, the NPC Action System revolves around assigning actions to an NPC based on **triggers**. These triggers
can be events like:

- **LEFT_CLICK**: When a player left-clicks the NPC.
- **RIGHT_CLICK**: When a player right-clicks the NPC.
- **CUSTOM**: Custom events triggered through the API.

Each trigger can execute a series of **actions**. Actions determine what the NPC does when the trigger is activated,
such as sending messages, executing commands, teleporting players, or waiting for a certain duration before performing
the next action. Administrators can add, modify, and reorder these actions using commands.

### Supported Action Types

The system currently supports the following action types:

- **Message**: Sends a message to the player.
- **ConsoleCommand**: Executes a command as the server/console.
- **PlayerCommand**: Executes a command as the player.
- **SendToServer**: Sends the player to another server (using BungeeCord plugin messaging).
- **WaitAction**: Pauses the action sequence for a specific duration.
- **ExecuteRandomAction**: Randomly selects and performs one action from a list, below the current action.

## Command Overview

FancyNPCs provides a range of commands for managing actions attached to an NPC. The following sections describe each
command and its usage.

### 1. Adding Actions to an NPC

**Command**:  
`/npc action <npc> <trigger> add <actionType> [value]`

This command adds an action to an NPC under a specific trigger. For example, you might assign a **Message** action to
the **RIGHT_CLICK** trigger, so when a player right-clicks the NPC, they receive a message.

Example:  
`/npc action Bob RIGHT_CLICK add message <green>Welcome to the server!`

If the action type requires a value (such as a message or command), it must be provided.

### 2. Inserting Actions Before or After

**Command**:  
`/npc action <npc> <trigger> add_before <index> <actionType> [value]`

**Command**:  
`/npc action <npc> <trigger> add_after <index> <actionType> [value]`

These commands allow you to insert an action before or after an existing action at a specific position (index). This is
helpful for fine-tuning the sequence of actions.

Example:  
`/npc action Bob RIGHT_CLICK add_before 2 message <green>Goodbye!`

### 3. Setting (Replacing) an Action

**Command**:  
`/npc action <npc> <trigger> set <number> <actionType> [value]`

This command replaces an action at a specific position in the action list for a trigger. If you want to change the
action at position 3 to a **PlayerCommand**, you can use this command.

Example:  
`/npc action Bob LEFT_CLICK set 3 player_command warp home`

### 4. Removing an Action

**Command**:  
`/npc action <npc> <trigger> remove <number>`

To remove an action from the list, use this command, specifying the position of the action to be removed.

Example:  
`/npc action Bob RIGHT_CLICK remove 2`

### 5. Moving Actions

**Move Up**:  
`/npc action <npc> <trigger> move_up <number>`

**Move Down**:  
`/npc action <npc> <trigger> move_down <number>`

These commands allow you to rearrange the sequence of actions by moving an action up or down in the list.

Example:  
`/npc action Bob RIGHT_CLICK move_up 3`

### 6. Clearing All Actions

**Command**:  
`/npc action <npc> <trigger> clear`

To remove all actions associated with a trigger, use the `clear` command.

Example:  
`/npc action Bob LEFT_CLICK clear`

### 7. Listing All Actions

**Command**:  
`/npc action <npc> <trigger> list`

This command lists all the actions assigned to a specific trigger for an NPC. It helps you review and manage the current
actions.

Example:  
`/npc action Bob RIGHT_CLICK list`

## Practical Example

Let’s create an NPC called **"Bob"** who greets players when right-clicked, executes a server command, waits, and then
sends them to a different server:

1. Add a message:  
   `/npc action Bob RIGHT_CLICK add message Hello, adventurer!`

2. Execute a console command:  
   `/npc action Bob RIGHT_CLICK add console_command say Bob has been clicked!`

3. Wait for 5 seconds:  
   `/npc action Bob RIGHT_CLICK add wait 5`

4. Send the player to another server:  
   `/npc action Bob RIGHT_CLICK add send_to_server Hub`

If you wanted to insert a random action after the message, you could use:

`/npc action Bob RIGHT_CLICK add_after 1 execute_random_action`

## Outlook

The NPC Action System in FancyNPCs provides a flexible and powerful way to create interactive NPCs on your server. By
combining triggers and actions, server administrators can design engaging interactions that enhance the player
experience.

In future updates, we plan to expand the system with additional action types and triggers, enabling even more creative
and dynamic NPC behaviors. Stay tuned for more exciting features and improvements!