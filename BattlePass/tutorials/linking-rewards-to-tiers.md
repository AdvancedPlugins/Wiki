---
description: Follow a step by step tutorial to link your rewards to tiers by yourself.
---

# Linking Rewards To Tiers

There are two passes called free and premium. You will use the same rewards.yml for each but you can pick and chose which go in what passes.



**UNDERSTANDING THE TIER SYSTEM**

Below is the default "free" pass all players have. At the bottom you have a list of tiers under "tiers:"    Please view this config below and read each explanation of what code does what.

```yaml
name: 'Free' #
default-points-required: 100 #
dont-give-premium-free-rewards: false # This will mean that premium users will not receive free rewards

items:
  doesnt-have-pass-item: # This is ONLY shown/used if you have dont-give-premium-free-rewards: true. This is used to make it so premium users can only have premium rewards.
    material: 'minecart:0' #(Tier block/item displayed in GUI)
    name: '&eTier %tier%' #(Tier name)
    lore: #(Tier description)
      - '' #(Tier description)
      - '&cYou can only claim premium rewards' #(Tier description)
  locked-tier-item: #(What is displayed when tier is lockedin GUI)
    material: 'furnace_minecart:0' #(Tier block/item displayed in GUI)
    name: '&eTier %tier%' #(Tier name)
    lore: #(Tier description)
      - '' #(Tier description)
      - '&7Rewards:' #(Tier description)
      - '%lore_addon%' #(Tier description)
      - '' #(Tier description)
      - '&7Status: &cLocked' #(Tier description)
  unlocked-tier-item: #(What is displayed when tier is unlocked in GUI)
    material: 'chest_minecart:0' #(Tier block/item displayed in GUI)
    name: '&aTier %tier%' #(Tier name)
    lore: #(Tier description)
      - '' #(Tier description)
      - '&7Rewards:' #(Tier description)
      - '%lore_addon%' #(Tier description)
      - '' #(Tier description)
      - '&7Status: &aUnlocked' #(Tier description)
  claimed-tier-item: #(What is displayed when tier is claimed in GUI)
    material: 'minecart:0' #(Tier block/item displayed in GUI)
    name: '&aTier %tier%' #(Tier name)
    lore: #(Tier description)
      - '' #(Tier description)
      - '&7Rewards:' #(Tier description)
      - '%lore_addon%' #(Tier description)
      - '' #(Tier description)
      - '&7Status: &aClaimed' #(Tier description)

tier-up-actions: #(What happens when a player goes up a tier)
  - '[message] {&7You reached tier &e%tier%}' #(message sent when on new tier)

tiers: #
  '2': #(The tier number)(This would be the second tier in the free pass and reward 1 in rewards.yml is in that place))
    rewards: ['1'] #(The reward numbers to give to the player see rewards.yml)
    required-points: 120 #(The amount of points the player must get to advance to the tier)
  '4':
    rewards: ['4', '2']
  '10':
    rewards: ['1', '2', '3', '4']
    required-points: 500
    locked-tier-item: # You can specify any of the items in the 'items' section above per tier. They're completely optional for each tier.
      material: 'barrier:0'
      name: '&eTier %tier%'
      lore:
        - ''
        - '&7Rewards:'
        - '%lore_addon%'
        - ''
        - '&7Status: &cSpecial Locked Item'
```



The way to format the Premium pass is the exact same as the free example above.



**ADDING TIERS TO THE CONFIG**

Here you will see the exact way and format to add more tiers to your free or premium passes. For example we have are default tiers '2','4' and '10'. Lets add a tier in at 7 with a reward here is how. Copy and paste one of the tiers, I copied '4' and change the 4 to your desired tier number and change the reward they will receive so I chose reward 1. Make sure everything is aligned and formatted correctly. Once you are happy with amount of tiers you have made save and exit then restart your server or reload the plugin.

```yaml
tiers:
  '2': # The tier number
    rewards: ['1'] # The reward numbers to give to the player (see rewards.yml).
    required-points: 120 # The amount of points the player must get to advance to the tier.
  '4':
    rewards: ['4', '2']
  '7':
    rewards: ['1']  
  '10':
    rewards: ['1', '2', '3', '4']
    required-points: 500
    locked-tier-item: # You can specify any of the items in the 'items' section above per tier. They're completely optional for each tier.
      material: 'barrier:0'
      name: '&eTier %tier%'
      lore:
        - ''
        - '&7Rewards:'
        - '%lore_addon%'
        - ''
        - '&7Status: &cSpecial Locked Item'
```

<mark style="color:orange;">Side note -</mark> You can also add more then one reward please follow the format above to do so.
