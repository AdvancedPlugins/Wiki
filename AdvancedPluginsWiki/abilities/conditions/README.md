---
description: Learn how to activate abilities depending on set conditions.
---

# Conditions

Conditions let you choose under what circumstances enchantment should be activated/stopped or chance of activation increased/decreased.

### **3 Conditions Elements**

1. Dynamic Variable ([Find all variables here](conditions-variables.md))
2. Expected result
3. Outcome

### How do Conditions work

Conditions work by comparing dynamic variables with your expected result. If variable's result matches your result, then the outcome will be taken into consideration.

### Examples of Conditions

Following condition will not activate effects if player's health is higher than 5 points (2.5 hearts):

`%victim health%      > 5     : %stop%`\
\| **Dynamic Variable** | **Expected Result** | **Outcome** |

Next condition will only allow enchantment to work if player is in a world called `my_world`:

`%player world% = my_world : %allow%`

Final example is a bit more complex, it combines multiple conditions. If player's Y level is less than 30 and health is more than 5 hearts, it will increase chance of effects activating by 10:

`%player y% < 30 && %player health% > 10 = : %chance%+10`

### Nested conditions

Nested Conditions enhance the flexibility of enchantment conditions by allowing complex logical groupings. This feature introduces parentheses () to combine multiple checks, enabling more sophisticated decision-making. For example:

`(%victim max health% > 20 AND %victim world% != dungeon) OR %victim world% = prison : %allow%`

This condition will activate if either: the victim has over 20 health and is not in the dungeon world, or if the victim is in the prison world. Nested conditions support AND, OR operators, and can be used to create intricate, multi-layered logic for enchantment activation.

