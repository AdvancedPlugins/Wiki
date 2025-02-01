# Creating event quests

You can also create event quests. They have own menu and are available in certain period of time. You can create them same as new week (in `quests` folder), but you need to change name to template `event-<id>-quests.yml` (Replace `<id>` with id of your event i.e. `easter`). Also, you need to add this configuration:

```yaml
category:
  start: # Start date
    date: "14/04/2025"
    time: "10:00"
  end: # End date
    date: "27/04/2025"
    time: "22:00"
  name: "Easter Quests" # Name
  required-permission: "" # Required permission
  show-without-permission: true # Show event even if player doesn't have required permission
  see-quests-when-not-active: true # Allow players to see event quests when event isn't active
  item: # Event display icon
    material: "EGG"
    amount: 1
    name: "&6Easter Quests"
    lore:
      - "&eSpecial quests for easter event"
      - "&e14/04/2025 - 27/04/2025"
      - ""
      - "%status%" # %status% will be replaced with messages from lang file: Starts in ..., Ends in..., Ended, No permission
```
