---
description: Create custom commands easily.
---

# Custom Commands

Unleash the full potential of your server with the ability to Create Your Own Commands. Tailor your server's functionality to suit your community's needs, from simple message commands to complex gameplay mechanics, enhancing interactivity and personalization.

Tab complete is integrated and supported!

{% code title="commands/report.yml" lineNumbers="true" fullWidth="true" %}
```yaml
baseCommand: /report
description: Report player

command:
  - effects:
      - "MESSAGE:&cCommand usage: /report <player> <reason>! <condition>%arg length% < 2 : %allow%</condition>"
      - "BROADCAST_PERMISSION:advancedchat.admin:&c[Report] %player name% &fhas reported &c%arg-1% &ffor &c%arg-2-END% <condition>%arg length% >= 2 : %allow%</condition>"
      - "MESSAGE:&fYour report has been submitted! Thank you for helping us keep the server clean! <condition>%arg length% >= 2 : %allow%</condition>"

invalidArgs:
  - effects:
      - "MESSAGE:&cCommand usage: /report <player> <reason>!"
```
{% endcode %}

## Configuration Explained

* **baseCommand**: Specifies the command to be used, in this case, `/report`.
* **description**: A brief description of what the command does, useful for documentation and help menus.

### **`command` Section**

This section outlines what happens when the command is executed correctly. It uses a list of `effects` , you can find all effects here: [https://wiki.advancedplugins.net/abilities/effects](https://wiki.advancedplugins.net/abilities/effects)

### **`invalidArgs` Section**

Defines actions to take when the command is used with incorrect arguments, typically to inform the player of the correct usage.

#### Additional Notes

* **Argument Variables**: Use placeholders like `%arg-1%` for the first argument or `%arg-1-4%` for arguments one to four. `%arg-2-END%` captures all arguments from the second to the last, useful for commands needing variable input lengths.
* **Conditions**: Are specified within `<condition>` tags, allowing certain effects to be conditional on the command's input.
* **Disabling Commands**: Change the file extension (e.g., from `.yml` to `.yml.off`) to disable specific commands without deleting them, providing flexibility in command management.
