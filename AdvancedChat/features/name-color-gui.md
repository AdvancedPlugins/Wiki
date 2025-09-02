---
description: Let players pick their chat color!
---

# 🎨 Name Color GUI

Name Color Customization is an EULA-compliant perk that allows players to personalize their chat experience with custom colors, including gradients. This feature lets players distinguish themselves in chat, enhancing their interaction and participation on the server.

## Configuration: `menus/nameColorMenu.yml`

This menu can be fully customised, all items in it can be moved / created and removed. Item Configuration guide: [https://wiki.advancedplugins.net/configuration/config-items](https://wiki.advancedplugins.net/configuration/config-items)

{% code title="menus/nameColorMenu.yml" lineNumbers="true" fullWidth="true" %}
```yaml
name: "&aName Color"
size: 36

items:
  filler:
    type: BLACK_STAINED_GLASS_PANE
    name: ' '
  31:
    type: PAPER
    name: '&cClear your name color.'
    action: CLEAR_NAME
  '30':
    name: '&cPrevious Page'
    action: PREVIOUS_PAGE
    head: eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvODFjOTZhNWMzZDEzYzMxOTkxODNlMWJjN2YwODZmNTRjYTJhNjUyNzEyNjMwM2FjOGUyNWQ2M2UxNmI2NGNjZiJ9fX0=
  '32':
    name: '&cNext Page'
    action: NEXT_PAGE
    head: eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMzMzYWU4ZGU3ZWQwNzllMzhkMmM4MmRkNDJiNzRjZmNiZDk0YjM0ODAzNDhkYmI1ZWNkOTNkYThiODEwMTVlMyJ9fX0=
  '35':
    type: WOODEN_DOOR
    name: '&cClose the menu'
    action: CLOSE

settings:
  # Slots in which colors can be displayed
  colorSlots: 9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26

  colorItem:
    name: "%color_name% &rName Color"
    lore:
      - '&7Click here to enable this name color.'
  noPermissionItem:
    name: "%color_name% &rName Color"
    lore:
      - '&cYou do not have permission to use this name color.'
      - '&7You can purchase this name color at &bour store!'

  # Permission: advancedchat.namecolor.<key> e.g. advancedchat.namecolor.white
  colors:
    white:
      format: "<white>%name%</white>"
      name: "&fWhite"
      material: WHITE_STAINED_GLASS_PANE
    dark_blue:
      format: "<dark_blue>%name%</dark_blue>"
      name: "&1Dark Blue"
      material: BLUE_STAINED_GLASS_PANE
    dark_green:
      format: "<dark_green>%name%</dark_green>"
      name: "&2Dark Green"
      material: GREEN_STAINED_GLASS_PANE
    dark_aqua:
      format: "<dark_aqua>%name%</dark_aqua>"
      name: "&3Dark Aqua"
      material: CYAN_STAINED_GLASS_PANE
    dark_red:
      format: "<dark_red>%name%</dark_red>"
      name: "&4Dark Red"
      material: RED_STAINED_GLASS_PANE
    dark_purple:
      format: "<dark_purple>%name%</dark_purple>"
      name: "&5Dark Purple"
      material: PURPLE_STAINED_GLASS_PANE
    gold:
      format: "<gold>%name%</gold>"
      name: "&6Gold"
      material: YELLOW_STAINED_GLASS_PANE
    gray:
      format: "<gray>%name%</gray>"
      name: "&7Gray"
      material: LIGHT_GRAY_STAINED_GLASS_PANE
    dark_gray:
      format: "<dark_gray>%name%</dark_gray>"
      name: "&8Dark Gray"
      material: GRAY_STAINED_GLASS_PANE
    blue:
      format: "<blue>%name%</blue>"
      name: "&9Blue"
      material: LIGHT_BLUE_STAINED_GLASS_PANE
    green:
      format: "<green>%name%</green>"
      name: "&aGreen"
      material: LIME_STAINED_GLASS_PANE
    aqua:
      format: "<aqua>%name%</aqua>"
      name: "&bAqua"
      material: LIGHT_BLUE_STAINED_GLASS_PANE
    red:
      format: "<red>%name%</red>"
      name: "&cRed"
      material: ORANGE_STAINED_GLASS_PANE
    light_purple:
      format: "<light_purple>%name%</light_purple>"
      name: "&dLight Purple"
      material: PINK_STAINED_GLASS_PANE
    yellow:
      format: "<yellow>%name%</yellow>"
      name: "&eYellow"
      material: YELLOW_STAINED_GLASS_PANE
    bold:
      format: "<bold>%name%</bold>"
      name: "&lBold"
      material: IRON_BLOCK
      lore:
        - '&f&lBold effect will be applied to your chat text.'
    italic:
      format: "<italic>%name%</italic>"
      name: "&f&oItalic&r"
      material: GOLD_BLOCK
      lore:
        - '&f&oItalic effect will be applied to your chat text.'
    underline:
      format: "<underlined>%name%</underlined>"
      name: "&nUnderline&r"
      material: DIAMOND_BLOCK
      lore:
        - '&f&nUnderline effect will be applied to your chat text.'
```
{% endcode %}

### Configuration Details

* **name & size**: Define the inventory menu's title and size, respectively.
* **items**: Sets up specific items within the menu.
  * **filler**: Acts as a placeholder in unused slots to maintain the visual integrity of the menu.
  * **31**: A dedicated slot for an item that allows players to clear their selected name color.

### **Settings**

* **colorSlots**: Identifies the inventory slots allocated for displaying name color options.
* **colorItem**: Describes the format and lore for colors that players have the permission to use.
* **noPermissionItem**: Provides the appearance and lore for colors not accessible to the player, potentially directing them towards purchase options.

### **Chat Colors**

* **colors**: Enumerates the available name color options, including their format, display name, and associated material for the menu.
  * **white**: An example color option. The permission to use this color would be `advancedchat.namecolor.white`.

#### Advantages

* **Enhanced Player Experience**: Offering name color customization encourages player expression and enhances their engagement.
* **EULA Compliant**: As a cosmetic feature, it aligns with Minecraft's EULA, making it a safe choice for server monetization.
* **Extensive Customization**: Supports not just solid colors but also gradients, allowing for more intricate and personalized chat displays.
