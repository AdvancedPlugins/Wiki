# Custom item types in menus & rewards

Currently, there are 3 types of custom items which you can use in menus and rewards.

## Heads

### BattlePass supports both **base64** custom heads and **player names**.&#x20;

To set custom heads in menus, it's as simple as setting correct material. Material format would be `head:<value>`, example with a player head:

```yaml
menu:
  4:
    item:
      material: "head:GC"
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
      material: "head:ewogICJ0aW1lc3RhbXAiIDogMTYyMzA4MTY3Nzk3MSwKICAicHJvZmlsZUlkIiA6ICIzNDQzMzliMGZhMmI0ZDU2OGQ5MmM3NmI5NzgyNmExYSIsCiAgInByb2ZpbGVOYW1lIiA6ICJ0b2phcGlrYWN6dSIsCiAgInNpZ25hdHVyZVJlcXVpcmVkIiA6IHRydWUsCiAgInRleHR1cmVzIiA6IHsKICAgICJTS0lOIiA6IHsKICAgICAgInVybCIgOiAiaHR0cDovL3RleHR1cmVzLm1pbmVjcmFmdC5uZXQvdGV4dHVyZS9mZTVhMTBlOWJiODU4MjYzMDAyMjI1M2UyOTAwNmIxNTEyNTVkODQ3ODQ0ODc0ODFhYTczOGY4YTAzNzNiN2YzIgogICAgfQogIH0KfQ=="
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
      material: "head:%player_name%"
      name: '&ePlayer Head'
```

Useful links:

