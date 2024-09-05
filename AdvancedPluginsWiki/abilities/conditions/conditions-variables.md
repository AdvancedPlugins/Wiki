---
description: Dynamic variables to be used in conditions and abilities.
---

# Conditions Variables

Conditions can be targeted against different entities. You can use **attacker** or **victim** instead of **player**, for example: `%player health%` -> `%victim health%`.

### List of built-in variables

{% hint style="info" %}
All variables can start with 'player', 'attacker', and 'victim'\
Example: '%victim is on fire%'
{% endhint %}

{% hint style="info" %}
Parsing for attacker or victim works for placeholders from PlaceholderAPI as well.\
Example: "%victim checkitem\_getinfo:39\_mat:%"
{% endhint %}

#### Player only variables

<table data-header-hidden><thead><tr><th>Variable</th><th width="300">Description</th></tr></thead><tbody><tr><td>Variable</td><td>Description</td></tr><tr><td>%can break%</td><td>True if a player can break the block</td></tr><tr><td>%faction land%</td><td>Gets faction land player is in.</td></tr><tr><td>%food%</td><td>Food level of player</td></tr><tr><td>%is bleeding%</td><td>True if the player is bleeding via McMMO</td></tr><tr><td>%helmet%</td><td>Equipped Helmet</td></tr><tr><td>%chestplate% </td><td>Equipped Chestplate</td></tr><tr><td>%leggins%</td><td>Equipped Leggins</td></tr><tr><td>%boots%</td><td>Equipped Boots</td></tr><tr><td>%is blocking%</td><td>True if the player is blocking</td></tr><tr><td>%is flying%</td><td>True if the player is flying</td></tr><tr><td>%is sneaking% </td><td>True if the player is sneaking</td></tr><tr><td>%level of skill &#x3C;skill>%</td><td>Level of a player's McMMO skill</td></tr><tr><td>%permissions%</td><td>All player's permissions</td></tr><tr><td>%is op%</td><td>True if player has OP</td></tr></tbody></table>

#### Global Variables

| Variable                                               | Description                                                                                                                                                        |
| ------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| %block below%                                          | Block type player/ mob is standing on                                                                                                                              |
| %trigger type%                                         | Type of trigger                                                                                                                                                    |
| %combo%                                                | Current combo                                                                                                                                                      |
| %custom name%                                          | Custom name of player/ mob                                                                                                                                         |
| %has enchantment in hand of \<enchant>%                | Whether player/ mob has an enchantment on the item in its main hand                                                                                                |
| %has enchantment in hand of \<enchant> level \<level>% | Whether player/ mob has an enchantment of a specific level on the item in its main hand                                                                            |
| %has enchantment in \<armor slot> of \<enchantment>%   | Whether player/ mob has an enchantment on the item in a specific armor slot                                                                                        |
| %has potion effect \<effect>%                          | <p>Whether player/ mob has a potion effect<br><a href="https://helpch.at/docs/1.12.2/index.html?org/bukkit/potion/PotionEffectType.html">PotionEffectTypes</a></p> |
| %item in hand level \<enhantment>%                     | Level of enchantment on item in main hand                                                                                                                          |
| %health%                                               | The health of player/ mob                                                                                                                                          |
| %health percentage%                                    | Percentage of health left                                                                                                                                          |
| %is critical%                                          | Whether attack was a critical hit                                                                                                                                  |
| %is gliding%                                           | Whether player/ mob is gliding                                                                                                                                     |
| %is holding%                                           | Type of item currently held by player/ mob                                                                                                                         |
| %is hostile%                                           | Whether mob is hostile                                                                                                                                             |
| %is damageable%                                        | Whether the player/mob can be damaged                                                                                                                              |
| %is on fire%                                           | Whether player/ mob is on fire                                                                                                                                     |
| %is removal%                                           | Whether effect is removal (EFFECT\_STATIC, HELD, SHIFT, SPRINT)                                                                                                    |
| %is under water%                                       | Whether player/ mob is underwater                                                                                                                                  |
| %item slot%                                            | Slot of item that triggered enchant                                                                                                                                |
| %max health%                                           | Maximum health of player/ mob                                                                                                                                      |
| %mob type%                                             | Type of mob                                                                                                                                                        |
| %name%                                                 | Name of player/ mob                                                                                                                                                |
| %nearby mobs%                                          | Amount of mobs in a 10 block radius                                                                                                                                |
| %offhand item%                                         | Type of item currently held in offhand by player/ mob                                                                                                              |
| %players%                                              | Amount of players in a 10 block radius                                                                                                                             |
| %potion effect level \<effect> \<level>%               | Whether player/ mob has a potion effect of a specifc level                                                                                                         |
| %time%                                                 | Time of the world                                                                                                                                                  |
| %x%                                                    | X coordinate of player/ mob                                                                                                                                        |
| %y%                                                    | Y coordinate of player/ mob                                                                                                                                        |
| %z%                                                    | Z coordinate of player/ mob                                                                                                                                        |
| %x double%                                             | More precise X coordinate of player/ mob                                                                                                                           |
| %y double%                                             | More precise Y coordinate of player/ mob                                                                                                                           |
| %z double%                                             | More precise Z coordinate of player/ mob                                                                                                                           |
| %block tags%                                           | Array of tags a target block has                                                                                                                                   |
| %is riding%                                            | Whether player/mob is riding player/mob (or is a passenger)                                                                                                        |
| %passengers%                                           | Passengers of the player/mob                                                                                                                                       |

