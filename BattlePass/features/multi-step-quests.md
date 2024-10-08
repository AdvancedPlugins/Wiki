# Multi-Step quests

Learn how to create multiple step quests!

```yaml
10: # Multiple step quest
    name: 'Week 1 - Advanced Miner'
    steps:
      1:
        type: block-break
        variable: coal_ore:0
        required-progress: 10
        points: 0
        info:
          - "&7Mine &e10 coal ores"
      2:
        type: block-break
        variable: iron_ore:0
        required-progress: 10
        points: 5
        info:
          - "&7Mine &e10 iron ores"
      3:
        type: block-break
        variable: diamond_ore:0
        required-progress: 10
        points: 25
        info:
          - "&7Mine &e10 diamond ores"
    item:
      material: golden_pickaxe:0
      name: '&eAdvanced Miner &7(&e%step%&7/&6%steps%&7)'
      lore:
        - '&7Mine various ores'
        - '%info%'
        - ''
        - '&7Progress &e%total_progress%&7/&e%required_progress%'
```

This quest has 3 steps:

* Mine 10 coal ores (no rewards)
* Mine 10 iron ores (gives 5 points)
* Mine 10 diamond ores (gives 25 points)

After completing all 3 steps, the quest will complete.

### How to create a quest with multiple steps

As in the example, create a section `steps` and add quest parameters to each step section as desired. Available parameters: type, variable, required-progress, points, whitelisted-worlds, blacklisted-worlds, whitelisted-regions, blacklisted-regions, complete-commands, info, exclusive, anti-abuse, special-progress.

### Info parameter

Each step can contain a list of information which you can use inside the quest icon (`%info%`).

### New placeholders in icon

* `%step%` - current step
* `%steps%` - number of steps
* `%info%` - information from step `info` parameter

### Global quest parameters

Some values like type, required-progress, whitelist, blacklist etc. can be used globally by adding them to the quest section instead of the step section.

Example:

```yaml
yamlCopy10: # Multiple step quest
    name: 'Week 1 - Advanced Miner'
    required-progress: 10
    points: 5
    steps:
      1:
        type: block-break
        variable: coal_ore:0
        info:
          - "&7Mine &e10 coal ores"
      2:
        type: block-break
        variable: iron_ore:0
        info:
          - "&7Mine &e10 iron ores"
      3:
        type: block-break
        variable: diamond_ore:0
        info:
          - "&7Mine &e10 diamond ores"
```

In this example, all steps require 10 progress and give 5 points (per step).
