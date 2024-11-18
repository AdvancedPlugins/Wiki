# Daily Quests Difficulty

Sometimes we want to make that daily quests have same difficulty every day. I.e. we want to make that daily quests always have 1 hard quest, 3 medium quests and 5 easy quests. It's now possible by using 'difficulty' property.

## Setting quest's difficulty

Firstly, we need to set difficulty of all daily quests. You can set it using in-game editor or by adding `difficulty` property to every daily quest in server files.

Difficulty name can be anything. It can be just one word, or it can be entire sentence with colors, but you need to make sure that quests with same difficulty has same difficulty property.

**Example configuration**

```yaml
  6: # Quest id
    type: throw-projectile
    variable: none
    name: 'Throw and Throw'
    required-progress: 200
    points: 10
    difficulty: medium # <-- Difficulty
    item:
      material: snowball
      name: '&eBaller'
      lore:
        - '&7To complete this quest, you must'
        - '&7throw/shoot 200 projectiles.'
        - '&7Difficulty: &e%difficulty%' # <-- You can also show difficulty in quest's description using %difficulty% placeholder
        - ''
        - '&7(&a%percentage_progress%&7)'
```

## Enabling & Setting strategy

Now we need to configure strategy in `settings.yml`

```yaml
daily-quest-difficulty:
  enabled: true
  strategy:
    easy: 5
    medium: 3
    hard: 1
```

As I said, name od difficulty can be anything, so you can even add `&4&lImpossible Quest` difficulty (sentence with colors)

{% hint style="info" %}
You can also configure i.e. 1 hard quest and 4 random quests by setting:

```yaml
# ...
strategy:
    # ...
    hard: 1
```

and

```yaml
current-season:
    # ...
    daily-quest-amount: 5
    # ...
```
{% endhint %}

```yaml
# ...
strategy:
    # ...
    "&4&lImpossible Quest": 1
```

## Configuring permanent quests

Sometimes, we want to make that one or more daily quests are always available. You can achieve that by adding ids of these quests to `permanent-daily-quest-ids`. Example:

```yaml
permanent-daily-quest-ids: ['1', '3', '5']
```

In this example, daily quests with id 1,3 and 5 will be always available