#### Type-specific variables (global)

| Variable               | Description                                        | Applicable Type(s)                                     |
| ---------------------- | -------------------------------------------------- | ------------------------------------------------------ |
| %is headshot%          | Whether an arrow/ trident hit was a headshot       | BOW, BOW\_MOB, DEFENSE\_BOW, DEFENSE\_BOW\_MOB         |
| %force%                | Force of bow when firing arrow                     | BOW\_FIRE                                              |
| %damaged from behind%  | If victim was damaged from behind by enemy         | DEFENSE, DEFENSE\_MOB, DEFENSE\_BOW, DEFENSE\_BOW\_MOB |
| %projectile type%      | Type of projectile ("arrow" or "trident")          | BOW, BOW\_MOB, DEFENSE\_BOW, DEFENSE\_BOW\_MOB         |
| %exp%                  | Amount of EXP to give/ drop                        | CATCH\_FISH, FISHING, KILL\_MOB                        |
| %caught%               | Type of item player caught                         | CATCH\_FISH, FISHING                                   |
| %maximum durability%   | Maximum durability of item                         | ITEM\_BREAK                                            |
| %block x%              | X coordinate of block broken                       | MINING                                                 |
| %block y%              | Y coordinate of block broken                       | MINING                                                 |
| %block z%              | Z coordinate of block broken                       | MINING                                                 |
| %block type%           | Type of block                                      | MINING, SWING                                          |
| %block type lowercase% | Type of block but all letters are lowercase        | MINING                                                 |
| %block drop type%      | Type of item block will drop                       | MINING                                                 |
| %is crop%              | Whether broken block was a crop                    | MINING                                                 |
| %is fully grown%       | Whether broken crop was fully grown                | MINING                                                 |
| %block location%       | Location of the block (used in location parameter) | MINING, SWING                                          |
| %damage%               | Final damage                                       | Any type triggered by damage or an attack              |
| %raw damage%           | Damage before armor                                | Any type triggered by damage or an attack              |
| %damage cause%         | Cause of damage                                    | Any type triggered by damage or an attack              |



### PlaceholderAPI support

E.g: `%victim player_level% > 10 : %stop%`, `player_level` is a PlaceholderAPI placeholder `%player_level%`.&#x20;

You can use `%player %`, `%attacker %` or`%victim %`

It's a must to remove percentage signs from PlaceholderAPI placeholders, more examples: `%server_online% -> server_online` -> `%player server_online% > 5 : %allow%`
