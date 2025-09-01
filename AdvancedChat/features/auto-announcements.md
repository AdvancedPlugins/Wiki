---
description: Announce important messages in chat automatically
---

# Auto Announcements

Auto Announcements enhance community engagement by automatically scheduling and broadcasting messages in chat. This feature is perfect for sharing updates, important notices, or just adding a bit of fun to the community environment, ensuring that all members are kept informed and involved without manual effort.

### Configuration: `announcements.yml`

{% code title="announcements.yml" lineNumbers="true" fullWidth="true" %}
```yaml
# Announcements Configuration
enabled: true

# Should announcements order be random?
random: true

# Announcements interval in seconds
interval: 300

order:
  - first
  - second

announcements:
  first:
    - '<gradient:white:aqua:white><strikethrough>                                                                  </gradient>'
    - ' '
    - "  <white>Join our Discord server by using <aqua><click:open_url:'https://discord.gg'>Clicking Here!</click></aqua>"
    - ' '
    - '<gradient:white:aqua:white><strikethrough>                                                                  </gradient>'
  second:
    - '<gradient:white:aqua:white><strikethrough>                                                                  </gradient>'
    - ' '
    - ' <white>Report players violating the rules using <aqua>/report'
    - ' '
    - '<gradient:white:aqua:white><strikethrough>                                                                  </gradient>'
```
{% endcode %}

## Key Settings Explained

* **enabled**: Activates the auto announcements feature.
* **random**: Determines whether announcements are displayed in a random order. When set to `true`, announcements are selected at random; otherwise, they follow the sequence specified in `order`.
* **interval**: Defines the time interval between announcements in seconds. In this example, a new announcement is made every 300 seconds (5 minutes).
* **order**: Specifies the order of announcements when `random` is set to `false`. Announcements will be made in the sequence listed here.
* **announcements**: Contains the actual announcement messages. Each announcement can include multiple lines, styled with formatting codes, including gradients and clickable links.
