# Creating & Configuring rewards

AdvancedChallenges offers an extensive configuration of reusable rewards. You can modify them in `plugins/AdvancedChallenges/rewards/common-rewards.yml` folder.

## Configuration

### Common configuration

```yaml
"2": # Reward unique ID
    name: "Shiny diamond" # Reward display name
    whitelisted-servers: [] # List of servers where reward can be claimed. Use [] to disable it
    # List of PlaceholderAPI requirements which player has to meet to get that reward
    # It also allows to use %contribution% placeholder which returns player's contribution percent
    requirements:
        - "%contribution% > 33.34"

    # Custom variables which may be used in value field
    # You can use math formulas, placeholderapi placeholders and custom placeholders:
    # %contribution% - player's contribution %
    # %level% - challenge / streak level
    #
    # `* (1 + (%booster% / 100.0))` - adds rewards booster support
    variables:
        amount: "FLOOR(3 * (%contribution% / 100.0)) * (1 + (%booster% / 100.0))"
    type: <see-below>
    value: <see-below>
```

### Command reward

```yaml
type: command
# List of commands executed by console
# %player% - player's name
# %amount% - custom placeholder made in variables section
value:
    - "eco give %player% %amount%"
```

### Item reward

```yaml
type: item
# Item configuration
value:
    type: diamond
    name: "&6Shiny diamond"
    dynamicAmount: "%amount%" # Custom placeholder from variables section
```

### Money reward (Vault required)

```yaml
type: money
value: "%amount%" # Custom placeholder from variables section
```
