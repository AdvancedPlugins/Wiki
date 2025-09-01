---
description: >-
  Here we explain few common issues new users may come across and how to fix
  them.
---

# 💡 Common Issues

## **OP having all Chat Formats, Channels etc.**

By default, OPs have all permissions. Our chat formats, channels and other features are permission based, that means that OP will have access to all these features and all their implementations. To give only a specific implementation to a player, you will need to set all the permissions to negative values.

Here is an example how to do this with LuckPerms:

#### For Chat Format:

```
/lp user USER permission set advancedchat.format.<format name> false
```

#### For Channel

```
/lp user USER permission set advancedchat.channel.join.<channel> false
/lp user USER permission set advancedchat.channel.leave.<channel> false
/lp user USER permission set advancedchat.channel.autojoin.<channel> false
```

