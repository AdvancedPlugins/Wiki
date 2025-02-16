# 🎁 Rewards Guide

There are two types of reward formats you can use, one is command format or item format. You may use any plugin's command's in them as long as you use the "%player%" placeholder.

**List of mathematical functions which can be used inside variables -> [check](https://ezylang.github.io/EvalEx/references/functions.html)**

---

**COMMAND FORMAT BREAKDOWN**

Before we start you need to understand what you are editing and what each line of the format means and what it does. Below is a explanation next to each section of the format.

```yaml
"1": #(The reward id used to link it to a tier) (DONT USE THE SAME NUMBER TWICE)
    type: command #(Reward type)
    name: "Announces you achievement" #(Reward description)
    commands: #(Item or Command being excuted when reward is claimed)
        - "broadcast &6%player% reached a key BattlePass tier!!"
```

**COMMAND FORMAT:**

Here is a example using a ExcellentCrates command to give a key to the player.

```yaml
"1":
    type: command # You can still use commands to give items :)
    name: "&e1 Common Key"
    commands:
        - "crate key give %player% Common 1"
```

**MONEY FORMAT BREAKDOWN**

{% hint style="warning" %}
Money rewards require Vault and economy plugin which is compatible with Vault
{% endhint %}

Before we start you need to understand what you are editing and what each line of the format means and what it does. Below is a explanation next to each section of the format.

```yaml
"1": #(The reward id used to link it to a tier) (DONT USE THE SAME NUMBER TWICE)
    type: money #(Reward type)
    name: "$%value%" #(Reward name)
    variables: # List of variables which can be calculated and used in reward and in name
        value: "(3 * (5 * (%level% ^ 2))) * (1 + (%booster% / 100))" # `* (1 + (%booster% / 100))` allows to use reward boosters
    value: "%value%" # Money added for player - %value% is a placeholder of "value" variable (see previous line)
```

**MONEY FORMAT:**

Here is a example of giving $10 per level

```yaml
"1":
    type: money
    name: "+$%value%"
    variables:
        money: "(%level% * 10) * (1 + (%booster% / 100))"
    value: "%money%"
```

**ITEM FORMAT BREAKDOWN**

Before we start you need to understand what you are editing and what each line of the format means and what it does. Below is a explanation next to each section of the format.

```yaml
"1": #(The reward id used to link it to a tier) (DONT USE THE SAME NUMBER TWICE)
    type: item #(Reward type)
    name: "&eWOAH! Something cool" #(Reward description)
    items: #(List of items it will give the player)
        "1": # The first item reward (required) #
            material: diamond_block:0 #(Block/item you want to give)
            amount: 1 #(Amount of block/item you want to give)
            name: "" #(Custom block/item name) (Can be left null for default name)
            lore: [] #(Custom block/item description) (Can be left null for default name)
            glow: true #(If the block/item will have a enchantment glow)
        "2": # The second item reward (not required) -> You can have more than two.
            material: coal_block:0 #Block/item you want to give)
            amount: 1 #(Amount of block/item you want to give)
            name: "" #(Custom block/item name) (Can be left null for default name)
            lore: #(Custom block/item description) (Can be left null for default name)
                - "&7An &bawesome &7lore, for an &eawesome &7coal block" #(Description)
```

**ITEM FORMAT:**

Here is a example of giving a diamond sword with a custom name and lore to the player.

```yaml
"1":
    type: item
    name: "&eWOAH! Something cool"
    items:
        "1":
            material: diamond_sword:0
            amount: 1
            name: "&4MIGHTY SWORD"
            lore:
                - "&7Used to slay foes!"
```
