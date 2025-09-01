---
description: Learn how to design your own prefixes for AdvancedChat!
---

# Prefix Guide

## **Overview**&#x20;

This guide will help you set up custom chat prefixes using the AdvancedChat plugin for Minecraft, which allows for a highly customizable chat experience incorporating elements like rank names and external data via PlaceholderAPI.

## **Editing the Prefix Configuration**

1. **Location**: Navigate to your server's plugin directory at `plugins/AdvancedChat/format`.
2. **File to Edit**: Open the `default.yml` file where you'll find the prefix settings.

## **Customizing the Prefix**

* **Basic Syntax**: Here's a basic prefix configuration example:

```yaml
prefix:
  text: '<gray>[Member]</gray>'
```

Replace `[Member]` with the desired rank or title.&#x20;

{% hint style="info" %}
You can use graphics here from ItemsAdder or Oraxen, we explain placeholders for each here: [itemsadder.md](../main/plugin-integrations/itemsadder.md "mention"),[oraxen.md](../main/plugin-integrations/oraxen.md "mention")
{% endhint %}

You can even use <mark style="color:yellow;">**Gra**</mark><mark style="color:orange;">**dien**</mark><mark style="color:red;">**ts**</mark> here as well [gradients-toasts-and-more.md](../main/gradients-toasts-and-more.md "mention")

* **Adding Hover Text**: Enhance prefixes with hoverable texts that provide additional player information. For example:

```yaml
hover:
  - '<gray>%player_name%<white> Information:</white>'
  - '<gray> •<white> Balance: <white>%vault_eco_balance%</white>'
  - '<gray> •<white> Health: <white>%player_health%/%player_max_health% ❤</white></white>'
  - '<gray> •<white> Level: <white>%player_level%</white></white>'
  - '<gray> •<white> Playtime: <white>%statistic_hours_played% Hours</white></white>'

```

Modify this section to display relevant data like balance, health, and playtime. Use PlaceholderAPI to fetch data from other plugins, e.g., town statistics in Towny.

* **Clickable Commands**: Make prefixes clickable, providing quick actions such as sending a message:

```yaml
click: 'SUGGEST_COMMAND:/msg %player_name% '
```

Adjust the command to suit specific server needs.

**Customization Tips**

* **Using PlaceholderAPI**: Incorporate data from various plugins by using placeholders. For instance, `%towny_town_name%` could show a player's town in a Towny-enabled server.
* **Color and Formatting**: Use Minecraft color codes (`<gray>`, `<white>`, etc.) and formatting codes to style the text.

**Conclusion** Adjust the prefix settings in `default.yml` to create a personalized and informative chat experience on your Minecraft server. Experiment with different placeholders and formatting to match your server's theme and player needs.

This customization allows you to create a dynamic chat environment that can enhance player interaction and server functionality.

\
