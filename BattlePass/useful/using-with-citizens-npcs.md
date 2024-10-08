---
description: Setting up NPCs to access menus!
---

# Using with Citizens NPCs

Integrate the BattlePass plugin functionalities with NPCs using the Citizens plugin to enhance player interaction and engagement on your Minecraft server.

## Required Plugins

* **BattlePass** plugin
* **Citizens** Plugin

## Steps

### 1. Create NPCs

First, create NPCs for each BattlePass menu you wish to integrate:

```
/npc create <NPC Name> --type PLAYER
```

### 2. Assign Commands to NPCs

Assign the following commands to your NPCs to enable players to access various BattlePass menus by interacting with them.



| Command                                  | Description              |
| ---------------------------------------- | ------------------------ |
| /npc command add bp open portal -p       | Open main menu           |
| /npc command add bp open daily-quests -p | Open daily quests' menu  |
| /npc command add bp open quests -p       | Open weekly quests' menu |
| /npc command add bp open rewards -p      | Open rewards menu        |

### 3. That's all!

As simple as that - set up NPCs with BattlePass!
