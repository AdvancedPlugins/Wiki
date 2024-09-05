# Setting up and using Variables

The core of actions is the variable system. The basis of this system is that it is a filter. If the variable is set to `none`, there is no filter. If it is set, if whatever the variable is entered as when a user performs an action matches the variable, it will progress.

Recently, we've also added sub variables which can make this system a bit more confusing. Here are some examples for different action types with and without sub variables.

Every action has the global sub variables listed below:

```
variable:
  root: none
  holding:
    item: diamond_sword:0
    name: 'IDK some name'
    amount: 1
```

Every sub-variable is optional. If you don't specify it, it won't be filtered for. Therefore, you can just use `holding.item` if you wish, or just `holding.amount`.

**Examples Without Sub-Variables:**

The following two actions function in the same manner, they're just two ways of formatting them.

`block-break`

```
variable:
  root: stone:0
```

`block-break`

```
variable: stone:0
```

Some more random examples: `throw-projectile`

```
variable: SNOWBALL
```

**Examples With Sub-Variables:**

`block-break`

```
variable:
  root: diamond_block:0
  holding:
    item: golden_pickaxe:0
```

`enchant-all`

```
variable:
  root: SOUL_SPEED
  item: diamond_sword
  level: 3
```

This action is to enchant an item with soul speed 3 using an anvil.

**Examples With Multiple Variables:**

`block-break`

```
variable: diamond_block:0 OR gold_block:0 OR iron_block:0
//This will progress the action if any of the blocks listed above is mined.
```

`block-place`

```
variable: stone:0 OR cobblestone:0 OR gravel:0
//This will progress the quest if any of the blocks listed above is placed.
```
