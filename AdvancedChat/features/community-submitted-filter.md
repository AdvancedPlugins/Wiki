---
description: Constant increase of chat protection without an effort from you.
---

# 🤝 Community-Submitted Filter

Enhance your server's chat moderation with the Community Chat Filter, a comprehensive and continually updated collection of over 2800 vulgar words and expressions. This filter, crafted through community contributions, evolves alongside online communication trends, ensuring your moderation efforts remain effective without manual updates.

## Configuration: `swearing.yml`

{% code title="rules/swearing.yml" %}
```yaml
enabled: true
# Bypass permission: advancedchat.bypass.rule.swearing

# This uses custom words list from our GitHub repository
swearWordsDatabase:
  - https://raw.githubusercontent.com/AdvancedPlugins/Chat/main/swear%20words/en.json
  - https://raw.githubusercontent.com/AdvancedPlugins/Chat/main/swear%20words/de.json

# allow swearing in these channels
disabledChannels:
  - sc
# Should the plugin check for swear words in private messages?
inMsg: true

# Should the curse words be obfuscated? (words replaced with asterisks)
# If set to false, the message will not be sent at all.
obfuscate: true

# Message to send when a player swears
action:
  - 'warn %player% Inappropriate language'
  - 'alert %player% Inappropriate language [%message%]'
```
{% endcode %}

#### Key Settings Explained

* **enabled**: Activates the vulgar words filter on your server, ensuring real-time moderation of chat content.
* **swear-words-database**: Specifies the URL to a JSON file hosted on GitHub, containing the list of community-submitted vulgar words. This database is a live resource, regularly updated by contributors.
* **disabledChannels**: Specifies the channels where swearing is allowed.
* **swear-message**: Defines the message that is sent to a player immediately after they use a word or expression listed in the database, urging them not to swear.
* **obfuscate**: When set to `true`, any detected swear words in a player's message are replaced with asterisks, censoring the inappropriate language. If `false`, the original message is suppressed entirely, and not sent.
* **action**: Outlines the consequences for swearing on the server. In this case, the player is warned, and staff are alerted about the incident, including the message content.
