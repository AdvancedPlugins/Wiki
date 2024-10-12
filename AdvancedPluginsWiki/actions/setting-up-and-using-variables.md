# Setting up and using Variables

{% hint style="warning" %}
BattlePass 4.6.2 and AdvancedJobs 1.4.1 removed MaterialData from items in variables (`:0`, `:1` at the end of item's type).
{% endhint %}

The core of actions is the variable system. The basis of this system is that it is a filter. If the variable is set to `none`, there is no filter. If it is set, if whatever the variable is entered as when a user performs an action matches the variable, it will progress.

Recently, we've also added sub variables which can make this system a bit more confusing. Here are some examples for different action types with and without sub variables.

Every action has the global sub variables listed below:

```yml
variable:
  root: none
  holding:
    item: diamond_sword
    name: 'IDK some name'
    amount: 1
    model: 0 # Custom Model Data (for resource packs)
```

Every sub-variable is optional. If you don't specify it, it won't be filtered for. Therefore, you can just use `holding.item` if you wish, or just `holding.amount`.

## Basic Examples

**Without Sub-Variables:**

The following two actions function in the same manner, they're just two ways of formatting them.

`block-break`

```yml
variable:
  root: stone
```

`block-break`

```yml
variable: stone
```

Some more random examples: `throw-projectile`

```yml
variable: SNOWBALL
```

**With Sub-Variables:**

`block-break`

```yml
variable:
  root: diamond_block
  holding:
    item: golden_pickaxe
```

`enchant-all`

```yml
variable:
  root: SOUL_SPEED
  item: diamond_sword
  level: 3
```

This action is to enchant an item with soul speed 3 using an anvil.

**With Multiple Variables:**

`block-break`

```yml
variable: diamond_block OR gold_block OR iron_block
#This will progress the action if any of the blocks listed above is mined.
```

`block-place`

```yml
variable:
  - "stone"
  - "cobblestone"
  - "gravel"
# This will progress the quest if any of the blocks listed above is placed.
```

## Blacklists

To create blacklist in variable, use `!` in front of first element

**Examples without subroots:**

`block-break`

```yml
variable: "!stone OR dirt"
# This will progress the quest if player mined any block except stone and dirt
```

`block-place`

```yml
variable: 
  - "!stone"
  - "dirt"
# This will progress the quest if player placed any block except stone and dirt
```

**Examples with subroots:**

```yml
variable:
  root: "none"
  holding:
    item: "!diamond_pickaxe"
# This will progress the quest if player doesn't hold diamond pickaxe
```

## Variable format

There are some formats which you can use in variables to achieve certain functionality

### "Contains" element

"CONTAINS" element check if action root/subroot contains specified text. TO create this, add `__` before element.

**Example:**

```yml
variable: __ORE
```
In this case, root will accept every item which contains ORE in name (it also applies for strings and entities)

### ItemsAdder (experimental)

Just add `itemsadder:` before element name to use itemsadder items, block or entities 

**Example:**
```yml
variable: itemsadder:ITEM_NAME
```

### Properties

You can add some properties in JSON format.

#### `nbt` property

Minecraft NBT String to modify required item. I.e. to create quest that progres only when we use unbreakable diamond pickaxe, we can use this property.

Note: Minecraft NBT String must contain item name. It also must be in correct format (1.20.5 changed format of NBT String i.e. in give command)

**Example:**

```yml
variable:
    root: none
    holding:
        item: "diamond_pickaxe{nbt: 'diamond_pickaxe[unbreakable={}]'}"
```

#### `faces` property

Support for block with multiple faces i.e. mushroom blocks.

**Example:**

```yml
variable: "brown_mushroom_block{faces: ['west', 'east']}"
```

#### `age` property

Age of Ageable material i.e. age of planted carrot

**Example:**

```yml
variable: "carrots{age: 3}"
```

#### `progress` property

Added progress property (similar to old `special-progress` section). It's multiplier of progress.

**Example:**

```yml
variable: "iron_ingot OR diamond{progress: 3}"
```
In this case, diamond gives 3 progress instead of 1.

{% hint style="info" %}
`special-progress` is still available for cases where we can't use progress property, i.e. in blacklists
{% endhint %}

## PAPI conditions

If you have PlaceholderAPI installed, you can use variables conditions to have more control over when player can progress quest.

There are 2 types of conditions:

* `or` (same as `||` in Java) - player must meet at least one condition to progress
* `and` (same as `&&` in Java) - player must meet all conditions to progress

**Example:**

```yml
variable:
    root: none
    conditions:
        or:
          - "%player_is_op% == yes"
          - "%player_level% > 10"
        and: []
```

In this case, action will progress only when the player is op OR has level greater than 10.