# Boosters

Boosters system allows adding booster for certain amount of time by admin. Booster can boost progress, points or rewards. It has a lot of possible areas where it affects.

### **Bungee Compatibility**

To make boosters work in bungee network, just set `bungee-fix: true` in `settings.yml`. Boosters will refresh every `auto-save-interval` from `settings.yml`

### New Commands

```
/bpa boosters add <player/all> <PROGRESS/POINTS/REWARDS> <percent> <hours> <affects> - Adds booster
/bpa boosters clear <player/all> - Removes boosters

/bp boosters - List of all active boosters
```

-   hours can be decimal. I.e. 0.5 means 30 minutes

### **Possible "affects" arg**

```
Possible cases (split with ,): [PROGRESS/POINTS]
- all
- daily
- week
- week-W
- daily-Q
- week-W-Q

W - ID of week
Q - ID of quest

Example: week-1,week-2-2,daily
Booster will affect quests from week 1, quest with ID 2 from week 2 and all daily quests

Possible cases (split with ,): [REWARDS]
- all
- reward-R
- tier-T

R - ID of reward
T - ID of tier

Example: tier-1,reward-2,reward-4
Booster will affect rewards with ID 2 and 4
```

### %booster% arg in reward's variables

To make boosters work in rewards, we need to use new placeholder - `%booster%`

Example:

```
  variables:
    value: "(2 * %tier%) * (1 + (%booster% / 100))"
```

### Quest ID in menu

When `menu-show-id: true`, players with permission `battlepass.debug.id` will see quest's ID in battlepass menu

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

### Permission Boosters

You can configure "permission boosters" in `plugins/BattlePass/settings.yml` in `permission-boosters` section.

```yaml
# Permission based boosters
# Players with permission `battlepass.booster.<booster-id>` will get the booster
# IMPORTANT: This boosters work only for ONLINE players.
permission-boosters:
    "extra25": #  Permission 'battlepass.booster.extra25'
        percent: 25.0
        affects: all
        type: PROGRESS
```
