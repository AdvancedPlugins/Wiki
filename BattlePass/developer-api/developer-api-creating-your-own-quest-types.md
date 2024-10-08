# Creating Your Own Quest Types

With BattlePass v4, creating your own quest types is quick and simple but there are still a few steps.

1\) Make sure you depend on BattlePass (or soft depend). If you're soft depending, remember to check if the plugin is enabled.

2\) Make a class for your quest and have it extend `ActionQuestExecutor`. Use your IDE to automatically implement the required constructor.

3\) Do whatever you wish and use the execute method to actually trigger the event with all the values with wish.

Use this example to explain the rest (most should be explained just by viewing available inputs anyway):

```java
public class BlockBreakQuest extends ActionQuestExecutor {

    public BlockBreakQuest(BattlePlugin plugin) {
        super(plugin);
    }

    @EventHandler(ignoreCancelled = true)
    public void onBlockBreak(BlockBreakEvent event) {
        Player player = event.getPlayer();
        Block block = event.getBlock();

        super.execute("block-break", player, result -> {
            return result.root(block);
        }, replacer -> replacer.set("block", block.getType()));
    }
}
```

4\) Now you need to actually register the quest. To do this, you first need to get the quest registry as such:

```java
ActionRegistry actionRegistry = BattlePlugin.getPlugin().getActionRegistry();
```

5\) Now, you can use the registerQuests method to register the quest. If it depends on an external plugin, use the registerHook method (checks if the plugin is enabled).

Internal:

```java
actionRegistry.quest(instance -> new BlockBreakQuest(instance));
```

External:

```java
actionRegistry.hook("pluginname", instance -> new BlockBreakQuest(instance));
```
