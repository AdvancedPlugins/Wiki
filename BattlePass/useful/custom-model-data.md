---
description: How to set custom model data for items with examples
---

# Custom Model Data

Just add `customModelData: <data>` to any item under material, example:

```yaml
items:
  doesnt-have-pass-item: # The item if a player does not have the premium pass.
    material: 'minecart:0'
    customModelData: 0 #Set custom model data
    name: '&eTier %tier%'
    lore:
      - ''
      - '&7Rewards:'
      - '%lore_addon%'
      - ''
      - '&7Status: &eNot Eligible'
      - '&cPurchase the battle pass to'
      - '&cbe able to earn premium rewards.'
```
