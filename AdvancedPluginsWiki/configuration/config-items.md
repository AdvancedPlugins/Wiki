---
description: How items are configured in AdvancedPlugins
---

# 🔧 Config Items

All AdvancedPlugins use similar item configuration format. You can follow this guide to configure your items.

## Item Configuration

### **type**

item's material&#x20;

### **id**

item's durability

### **amount**

item's amount

### **name**&#x20;

item's custom name

### **lore**

&#x20;item's custom lore

### **item-flags**&#x20;

list of item flags applied to items

### **custom-model-data**&#x20;

&#x20;item's custom model data for custom textures

### **armor-trim**&#x20;

set item's trim material and pattern (new in Minecraft 1.20)

* format: `'MATERIAL;PATTERN'`, e.g. `QUARTZ;COAST`
* Trim material: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimMaterial.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimMaterial.html)
* Trim pattern: [https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimPattern.html](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/inventory/meta/trim/TrimPattern.html)
* **force-glow**&#x20;

set whether item should glow or not

### **enchantments**&#x20;

list of enchantments applied to item

### **custom-enchantments**

&#x20;list of custom enchantments \*_present in AdvancedEnchantments only_

### **rgb-color**&#x20;

item's color (applyable for colored leather armor)

### **nbt**

&#x20;set item's custom nbt (json format)&#x20;

### **owner**

skull's owner. It can be player username or base64

### **unbreakable**&#x20;

set item unbreakable (boolean - true/false)

### **itemsadder**&#x20;

use custom item from ItemsAdder plugin (item's name)

## Configuration Example

```yaml
item: 
  amount: 1
  name: '&cCustom chestplate'
  lore:
    - '&dExclusive from &dVillagers'
  enchantments:
    - 'Protection:20'
    - 'Unbreaking:2'
  custom-enchantments:
    - 'glow:1'
  item-flags:
    - 'HIDE_ENCHANTS'
  custom-model-data: 1
  armor-trim: 'DIAMOND;SILENCE'
  force-glow: false
  rgb-color: 255;0;0
  owner: 40b7ff035bb8761eb40e86f3a17faee349dbcccd84a77703b47e9894a1df847f #base64
  nbt: '{CanDestroy:["minecraft:diamond_ore"],CustomNBTData:"test:true"}'
  unbreakable: true
  itemsadder: 'lava_pickaxe'
```
