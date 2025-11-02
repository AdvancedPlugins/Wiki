# Boosters

Boosters system allows adding booster for certain amount of time by admin. Booster can boost progress, points or rewards. It has a lot of possible areas where it affects.

## Applying boosters

### By commands

```
/aca boosters add <player/all> <PROGRESS/POINTS/REWARDS> <percent> <hours> <affects> - Adds booster
/aca boosters clear <player/all> - Removes boosters

/challenges boosters - List of all active boosters
```

-   hours can be decimal. I.e. 0.5 means 30 minutes

### By permission

You can configure "permission boosters" in `plugins/AdvancedChallenges/config.yml` in `permission-boosters` section.

```yaml
# Permission based boosters
# Players with permission `advancedchallenges.booster.<booster-id>` will get the booster
# IMPORTANT: This boosters work only for ONLINE players.
permission-boosters:
    "extra25": #  Permission 'advancedchallenges.booster.extra25'
        percent: 25.0
        affects: all
        type: PROGRESS
```

### **Possible "affects" arg**

```
Possible cases (split with ,): [PROGRESS/POINTS]
- all
- CAT
- CAT-CH

CAT - ID of category
CH - ID of challenge

i.e. daily - all daily quests, daily-d-10 - daily challenge with d-10 id

Possible cases (split with ,): [REWARDS]
- all
- reward-R

R - ID of reward

i.e. reward-daily - daily reward
```

### %booster% arg in reward's variables

To make boosters work in rewards, we have to use a placeholder - `%booster%`

Example:

```
  variables:
    value: "(2 * %tier%) * (1 + (%booster% / 100))"
```

### Boosters strategy

Boosters have 3 different strategies. It's important when player has more than 1 active booster at once

`boosters-strategy` in `plugins/AdvancedChallenges/config.yml`

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
