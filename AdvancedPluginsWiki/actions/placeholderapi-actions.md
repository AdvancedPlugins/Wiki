---
description: Learn how you can integrate almost any other plugin into your actions.
---

# PlaceholderAPI Actions

Actions support PlaceholderAPI’s placeholders. Here you will learn how you can add any plugin, which has PlaceholderAPI's support to your actions.

### PlaceholderAPI - `placeholderapi_match_<PLACEHOLDER>`

**Description:** When the placeholder is resolved for the player, it will progress if the variable is the same as what the placeholder resolves to. E.g if the type was as `placeholderapi_match_essentials_fly` and the variable was yes, if the player was flying the action would progress.

```yaml
type: placeholderapi_match_essentials_fly
variable: 'yes'
required-progress: 5
```

### PlaceholderAPI - `placeholderapi_integer_<PLACEHOLDER>`

This works by matching your listed placeholder to a specific number. If your **PlaceholderAPI's** placeholder was `%player_level%` your action would look like this: `placeholderapi_integer_player_level`\
\
Example, if you wanted to make an action which activates as soon as player reaches experience level 100, you can set up an action looking like this:

```yaml
type: placeholderapi_integer_player_level 
required-progress: 10
```
