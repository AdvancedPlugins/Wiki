---
description: Excellent Eula friendly perk!
---

# Chat Tags GUI

Chat Tags offer a unique way for players to customize their in-chat appearance with special suffixes following their names, a feature that aligns perfectly with EULA compliance for Minecraft servers. These tags can be integrated with plugins like ItemsAdder or Oraxen to display emojis or icons, enhancing the chat experience with visual flair.

## Default Files

You can find the default configuration here: [https://github.com/AdvancedPlugins/Chat/blob/main/menus/chatTagsMenu.yml](https://github.com/AdvancedPlugins/Chat/blob/main/menus/chatTagsMenu.yml)

## Creating Tags

You can create, edit and apply tags using tags commands, which can be found here: [#tags](../main/commands-and-permissions.md#tags "mention")

## Configuration: menus/chatTagsMenu.yml

This menu can be fully customised, all items in it can be moved / created and removed. Item Configuration guide: [https://wiki.advancedplugins.net/configuration/config-items](https://wiki.advancedplugins.net/configuration/config-items)

{% code title="menus/chatTagsMenu.yml" fullWidth="true" %}
```yaml
# Chat Tags Configuration
name: "&b&lChat Tags"
size: 45

# Should locked tags be shown in the menu?
showLockedTags: true

# Should a space be automatically added before a tag in chat?
# When true, e.g. format: "[Member] playerName [tag]"
# When false, e.g. format: "[Member] playerName[tag]"
addSpaceBeforeTag: true

items:
  0-8:
    type: BLACK_STAINED_GLASS_PANE
    name: ' '
  27-35:
    type: BLACK_STAINED_GLASS_PANE
    name: ' '
  '39':
    name: '&cPrevious Page'
    action: PREVIOUS_PAGE
    head: eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvODFjOTZhNWMzZDEzYzMxOTkxODNlMWJjN2YwODZmNTRjYTJhNjUyNzEyNjMwM2FjOGUyNWQ2M2UxNmI2NGNjZiJ9fX0=
  '40':
    type: PAPER
    name: '&cReset your chat tag.'
    lore:
      - ' &8● &7Click here to &cclear&7 your chat tag.'
    action: RESET_TAG
  '41':
    name: '&cNext Page'
    action: NEXT_PAGE
    head: eyJ0ZXh0dXJlcyI6eyJTS0lOIjp7InVybCI6Imh0dHA6Ly90ZXh0dXJlcy5taW5lY3JhZnQubmV0L3RleHR1cmUvMzMzYWU4ZGU3ZWQwNzllMzhkMmM4MmRkNDJiNzRjZmNiZDk0YjM0ODAzNDhkYmI1ZWNkOTNkYThiODEwMTVlMyJ9fX0=
  '44':
    type: WOODEN_DOOR
    name: '&cClose the menu'
    action: CLOSE

settings:
  # Slots in which colors can be displayed
  tagSlots: 9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26
  tagItem:
    name: "%tag% <white>Chat Tag"
    lore:
      - '<gray>Click here to enable this chat tag.'
  noPermissionItem:
    name: "%tag% <white>Chat Tag"
    lore:
      - '<red>You do not have permission to use this chat tag.'
      - '<gray>You can purchase this chat tag at <aqua>our store!'

  tags: # Permissions are: advancedchat.tag.<tag> e.g. advancedchat.tag.mvp
    hacker:
      format: "<dark_green>[HACKER]</dark_green>"
      material: COMMAND_BLOCK
  .... many more tags
```
{% endcode %}

## Key Settings Explained

* **name**: The title of the chat tags menu.
* **size**: The size of the inventory menu in slots.
* **items**: Defines specific items within the menu, such as the filler item for unused slots and the option to reset the chat tag.
  * **filler**: A placeholder item to maintain the menu's aesthetic.
  * **31**: (example slot) The slot designated for the paper item allowing users to reset their chat tag to default.
* **settings**: Contains configurations for how chat tags are displayed and managed within the menu.
  * **tagSlots**: Specifies which inventory slots can display chat tags.
  * **tagItem**: Describes the appearance and interaction text for chat tags that players have permission to use.
  * **noPermissionItem**: Details the appearance and lore for chat tags that the player does not have permission to use, potentially guiding them towards purchasing options.

### **Chat Tags Configuration**

Example tag:

* **tags**: Defines the available chat tags, their format, and associated permissions.
  * **mvp**: An example tag with a specific format (`&5[MVP]&r`) and material (`DIAMOND`). The permission to use this tag would be `advancedchat.tag.mvp`.

### Utilization and Benefits

* **Personalization**: Chat Tags allow players to customize their chat presence, offering a visible perk for engagement or purchases.
* **EULA Compliance**: As purely cosmetic, chat tags comply with Minecraft's EULA, making them ideal for monetization strategies.
* **Integration**: The possibility to include emojis or icons through plugins broadens the customization options, making each chat tag truly unique.
