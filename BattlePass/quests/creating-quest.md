# How to create quest?

## Using in-game editor (easier method)

You use in-game editor you need to use command `/bpa editor`. In menu you need to choose category which you want edit. After that you can edit existing quest or create a new quest.

## By editing `.yml` files

To create or edit quest go to `plugins/BattlePass/quests` folder and open file with category which you want to edit. There you can edit quest which already exists or create a new quest by adding it to `quests` section using this template (if you don't need certain option, just remove line with it):

```yaml
10: # UNIQUE quest ID
    name: "My Quest" # Name of your quest
    type: "block-break" # Check "Quest Types"
    variable: "iron_ore" #Check "Setting up and using Variables"
    points: 5 # Number of points for completing quest
    required-progress: 10 # Required progress to complete quest
    exclusive: "free" # "free" if quest is for everyone or "premium" if is only for players with premium pass
    special-progress: [] # Check "Special Cases Progress"
    complete-commands:  # Commands executed after completing quest
        - "give %player% coal 1" # It will give 1 coal to player for completing this quest :)
    whitelisted-world: []  # Worlds where player can complete quest (or empty when all worlds are allowed)
    blacklisted-worlds: [] # Worlds where player can't complete quest
    whitelisted-regions: [] # WorldGuard regions where player can complete quest (or empty when all regions are allowed)
    blacklisted-regions: [] # WorldGuard regions where player can't complete quest 
    item: # Icon configuration
        material: "diamond" # https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html
        name: "&6Week X &7| &eMy Quest" # Name of item
        lore: # Item description
            - "&6Break 10 iron ores"
            - "&e%total_progress%&7/&e%required_progress%"
        item-flags: [] # https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/ItemFlag.html
        enchants: # List of enchantments
            - "PROTECTION:4"
        customModelData: 0 # Custom Model Data of your item (for resource packs)
        amount: 1 # Item amount
        nbt: "" # Custom NBT text used like in /give command. Example: "diamond[unbreakable={}]" will add Unbreakable modification to this item
```

### Icon placeholders

```
%info% - Information about current step
%step% - Current step
%steps% - Number of steps in this quest
%total_progress% - Progress (number)
%required_progress% - Required progress (number)
%percentage_progress% - Progress (percent)
%progress_bar% - Progress (bar)
```