* [https://mineskin.org](https://mineskin.org) - Create base64 textures from custom player skins
* [https://minecraft-heads.com](https://minecraft-heads.com) - Database of custom skins

## Exact copy of item - Base64

If you want to make exact copy of item in your hand and use it in menu or as reward (useful for custom items), firstly use `/bpa material b64` command in your game. After that, click on output to copy B64 of this item. After that use it as material with `b64:` prefix. Example:

```yaml
material: "b64:rO0ABXNyABpvcmcuYnVra2l0LnV0aWwuaW8uV3JhcHBlcvJQR+zxEm8FAgABTAADbWFwdAAPTGphdmEvdXRpbC9NYXA7eHBzcgA1Y29tLmdvb2dsZS5jb21tb24uY29sbGVjdC5JbW11dGFibGVNYXAkU2VyaWFsaXplZEZvcm0AAAAAAAAAAAIAAkwABGtleXN0ABJMamF2YS9sYW5nL09iamVjdDtMAAZ2YWx1ZXNxAH4ABHhwdXIAE1tMamF2YS5sYW5nLk9iamVjdDuQzlifEHMpbAIAAHhwAAAABHQAAj09dAABdnQABHR5cGV0AARtZXRhdXEAfgAGAAAABHQAHm9yZy5idWtraXQuaW52ZW50b3J5Lkl0ZW1TdGFja3NyABFqYXZhLmxhbmcuSW50ZWdlchLioKT3gYc4AgABSQAFdmFsdWV4cgAQamF2YS5sYW5nLk51bWJlcoaslR0LlOCLAgAAeHAAAA9zdAALUExBWUVSX0hFQURzcQB+AABzcQB+AAN1cQB+AAYAAAAHcQB+AAh0AAltZXRhLXR5cGV0AAxkaXNwbGF5LW5hbWV0AARsb3JldAAIZW5jaGFudHN0AAlJdGVtRmxhZ3N0AAtza3VsbC1vd25lcnVxAH4ABgAAAAd0AAhJdGVtTWV0YXQABVNLVUxMdABNeyJ0ZXh0IjoiIiwiZXh0cmEiOlt7InRleHQiOiI6KSIsIml0YWxpYyI6ZmFsc2UsImNvbG9yIjoiZ29sZCIsImJvbGQiOnRydWV9XX1zcgATamF2YS51dGlsLkFycmF5TGlzdHiB0h2Zx2GdAwABSQAEc2l6ZXhwAAAAA3cEAAAAA3QAfnsidGV4dCI6IiIsImV4dHJhIjpbeyJ0ZXh0IjoiWWVhaCwgcmVhZGluZyB3aWtpIGlzIGltcG9ydGFudCIsIml0YWxpYyI6ZmFsc2UsInVuZGVybGluZWQiOnRydWUsImNvbG9yIjoieWVsbG93IiwiYm9sZCI6dHJ1ZX1dfXQAAiIidABBeyJ0ZXh0IjoiIiwiZXh0cmEiOlt7InRleHQiOiJ+IEJhdHRsZVBhc3MgRGV2IiwiY29sb3IiOiJ3aGl0ZSJ9XX14c3IAN2NvbS5nb29nbGUuY29tbW9uLmNvbGxlY3QuSW1tdXRhYmxlQmlNYXAkU2VyaWFsaXplZEZvcm0AAAAAAAAAAAIAAHhxAH4AA3VxAH4ABgAAAAF0ABJtaW5lY3JhZnQ6aW5maW5pdHl1cQB+AAYAAAABc3EAfgAOAAAAAXNxAH4AHwAAAAF3BAAAAAF0AA1ISURFX0VOQ0hBTlRTeHNxAH4AAHNxAH4AA3VxAH4ABgAAAARxAH4ACHQACHVuaXF1ZUlkdAAEbmFtZXQACnByb3BlcnRpZXN1cQB+AAYAAAAEdAANUGxheWVyUHJvZmlsZXQAJDczOGU5Zjg5LWNmZjktNDQzNS1hYTVmLTQ5ZjNhYWVkYTAwNHQABktQR19UQnNxAH4AHwAAAAF3BAAAAAFzcgAXamF2YS51dGlsLkxpbmtlZEhhc2hNYXA0wE5cEGzA+wIAAVoAC2FjY2Vzc09yZGVyeHIAEWphdmEudXRpbC5IYXNoTWFwBQfawcMWYNEDAAJGAApsb2FkRmFjdG9ySQAJdGhyZXNob2xkeHA/QAAAAAAADHcIAAAAEAAAAANxAH4AMHQACHRleHR1cmVzdAAFdmFsdWV0AlRld29nSUNKMGFXMWxjM1JoYlhBaUlEb2dNVGN5T0RjMU5USTNNemN6TkN3S0lDQWljSEp2Wm1sc1pVbGtJaUE2SUNJM016aGxPV1k0T1dObVpqazBORE0xWVdFMVpqUTVaak5oWVdWa1lUQXdOQ0lzQ2lBZ0luQnliMlpwYkdWT1lXMWxJaUE2SUNKTFVFZGZWRUlpTEFvZ0lDSnphV2R1WVhSMWNtVlNaWEYxYVhKbFpDSWdPaUIwY25WbExBb2dJQ0owWlhoMGRYSmxjeUlnT2lCN0NpQWdJQ0FpVTB0SlRpSWdPaUI3Q2lBZ0lDQWdJQ0oxY213aUlEb2dJbWgwZEhBNkx5OTBaWGgwZFhKbGN5NXRhVzVsWTNKaFpuUXVibVYwTDNSbGVIUjFjbVV2T0Roa1pqZ3lZelpsTTJZeE9USTVaRFZqTWpZeVl6WmlNRGxoWVdaaE16RTRNVGt4TW1WaU56UTJNbU5pWXpreU16SmtNRFZpWWpjeU5tUmlNakl4WmlJS0lDQWdJSDBzQ2lBZ0lDQWlRMEZRUlNJZ09pQjdDaUFnSUNBZ0lDSjFjbXdpSURvZ0ltaDBkSEE2THk5MFpYaDBkWEpsY3k1dGFXNWxZM0poWm5RdWJtVjBMM1JsZUhSMWNtVXZNak0wTUdNd1pUQXpaR1F5TkdFeE1XSXhOV0U0WWpNell6SmhOMlU1WlRNeVlXSmlNakExTVdJeU5EZ3haREJpWVRka1pXWmtOak0xWTJFM1lUa3pNeUlLSUNBZ0lIMEtJQ0I5Q24wPXQACXNpZ25hdHVyZXQCrFNzNmxxb2RDYmF1VWEzQVVoaXhXQkZzMVBWcVk5QXdlS1RiSnhXcTVabnF5TVlXYlYyQjZwUnpZTEs3UkR2M3NJMHhSSlZObGhHWWhpWVYvQnJCRjYvQjFnWDNVZ3htMVVZYnBvMHp6SzMrMDR4dVNLZHZjZVcrOUp3V2dZblFQR2NPeEcxMW1NYy9RM0pCSkJZV0FLVlVpbDJQSk0zbGxtQzhSQkQ2bGJyRFYyVXJEeUltMnZDVm5aamh1OGJFVCtFZDJWdFpTcmkvTmxXNzNnRGVxbEVMSERndlhiNlJXb05DOUFyMEd2U001N0xnVTFaampwbGx6WHFXbUptRDhDbTNHVFNSZ1VmQ29qam9UYzBTVTl1eGJyVnM3SEhpbGx0ZEhuT0RFQjNYaXoycmYxcnkxQTFYUnlDTXZaTE44TElTSEVJSU5KRlk5ZzMyNDExTTkvNUpsRzNVbXFwQVo4cEFVWE9ITHVuYkhvTkM0eENXNTE1UndEUG56aHlwcW9laElYWnZxR05rN1FZZU5obXNvWXZQR0xJWWlLNDVEcDZFREJwZGdoRlkwaVkzeGQ3S2h2akMzQXliekpBeUxjbGdzZG82TERCM05WTHB6ZithYUlrb1hHaWxCdEVtV1R5SmRrajVLSnRGdHlIY2ZlVUVmMzFhTTl4d2ROUUMwNWJtbDlPNWxyOXQvekZ2SUNJMzNlN1MxMEdMK1p3c29uMWFKMWV6QUgzTGJLL2ZKVkhCNEFvdEhPK3IzOW10cGtPU3JIZkR4NDlEMFNBcDdmUTlxc3pQU3ppc1ZOc1VKQnRRS1ZmaDFyc3hjajRUdVA1cm5VaUdvTWxDQnE1amUwN3hEZXhzOUhWODF3UWs1bTJMRnFnYWNUN04wZjVWMHFRQktLeGlrdS9vPXgAeA=="
```

## ItemsAdder

To use item from itemsadder, set material as id of that item with `itemsadder:` prefix.

```yaml
material: "itemsadder:my_item"
```