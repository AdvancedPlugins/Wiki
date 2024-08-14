# 😁 Custom Heads in Menus

### AdvancedJobs supports both **base64** custom heads and **player names**.&#x20;

To set custom heads in menus, it's as simple as setting correct material. Material format would be `head:<value>`, example with a player head:

```yaml
menu:
  4:
    item:
      material: head:GC
      name: '&eSeason 1 Battle Pass'
      lore:
        - '&7%pass_type% Battle Pass'
        - ''
        - '&7Week &f%week%'
        - ''
        - '&eStatistics'
        - '&f&l * &7Tier &f%tier%'
        - '&f&l * &7Points &f%points%&8/&f%required_points%'
```

Example with **base64** (custom head/skin):

```yaml
menu:
  '4':
    item:
      material: head:ewogICJ0aW1lc3RhbXAiIDogMTYyMzA4MTY3Nzk3MSwKICAicHJvZmlsZUlkIiA6ICIzNDQzMzliMGZhMmI0ZDU2OGQ5MmM3NmI5NzgyNmExYSIsCiAgInByb2ZpbGVOYW1lIiA6ICJ0b2phcGlrYWN6dSIsCiAgInNpZ25hdHVyZVJlcXVpcmVkIiA6IHRydWUsCiAgInRleHR1cmVzIiA6IHsKICAgICJTS0lOIiA6IHsKICAgICAgInVybCIgOiAiaHR0cDovL3RleHR1cmVzLm1pbmVjcmFmdC5uZXQvdGV4dHVyZS9mZTVhMTBlOWJiODU4MjYzMDAyMjI1M2UyOTAwNmIxNTEyNTVkODQ3ODQ0ODc0ODFhYTczOGY4YTAzNzNiN2YzIgogICAgfQogIH0KfQ==
      name: '&eSeason 1 Battle Pass'
      lore:
        - '&7%pass_type% Battle Pass'
        - ''
        - '&7Week &f%week%'
        - ''
        - '&eStatistics'
        - '&f&l * &7Tier &f%tier%'
        - '&f&l * &7Points &f%points%&8/&f%required_points%'
```

### Player's head in GUI

Since 3.12.5, you are able to shown the user which opened the gui head. The format for material is using PlaceholderAPI, and you must have the `Player` ecloud extension.

```yaml
menu:
  '4':
    item:
      material: head:%player_name%
      name: '&ePlayer Head'
```

Useful links:

* [https://mineskin.org](https://mineskin.org) - Create base64 textures from custom player skins
* [https://minecraft-heads.com](https://minecraft-heads.com) - Database of custom skins
