# Settings

Settings are values you can set for each ability. Be it world whitelist, whitelist/blacklist for materials and more.&#x20;

## Examples

Example for ability to Veinmine blocks

{% code lineNumbers="true" fullWidth="false" %}
```yaml
  levels:
    '1':
      chance: 15
      cooldown: 4
      settings:
        whitelist:
          - "COAL_ORE"
          - "COPPER_ORE"
          - "IRON_ORE"
          - "GOLD_ORE"
          - "LAPIS_ORE"
          - "REDSTONE_ORE"
          - "DIAMOND_ORE"
          - "EMERALD_ORE"
          - "NETHER_QUARTZ_ORE"
          - "NETHER_GOLD_ORE"
          - "ANCIENT_DEBRIS"
          - "DEEPSLATE_COAL_ORE"
          - "DEEPSLATE_COPPER_ORE"
          - "DEEPSLATE_IRON_ORE"
          - "DEEPSLATE_GOLD_ORE"
          - "DEEPSLATE_LAPIS_ORE"
          - "DEEPSLATE_REDSTONE_ORE"
          - "DEEPSLATE_DIAMOND_ORE"
          - "DEEPSLATE_EMERALD_ORE"
      effects:
        - 'BREAK_BLOCK @Veinmine'
```
{% endcode %}

## Important for AdvancedEnchantments

Settings must be set for each level, not for whole enchant.&#x20;

## Setting reference table

| Setting        | Description                                                                          |
| -------------- | ------------------------------------------------------------------------------------ |
| worldBlacklist | List of worlds where this ability is blacklisted and won't activate. Case sensitive. |
| blacklist      | Material blacklist (works with certain effects only)                                 |
| whitelist      | Material whitelist(works with certain effects only)                                  |
