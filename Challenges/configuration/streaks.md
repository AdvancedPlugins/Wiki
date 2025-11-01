# Creating & Configuring streaks

AdvancedChallenges add playtime, daily and votes streak which allows players to redeem rewards for completing these actions.

Streaks may be configured in these files:

-   Daily streak - `plugins/AdvancedChallenges/rewards/daily-rewards.yml`
-   Playtime streak - `plugins/AdvancedChallenges/rewards/playtime-rewards.yml`
-   Vote streak (Votifier required) - `plugins/AdvancedChallenges/rewards/vote-rewards.yml`

## Configuration

```yaml
enabled: true # If streak is enabled
name: "Daily Activity" # Streak display name
# If streak > last key from section below, plugin will automatically generate reward basing on the current pattern
# Basing on the default pattern, player will also get rewards on 31, 40, 60, 61, 70, 90 etc.
repeat: true
max-streak: 100 # Max streak
streak / hours / votes:
    # streak: list of rewards
    "1": [daily]
    "10": [daily]
    "30": [daily]
```
