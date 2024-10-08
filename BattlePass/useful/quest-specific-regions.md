# Quest Specific Regions

For any quests that you would like the progress it not be progressed in, simple add `blacklisted-regions` to the quest you desire as shown below.

```
quests:
  1: # Quest id
    name: 'Daily - Miner' # The name given to the quest.
    type: block-break # The type of quest
    variable: coal_ore:0 # The block the player must break.
    required-progress: 10 # The amount of times the player should break the coal ore block.
    points: 10 # The amount of points that will be rewarded
    blacklisted-regions: #The regions where the quest will not progress
      - 'no-mining-region'
      - 'noCoalRegion'
    item: # The item that will be displayed in menus.
      material: diamond_pickaxe:0
      amount: 1
      name: '&eMiner'
      lore:
        - '&7Mine &e10 coal'
        - ''
        - '&7Progress &e%total_progress%&7/&e%required_progress%'
```

#### Compatibility

* WorldGuard
