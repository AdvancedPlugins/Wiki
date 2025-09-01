---
description: Let players pick their chat color!
---

# 🎨 Chat Color GUI

Chat Color Customization is an EULA-compliant perk that allows players to personalize their chat experience with custom colors, including gradients. This feature lets players distinguish themselves in chat, enhancing their interaction and participation on the server.

## Configuration: `menus/chatColorMenu.yml`

This menu can be fully customised, all items in it can be moved / created and removed. Item Configuration guide: [https://wiki.advancedplugins.net/configuration/config-items](https://wiki.advancedplugins.net/configuration/config-items)

{% code title="menus/chatColorMenu.yml" lineNumbers="true" fullWidth="true" %}
```yaml
name: "&aChat Color"
size: 36

items:
  filler:
    type: BLACK_STAINED_GLASS_PANE
    name: ' '
  31:
    type: PAPER
    name: '&cClear your chat color.'
    action: CLEAR_COLOR

settings:
  # Slots in which colors can be displayed
  colorSlots: 9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26

  colorItem:
    name: "%color name% &rChat Color"
    lore:
      - '&7Click here to enable this chat color.'
  noPermissionItem:
    name: "%color name% &rChat Color"
    lore:
      - '&cYou do not have permission to use this chat color.'
      - '&7You can purchase this chat color at &bour store!'

  # Permission: advancedchat.chatcolor.<key> e.g. advancedchat.color.white
  colors:
    white:
      format: "<white>%message%</white>"
      name: "&fWhite"
      material: WHITE_STAINED_GLASS_PANE
```
{% endcode %}

### Configuration Details

* **name & size**: Define the inventory menu's title and size, respectively.
* **items**: Sets up specific items within the menu.
  * **filler**: Acts as a placeholder in unused slots to maintain the visual integrity of the menu.
  * **31**: A dedicated slot for an item that allows players to clear their selected chat color.

### **Settings**

* **colorSlots**: Identifies the inventory slots allocated for displaying chat color options.
* **colorItem**: Describes the format and lore for colors that players have the permission to use.
* **noPermissionItem**: Provides the appearance and lore for colors not accessible to the player, potentially directing them towards purchase options.

### **Chat Colors**

* **colors**: Enumerates the available chat color options, including their format, display name, and associated material for the menu.
  * **white**: An example color option. The permission to use this color would be `advancedchat.chatcolor.white`.

#### Advantages

* **Enhanced Player Experience**: Offering chat color customization encourages player expression and enhances their engagement.
* **EULA Compliant**: As a cosmetic feature, it aligns with Minecraft's EULA, making it a safe choice for server monetization.
* **Extensive Customization**: Supports not just solid colors but also gradients, allowing for more intricate and personalized chat displays.
