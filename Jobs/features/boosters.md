# Boosters

```
/aja boosters add <player/all> <PROGRESS/POINTS/REWARDS> <percent> <hours> <affects> - Adds booster
/aja boosters clear <player/all> - Removes boosters

/aja boosters - List of all active boosters
```

* hours can be decimal. I.e. 0.5 means 30 minutes

### **Possible "affects" arg**

```
 Possible cases (split with ,): [PROGRESS/POINTS]
    - all
    - free
    - premium
    - job-J

    J - ID of job

    Example: free,job-explorer
    Booster will affect all free jobs and explorer job

    Possible cases (split with ,): [REWARDS]
    - all
    - free
    - premium
    - job-J
    - reward-R

   R - ID of reward
   J - ID of job

   Example: free,reward-1
   Booster will affect all rewards in free jobs and reward with ID 1
```

### %booster% arg in reward's variables

To make boosters work in rewards, we need to use new placeholder - `%booster%`

Example:

```
  variables:
    value: "(2 * %tier%) * (1 + (%booster% / 100))"
```

### Boosters strategy

Boosters have 3 different strategies. It's important when player has more than 1 active booster at once

`boosters-strategy` in `settings.yml`

```
# SUM - If player has multiple boosters, plugin will sum them
# Example:
# - Server booster +10%
# - Player booster +7%
# - Player booster +5%
# Final booster: 10 + 7 + 5 = 22%
#
# SUM_DIFFERENT - If player has multiple boosters, highest server booster will be added to the highest player booster
# Example:
# - Server booster +10%
# - Player booster +7%
# - Player booster +5%
# Final booster: 10 + 7 = 17%
#
# HIGHEST - If player has multiple boosters, plugin will use the highest booster
# Example:
# - Server booster +10%
# - Player booster +7%
# - Player booster +5%
# Final booster: 10%
```
