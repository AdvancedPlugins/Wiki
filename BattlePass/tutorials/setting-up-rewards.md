---
description: Follow a step by step tutorial to create a reward by yourself.
---

# Setting Up Rewards

There are three types of reward formats you can use: command format, money format or item format. You may use any plugin's command's in them as long as you use the "%player%" placeholder.

**COMMAND FORMAT BREAKDOWN**

Before we start you need to understand what you are editing and what each line of the format means and what it does. Below is a explanation next to each section of the format.

```yaml
'1': #(The reward id used to link it to a tier) (DONT USE THE SAME NUMBER TWICE)
  type: command #(Reward type)
  name: "Announces you achievement" #(Name for booster message)
  lore-addon: #(Reward description)
    - '&6 - Announces you achievement.' #(Reward description)
  commands: #(Item or Command being excuted when reward is claimed)
    - 'broadcast &6%player% reached a key BattlePass tier!!' 
```

**COMMAND FORMAT:**

Here is a example using a ExcellentCrates command to give a key to the player.

```yaml
'1':
  type: command # You can still use commands to give items :)
  name: "1 Common Key" 
  lore-addon:
    - '&6 - &e1 Common Key'
  commands:
    - 'crate key give %player% Common 1'
```

**ITEM FORMAT BREAKDOWN**

Before we start you need to understand what you are editing and what each line of the format means and what it does. Below is a explanation next to each section of the format.

```yaml
'1': #(The reward id used to link it to a tier) (DONT USE THE SAME NUMBER TWICE)
  type: item #(Reward type)
  name: "Something cool" #(Name for booster message)
  lore-addon: #(Reward description)
    - '&7 - &eWOAH! Something cool' #(Reward description)
  items: #(List of items it will give the player)
    '1': # The first item reward (required) #
      material: diamond_block:0 #(Block/item you want to give)
      amount: 1 #(Amount of block/item you want to give)
      name: '' #(Custom block/item name) (Can be left null for default name) 
      lore: [] #(Custom block/item description) (Can be left null for default name) 
      glow: true #(If the block/item will have a enchantment glow)
    '2': # The second item reward (not required) -> You can have more than two.
      material: coal_block:0 #Block/item you want to give)
      amount: 1 #(Amount of block/item you want to give)
      name: '' #(Custom block/item name) (Can be left null for default name) 
      lore: #(Custom block/item description) (Can be left null for default name) 
        - '&7An &bawesome &7lore, for an &eawesome &7coal block' #(Description)
```

{% hint style="info" %}
In `item` rewards you can also use exact copy of item. [Read more](../general/custom-item-types.md)
{% endhint %}

**ITEM FORMAT:**

Here is a example of giving a diamond sword with a custom name and lore to the player.

```yaml
'1':
  type: item
  name: "Something cool"
  lore-addon:
    - '&7 - &eWOAH! Something cool'
  items:
    '1':
      material: diamond_sword:0
      amount: 1
      name: '&4MIGHTY SWORD'
      lore:
        - '&7Used to slay foes!' 
```

**MONEY FORMAT BREAKDOWN**

{% hint style="warning" %}
Money rewards require Vault and economy plugin which is compatible with Vault
{% endhint %}

Before we start you need to understand what you are editing and what each line of the format means and what it does. Below is a explanation next to each section of the format.

```yaml
'1': #(The reward id used to link it to a tier) (DONT USE THE SAME NUMBER TWICE)
  type: money #(Reward type)
  name: "$100" #(Name for booster message)
  lore-addon: #(Reward description)
    - '&6 - $100' #(Reward description)
  value: 100 #(Money given to player)
```

**MONEY FORMAT:**

Here is a example where player get $250

```yaml
'1':
  type: command # You can still use commands to give items :)
  name: "$250"
  lore-addon:
    - '&6 - $250'
  value: 250
```

## Reward variables (+ boosters support)

Sometimes, you want to create one reward for multiple tiers. Let's say that you want to create reward which gives money to player (`money` type). This reward should be increased by $100 on every tier, so on 5th tier player get $500, on 8th $800 etc. You can create that using variables.

```yaml
'1': # The unique id of the reward
  type: money 
  name: "$%value%"
  variables: # List of variables
    value: "(100 * %tier%) * (1 + (%booster% / 100))" # %value% reward
  lore-addon:
    - '&7 - &eMoney ($%value%)'
  value: '%value%' # Given money - %value% variable
```

In this case player gets `(100 * %tier%) * (1 + (%booster% / 100))` money.

* `(100 * %tier%)` - $100 multiplied by tier
* `* (1 + (%booster% / 100))` - [Reward boosters](../features/boosters.md) support

Ofc, you can create multiple variables with custom names in the same reward

#### ADDING ENCHANTMENTS

Make sure to use lowercase for enchantment IDs. You can also add enchantments from AdvancedEnchantments.

```yaml
'1':
  type: item
  name: "Jben's Sword"
  lore-addon:
    - '&7 - &eForged in the Abyss, the Shadowrend Blade is a weapon of immense power.
  items:
    '1':
      material: netherite_sword:0
      amount: 1
      name: '&4Shadowrend Blade'
      lore:
        - '&7Forged in the Abyss'
      enchants:
        - 'unbreaking:1'
        - 'strike:1'
```
