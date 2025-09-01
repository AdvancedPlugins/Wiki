---
description: Create and use chat channels.
---

# Channels

Chat Channels offer a structured way to organize conversations on your Minecraft server. By creating separate channels for various topics, games, or private discussions, you ensure that every conversation is placed appropriately, maintaining clarity and focus in server communications.

## Configuration: channels.yml

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

quick-message:
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

## Overview of Settings

* **Permissions**: Different permissions allow users to join channels, list available channels, automatically join channels upon server join, and leave channels.
* **prefix**: Configures the appearance of channel names in chat messages.
  * **enabled**: When `true`, enables the prefix.
  * **channelPrefix**: The format of the prefix, including placeholders for channel color and name.
* **quick-message**: Allows users to send messages to a specific channel quickly using a designated character.
  * **char**: The character used to indicate a quick message.

## Channel Configuration

Each channel is uniquely identified and configured within the `channels` section:

* **sc**: An example channel identifier, short for "Staff Chat".
  * **name**: The human-readable name of the channel.
  * **color**: Specifies the color of the channel name in chat, using Minecraft formatting codes.
  * **alwaysVisible**: If `true`, messages from this channel are visible to all players with the necessary permissions, regardless of their current channel.
  * **sameWorld**: Restricts messages to players in the same world as the sender when `true`.
  * **range**: Defines the chat visibility range. A value of `0` disables range restrictions.
  * **priority**: Channels with lower priority numbers are listed first in the channel list and may be considered default channels for new players.
