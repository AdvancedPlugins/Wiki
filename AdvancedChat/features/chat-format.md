---
description: Learn how to configure chat formats.
---

# 💬 Chat Format



<figure><img src="https://i.imgur.com/aEqrPei.gif" alt=""><figcaption></figcaption></figure>

Chat format files are located in the `plugins/AdvancedChat/format` directory.

### Creating New Formats

To create a custom chat format, you'll need to add a new file to the `plugins/AdvancedChat/format` directory. This file should follow the YAML file format (`.yml`). You can base your new format on the provided examples or start from scratch using the guidelines below.

{% hint style="success" %}
Permission to assign user a format: <mark style="background-color:green;">advancedchat.format.\<format name></mark>
{% endhint %}

### Format File Explained

Below is an explanation of the various sections within a chat format file and how to configure them:

{% code title="format/default.yml" overflow="wrap" lineNumbers="true" fullWidth="true" %}
```yaml
# Here you can configure chat formatting
# Assign format with advancedchat.format.<formatName>

# This is a default format, so it will be applied to everyone by default.
# WE RECOMMEND KEEPING THIS DEFAULT FORMAT (feel free to change anything except the file name).
priority: 100
prefix:
  text: '<gray>[Member]</gray>'
  tooltip:
    - '<gray>%player_name% Information:</gray>'
    - '<gray>Balance: &f%vault_eco_balance%</gray>'
  click: 'RUN_COMMAND:/list'
name:
  text: " <white>%player_name%</white>"
  tooltip:
    - '<gray>%player_name% Information:</gray>'
    - '<gray>Balance: </gray><white>%vault_eco_balance%</white>'
  click: 'RUN_COMMAND:/list'
suffix:
  text: ' %advancedchat_tag%: '
  tooltip:
    - ''
  click: ''
chat:
  text: '%message%'
  tooltip:
    - 'This is a message sent by %player_name%'
  click: ''
# Customisable range. If set to 0, range will be disabled.
# Channel range overrides this range and takes a higher priority.
range: 0.0
```
{% endcode %}

* **priority**: Determines the priority of the format. Higher numbers have higher priority.
* **prefix**: Configuration for the prefix displayed before the player name.
  * **text**: The text of the prefix.
  * **tooltip**: Hover text shown when the mouse is over the prefix.
  * **click**: Action to perform when the prefix is clicked.
* **name**: Configuration for the player name display.
  * Similar to the prefix, it can have text, tooltip, and click configurations.
* **suffix**: Configuration for the suffix displayed after the player name.
* **chat**: Configuration for the chat message itself.
* **range**: Determines the range in which the chat will be visible. A value of 0 disables range limitations.
