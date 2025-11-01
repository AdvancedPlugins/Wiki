# Creating & Configuring challenge categories

Categories are groups of challenges. From these groups, plugin choose specified number of challenges at specified change every specified amount of time. It also allows to configure some default settings.

**NOTE: Categories system may be used to group challenges in menus, but don't have to be used for that**

## Creating category

To create a category, go to `plugins/AdvancedChallenges/challenges` fodler and create a YAML file ended with `-challenges.yml`i.e. `example-challenges.yml`.

## Configuring cateogry

```yaml
category:
    name: "My New Category" # Display name of category
    # Math formula for calculating player's max contribution (in %)
    # You can also use %avg_players% if enabled in settings
    # This placeholder returns an avg amount of players in the last `duration`
    max-percent-per-player: "MAX(33.34, 100 / %avg_players%)" # In this example, player can make (100 / avg_players)% of challenge, but that value can't be lower than 33.34%
    duration: 1d # Challenge duration
    try-every: 1d5m # Time after which challenges from this category are rerolled (recommended to make it `duration` + 5m)
    select-chance: 100.0 # Chance to select any challenge from this category. If the category won't pass this %, none of the challenges will be selected and the timer will be reset
    limit: 3 # Challenges limit
    # These settings will be used for all challenges in this category unless overridden in the challenge itself
    # Not applies for steps and icon
    defaultSettings:
        # Example configuration
        group: "example"
        manual: false
        join-fee: 0

# List of challenges
challenges:
    # Example
    example-1:
        name: ""
        # Other challenge data...
```
