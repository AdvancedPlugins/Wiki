---
description: Learn how to modify any impossible to edit message!
---

# ✒️ Chat Text Customizer

Elevate your server's chat experience with the Chat Text Customizer. This tool surpasses the conventional limitations of plugins and Minecraft itself, offering unparalleled flexibility in message display customization. Whether you aim to modify messages from various plugins or Minecraft's default communications, this customizer facilitates seamless edits, ensuring your chat environment is uniquely yours.

## Key Features

* **Full Compatibility**: Works with messages from any source, be it Minecraft or third-party plugins.
* **Advanced Editing**: Supports gradients, PlaceholderAPI, and more, for dynamic and vibrant chat messages.
* **Versatile Matching**: Utilizes different matching strategies (EQUALS, STARTS\_WITH, ENDS\_WITH, CONTAINS, REGEX) to accurately identify and modify messages.
* **ProtocolLib Requirement**: Ensure you have **ProtocolLib** installed to utilize this feature. You can learn how to add ProtocolLib to your server here: [#step-1-installing-the-plugin](../first-install.md#step-1-installing-the-plugin "mention")

## Configuration Overview

### Message Customization

Customize any chat message leveraging extensive editing capabilities. The customization process involves identifying the target message and applying the desired modifications.

### **Identifying Messages**

Use `findType` to specify how to match the message you intend to replace. This could be an exact match, a prefix, suffix, substring, or a regular expression for complex patterns.

### **Example: Customizing the "Unknown Command" Message**

```yaml
unknownCommand:
  findType: EQUALS
  find: '&fUnknown command. Type "/help" for help.'
  replace:
    0:
      from: '&fUnknown command. Type "/help" for help.'
      to: '&cYou''ve typed an unknown command! Type "/help" for help or use "/discord" to join our Discord server!'
```

This example demonstrates how to replace the default "unknown command" message with a more informative and engaging one.

