---
description: Automatically moderate and punish players for their violations.
---

# 🙂 Auto Moderation

Auto Moderation serves as a vigilant guardian of your server's chat, ensuring continuous oversight and integrity in communications, even during your absence. This system automates the enforcement of chat rules, dealing with spam and other infractions by issuing warnings, kicks, mutes, or bans to offenders based on predefined thresholds.

## Configuration: `config.yml`

#### Customization

This feature allows for significant customization to fit the specific needs and policies of your server. You can set up different actions (warn, kick, mute, ban) to be executed at various thresholds of warnings, tailoring the moderation intensity and response to your community's standards.

#### Benefits

* **Continuous Moderation**: Keeps your chat clean and aligned with your community's values, even when moderators are offline.
* **Automated Rule Enforcement**: Automatically handles violations, saving time and ensuring consistent rule application.
* **Flexible Configuration**: Easily adjust thresholds and responses to find the perfect balance for your server's culture.

### Warning Thresholds

The warning system plays a crucial role in moderating chat by tracking the number of violations each player accumulates. Once a player reaches a certain threshold, predefined actions are automatically triggered.

### **Example Configuration**

{% code title="config.yml" %}
```yaml
warn:
  thresholds:
    3:
      commands:
        - "kick %player% Excessive warnings"
    4:
      commands:
        - "mute %player% 10m Excessive warnings"
```
{% endcode %}

In this example, the server is configured to automatically kick a player after they receive their third warning for rule violations. Upon their fourth warning, the player will be muted for 10 minutes, with the reason being "Excessive warnings".

