# 🔀 Multi-Type Jobs 

AdvancedJobs allows for the creation of complex job configurations through the use of multi-type jobs. This feature enables a single job to progress through multiple action types, providing a more diverse and engaging gameplay experience.

## Example Configuration

Here's an example of a multi-type job configuration:

```yaml
types:
    1:
        type: crops-planted
        variable: none
        multiplier: 0.25
        special-progress:
            - "nether_wart 2"
    2:
        type: harvest-crops
        variable:
            root: CARROTS
```

In this example, player will progress job in these cases:
* When harvesting carrots (1 point per carrot)
* When planting nether warts (0.25 * 2 = 0.5 point per nether wart)
* When planting other crops (0.25 per planted crop)

**Note**: When using only one type, you can use the old system.
