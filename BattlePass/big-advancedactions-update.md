# Big AdvancedActions Update

## Big AdvancedActions Update

It closes 6 BattlePass issues and 3 AdvancedJobs issues. It also adds a lot of new features😁

### Removed unused MaterialData from variables

MaterialData (:0,:1 etc.) was useful before Minecraft 1.13 - that Minecraft update removed numeric IDs and MaterialData. Our plugin supports versions 1.17+, so it's no longer required to maintain MaterialData. It also confused a lot of people (what's this :0???)

### Refactored & Recreated variables and action root system

Using new system, we can set string,material,itemstack,block and entity as root/subroot. It gives us more options to enhance our plugin in the future.

#### Removed almost unused MultiMaterial from variables and replaced it to "CONTAINS" type

"CONTAINS" element check if action root/subroot contains specified text. TO create this, add `__` before element.

Example:

```
variable: __ORE
```

In this case, root will accept every item which contains ORE in name (it also applies for strings and entities)

#### Added ability to create variable using list instead of string with " OR " between elements

Example:

```
variable:
    root:
      - "diamond"
      - "iron_ingot"
```

It's same as

```
variable:
    root: "diamond OR iron_ingot"
```

#### Removed case-sensitive from subroots

Now you can specify subroots using lower or upper case.

#### Added suport for itemsadder (experimental)

Just add `itemsadder:` before element name to use itemsadder items, block or entities (I don't know how itemsadder works, so I can't create a nice example, but it's something like `variable: itemsadder:ITEM_NAME` )

### Added JSON properties to root/subroot elements

Now, we can add some properties to root/subroot element using JSON after element.

#### `nbt` property

Added NBT tags to items. Now we can specify Minecraft NBT String to modify required item. I.e. to create quest that progres only when we use unbreakable diamond pickaxe, we can use this property.

**Note: Minecraft NBT String must contain item name. It also must be in correct format (1.20.5 changed format of NBT String i.e. in give command**

Example:

```
variable:
    root: none
    holding:
        item: "diamond_pickaxe{nbt: 'diamond_pickaxe[unbreakable={}]'}"
```

#### `faces` property

Added support for block with multiple faces i.e. mushroom blocks.

Example:

```
variable: "brown_mushroom_block{faces: ['west', 'east']}"
```

#### `age` property

After this update, to specify age of Ageable material, instead of using :AGE, we must use `age` property.

Example:

```
variable: "carrots{age: 3}"
```

#### `progress` property

Added `progress` property (similar to old `special-progress` section). It's multiplier of progress.

Example:

```
variable: "iron_ingot OR diamond{progress: 3}"
```

In this case, diamond gives 3 progress instead of 1.

**Note: `special-progress` is still available for cases where we can't use progress property, i.e. in blacklists**

### Updated blacklists system

Now you can create blacklists for roots **and subroots**. To create blacklist, just add `!` at the beginning of root string (or at the beginning of first element in list root).

**Note: Use only one `!` instead of multiple like in previous versions**

Example:

```
variable: "!diamond OR iron_ingot"
```

```
variable:
  - "!diamond"
  - "iron_ingot"
```

In this case, action will progress in any case except diamonds and iron ingots

### Added variable conditions using PAPI

There are 2 types of conditions:

* `or` (same as `||` in Java) - player must meet at least one condition to progress
* `and` (same as `&&` in Java) - player must meet all conditions to progress

Example:

```
variable:
    root: none
    conditions:
        or:
          - "%player_is_op% == yes"
          - "%player_level% > 10"
        and: []
```

In this case, action will progress only when the player is op OR has level greater than 10.

### Updated anti abuse systems

* Changed old anti abuse block tracking system to recommended `PlayerBlockTracker`
* Added anti abuse system to `block-place` action - now placing block after breaking it won't progress action
* Added anti abuse system to `craft` action - now crafting ingots -> blocks -> ingots…. won't progress action

### Fixed "harvesting materials" like POTATOES, CARROTS etc.

Materials like `POTATOES` are Materials, but can't be used to create ItemStack. In previous version of AdvancedActions, people couldn't set root as these materials, because it throws "Not an item" error. (It wasn't possible to i.e. create quest "harvest 10 potatoes".

### Fixed `harvest-crops` action

This update fixes this action - now harvesting pumpkins, melons and sugar cane also progress quest. I implemented anti abuse system for these new materials and created a system to count how many sugar canes player harvested.

### Updated some internal actions

* `brew` - added `item` subroot
* `consume` - added `item` when `root` is `potion`
* `breed` - root changed from string to entity (still players can use entity type, but they can also use i.e itemsadder entity)
* `fish` - root changed from string to itemstack
* `harvest-crops` - root changed from string to block
* `kill-mob` - root changed from string to entity
* `crops-planted` - root changed from string to material
* `regenerate` - progress changed from int to double
* `ride-mob` - root changed from string to entity
* `tame` - root changed from string to entity
