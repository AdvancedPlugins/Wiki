# Special Progress (custom types progress)

Define special cases progress, e.g. when you want a kill-mob action to give a different number of progress points depending on the mob, or mining ores.

### Syntax:

```yaml
special-progress:
  - "VARIABLE MULTIPLIER"
```

### Example:

```yaml
type: block-break
variable: coal_ore:0 OR diamond_ore:0
special-progress:
  - "diamond_ore:0 5" # Diamond ore will give 5 progress instead of 1
```
