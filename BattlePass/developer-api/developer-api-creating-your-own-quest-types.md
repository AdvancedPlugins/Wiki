# Creating Your Own Quest Types

With BattlePass v4, creating your own quest types is quick and simple but there are still a few steps.

1\) Make sure you depend on BattlePass (or soft depend). If you're soft depending, remember to check if the plugin is enabled.

2\) Make a class for your quest and have it extend `ExternalActionContainer`. Use your IDE to automatically implement the required constructor.

3\) Do whatever you wish and use the execute method to actually trigger the event with all the values with wish.

Use this example to explain the rest (most should be explained just by viewing available inputs anyway):

**Don't forget to change `your_plugin_name` and `quest_name`**

```java
public class BlockBreakQuest extends ExternalActionContainer {

    public BlockBreakQuest(JavaPlugin plugin) {
        super(plugin, "your_plugin_name");
    }

    @EventHandler(ignoreCancelled = true)
    public void onBlockBreak(BlockBreakEvent event) {
        Player player = event.getPlayer();
        Block block = event.getBlock();

        super.executionBuilder("quest_name") // Create execution
                .player(player) // Set player
                .root(block) // Set root
                .progressSingle() // Add 1 progress
                .buildAndExecute();  // Execute
    }
}

```

**This example will create quest with type `your_plugin_name_quest_name` **

4\) Now you need to actually register the quest. To do this, you first need to get the quest registry as such:

```java
ActionRegistry actionRegistry = BattlePlugin.getPlugin().getActionRegistry();
```

5\) Now, you can use the `quest` method to register the quest. If it depends on an external plugin, use the `hook` method (checks if the plugin is enabled).

Internal:

```java
actionRegistry.quest(BlockBreakQuest::new);
```

External:

```java
actionRegistry.hook("pluginname", BlockBreakQuest::new);
```

## Useful `ActionExecutionBuilder` methods

* `player(Player player)` - Set player
* `overrideUpdate()` - Set progress to override entire progress
* `canBeAsync()` - Execute asynchronously (don't use when root/subroot uses blocks,items or entities)

---

* `root(String root)` - Set root to string
* `root(Block root)` - Set root to block
* `root(ItemStack root)` - Set root to itemstack
* `root(Entity root)` - Set root to entity
* `root(Material root)` - Set root to material

---

* `subRoot(String key, String value)` - Add subroot with string
* `subRoot(String key, Material value)` - Add subroot with material
* `subRoot(String key, ItemStack value)` - Add subroot with itemstack
* `subRoot(String key, Block value)` - Add subroot with block
* `subRoot(String key, Entity value)` - Add subroot with entity
* `subRoot(ItemStack itemStack)` - Add `item` subroot with itemstack

---

* `progressSingle()` - Add 1 progress
* `progress(BigInteger progress)` - Add progress
* `progress(int progress)` - Add progress
* `progress(double progress)` - Add progress