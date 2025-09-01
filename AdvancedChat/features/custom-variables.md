---
description: Ultimate control of variables.
---

# Custom Variables

Custom variables offer a flexible way to enhance chat and message customization within the AdvancedChat plugin. These variables can dynamically display content based on the player's context, the server state, or other criteria, using JavaScript expressions for their values. They can be utilized in chat messages or within the plugin's messaging system for various creative applications.

## Configuration Example: `variables/item.yml`

{% code title="variables/item.yml" lineNumbers="true" fullWidth="true" %}
```yaml
type: CHAT_MESSAGE # If you are parsing a chat message, use CHAT_MESSAGE. This means message will be surrounded in
# [] tags. If you are creating a PLACEHOLDER, it will be using %% formatting, e.g. %item%

# What is the name of the variable? This will be used within the tags, e.g. [item] or %item%
name: item

# Value of this variable, this uses the nashorn engine, so you can use any javascript here.
# You are also able to access Player instance, e.g. player.getName() or player.getUniqueId()
# As well as JavaPlugin using `plugin` variable, e.g. plugin.getServer().getOnlinePlayers().size()
# Event variable is also available, you can use it depending on the event, if this is used for chat it would access AsyncPlayerChatEvent
# Read more in the wiki here: TODO ADD WIKI LINK
# This must always be a string (text)
value: '"x"+player.getItemInHand().getAmount() + " " + capitalize(player.getItemInHand().getType().name())'

# Hover, this can be:
# Text field, saying whatever you want it to say.
# Item field, showing the item in the hover.
# Entity field, showing the entity in the hover.
hover: player.getItemInHand()
```
{% endcode %}

#### Key Elements Explained

* **type**: Determines how the variable is used. `CHAT_MESSAGE` means the variable will be encapsulated in brackets `[]` when used in chat messages. If it's a `PLACEHOLDER`, it will be encapsulated in percentage symbols `%%` (e.g., `%item%`).
* **name**: The identifier for the variable, which will be used within tags in messages (e.g., `[item]` or `%item%` for placeholders).
* **value**: Defines the value of the variable using JavaScript. It can interact with the Minecraft server API, access player information, and even perform operations or transformations on data. In this example, it concatenates the quantity and capitalized name of the item the player is holding.
  * Accessible objects include the `player` instance, allowing you to fetch information such as the player's name (`player.getName()`) or the item they are holding (`player.getItemInHand()`).
  * The `plugin` variable gives access to server-wide information, such as the total number of online players (`plugin.getServer().getOnlinePlayers().size()`).
  * The `event` variable allows interaction with event-specific data, useful when the variable is linked to specific events like chat messages (`AsyncPlayerChatEvent`).
* **hover**: Configures a hover effect for the variable. This can be plain text, an item stack (showing the item's details on hover), or an entity. In the provided example, hovering over the variable in chat will show the item the player is holding.

#### Implementation and Uses

* **Chat Customization**: Enhance player chat messages by incorporating dynamic information like current held items, player stats, or server events.
* **Messaging System**: Use custom variables in automated messages, announcements, or commands within the AdvancedChat plugin to provide personalized information.
* **Interactive Content**: Combine custom variables with hover texts or actions (like clickable links) to create interactive chat experiences.
