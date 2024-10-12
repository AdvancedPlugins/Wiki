# Special Progress

Define special cases progress multipliers, e.g. when you want a `kill-mob` action to give a different number of progress points depending on the mob, or mining ores.

Better, newer approach for special progress -> [Check](https://wiki.advancedplugins.net/actions/setting-up-and-using-variables)

### Syntax:

```yaml
special-progress:
  - "VARIABLE MULTIPLIER"
```

### Example:

```yaml
type: block-break
variable: coal_ore OR diamond_ore
special-progress:
  - "diamond_ore 5" # Diamond ore will give 5 progress instead of 1
```
