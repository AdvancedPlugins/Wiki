---
description: How to support DiscordSRV
---

# DiscordSRV

## Initial setup

Follow guide on [https://docs.discordsrv.com/installation/initial-setup](https://docs.discordsrv.com/installation/initial-setup)

## Global message

To make global messages sync with discord, you don't need to do any additional steps. From version 1.1.8 we do this on your part. Only thing you might need to turn off is `UseModernPaperChatEvent`, but that's set on false on default, so just double check that.

{% code title="DiscordSRV/config.yml" %}
```yaml
UseModernPaperChatEvent: false
```
{% endcode %}

## **Channel message**

To make the channels work, you need to do only one additional step, and that's to declare the discord channels in config.yml with AdvancedChat Channel ID.&#x20;

* Here is an example:

{% code title="DiscordSRV/config.yml" %}
```yaml
Channels: {"global": "1111111111111111111", "sc": "2222222222222222222"}
```
{% endcode %}

* Here's the channels configuration in AdvancedChat:&#x20;

{% code title="AdvancedChat/channels.yml" %}
```yaml
# Chat Channels
# Permission: advancedchat.channel.join.<channel>
# Permission: advancedchat.channels to list channels using /channels command
# Permission: advancedchat.channel.autojoin.<channel name> to auto join channel on join
# Permission: advancedchat.channel.leave.<channel> to have channel leave permission

# Should player automatically join an available channel on join?
autoJoin: true

prefix:
  enabled: true
  channelPrefix: "%channel_color%[%channel_name%] "
  hover:
    - '<yellow>Join <gold>%channel_name%'
  click: "SUGGEST_COMMAND:!%channel_id% "
  #click: 'RUN_COMMAND:/channel join %channel_id%'

quickMessage:
  char: '!'

channels:
  sc: #Staff chat
    name: 'Staff Chat'
    # %channel_color%
    color: "<green>"
    # Whether channel text should always be visible even when not in channel? You must have channel permission
    alwaysVisible: true
    # Only send to players in the same world
    sameWorld: false
    # Channel messages range
    # If set to 0, range won't be enabled. Set to any other number to enable.
    range: 0
    # Lowest priority will come first
    priority: 10
```
{% endcode %}

{% hint style="info" %}
Make sure your DiscordSRV/config.yml file either doesn't contain or has set `RespectChatPlugins` to true, otherwise cancelled messages will still go through to discord
{% endhint %}

{% code title="DiscordSRV/config.yml" %}
```yaml
# or remove completely from config
RespectChatPlugins: true
```
{% endcode %}

\
Discord -> Minecraft doesn't work
---------------------------------

If Discord messages are not being shown in Minecraft or the console has errors, please try the latest SNAPSHOT build of DiscordSRV before creating a github issue. You can download it here:

[https://snapshot.discordsrv.com/](https://snapshot.discordsrv.com/)
