---
description: New effects system that brings all our plugins into one.
---

# Introduction

We have launched a new effects system to unify all of our plugins which use effects (Enchantments, Pets and Mobs) into one system working together.&#x20;

## Explanation

Abilities are a unique implementation of completely customizable abilities. Abilities can be a powerful tool for adding dynamic gameplay mechanics. By combining effects, triggers, targets, conditions and effects, you can create a wide variety of actions and reactions in your plugin.

* [Effects](effects.md)
* [Triggers](triggers.md)
* [Targets](targets.md)
* [Conditions](conditions/)
* [Functions](functions.md)
* [Variables](variables.md)
* [Pointers](pointers.md)

### Examples

```yaml
    chance: 30 # Chance is optional, default is 100
    cooldown: 5 # Cooldown is optional, default is 0
    cooldownMessage: "&cThis ability is in cooldown!" # Optional cooldown message
    effects:
      - 'LIGHTNING @Victim'
      - 'FIREBALL @Victim'
      - 'MESSAGE:You have been &bfrozen! @NearestPlayer{r=3}'
      - 'FREEZE:10 @NearestPlayer{r=3}'
```
