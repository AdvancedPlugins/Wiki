# Variables

Variables are placeholders for dynamic data in Ability configurations. They allow for more flexibility and customization in Abilities.

### Usage

To use a variable, simply include it in an Ability configuration with the `%` symbol surrounding it. For example:

```yaml
effects:
- "MESSAGE: The attacker's name is %attacker name%"
```

### Available Variables

| VARIABLE                                      | DESCRIPTION                                                                                                                                                                                                                          |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `%attacker name%`                             | The name of the entity that initiated an Ability.                                                                                                                                                                                    |
| `%victim name%`                               | The name of the entity that was targeted by an Ability.                                                                                                                                                                              |
| `%block type%`                                | The type of the block that was targeted by an Ability.                                                                                                                                                                               |
| `%system time%`                               | The current system time, in milliseconds.                                                                                                                                                                                            |
| `%exp%`                                       | Amount of exp that was dropped in trigger event                                                                                                                                                                                      |
| `%player name%`                               | Main entity's name                                                                                                                                                                                                                   |
| `%damage%`                                    | Damage dealt (after armor etc)                                                                                                                                                                                                       |
| `%raw damage%`                                | Raw damage dealt (before armor etc)                                                                                                                                                                                                  |
| `%damage cause%`                              | Cause of damage                                                                                                                                                                                                                      |
| `%random%`                                    | Last \<random> number                                                                                                                                                                                                                |
| `%is removed%`                                | Whether the effect is being removed. Is used mostly on triggers like EFFECT\_STATIC, HELD etc.                                                                                                                                       |
| `%client version%`                            | Returns client's protocol version. Find all versions here: [https://wiki.vg/Protocol\_version\_numbers](https://wiki.vg/Protocol\_version\_numbers)                                                                                  |
| `%potion type%, %is extended%, %is upgraded%` | From BREW\_POTION trigger, passes data on potion. Potion types: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionEffectType.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/potion/PotionEffectType.html) |
| `%block is interactable%`                                    | Whether the block is interactable or not from [bukkit api](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/block/BlockType.html#isInteractable())                                                                                                                                                                                                                |


## Plugin-specific variables:

### AdvancedEnchantments:

| VARIABLE          | DESCRIPTION             |
| ----------------- | ----------------------- |
| `%level%`         | Level of enchantment    |
| `%souls on item%` | Amount of souls in item |
