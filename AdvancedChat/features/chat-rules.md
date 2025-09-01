---
description: Your chat. Your Rules.
---

# Chat Rules

Utilize the Abilities scripting system to craft bespoke chat rules tailored to your server's specific needs. This flexible framework supports a wide array of rule types, from straightforward anti-caps measures to more complex ones like spam prevention, anti-advertising, similarity checks, and beyond. Our system comes with a suite of pre-made rules that are fully editable and configurable, offering a solid foundation for your moderation strategy.

## Example: `caps.yml` for Caps in Chat

```yaml
# Configuration for Caps in Chat
enabled: true
conditions:
  - '%permissions% contains advancedchat.caps || %is op% = true : %stop%'
  - '%caps_percentage% > 70 : %allow%'
effects:
  - 'CANCEL_EVENT'
  - 'MESSAGE:&c&l(!) &c%player name%, please do not use excessive caps.'
  # - 'CONSOLE_COMMAND:warn %player name% Caps' # you could also warn the player here
```

Learn more about abilities here: [https://wiki.advancedplugins.net/abilities/introduction](https://wiki.advancedplugins.net/abilities/introduction)
