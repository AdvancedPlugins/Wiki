# Commands

* /bp (/battlepass)
  * `/bp about` -> Displays plugin version info.
  * `/bp help` -> Gives available battlepass commands.
  * `/bp stats` -> Gives your BattlePass stats, set in the lang.yml.
  * `/bp open <menu name>` -> Opens the specified menu.
* /bpa (/battlepassadmin)
  * `/bpa reload` -> Reloads all the reloadable files.
  * `/bpa give balance <player> <amount>` - Give a player internal balance (used with internal method on reward-excess-points).
  * `/bpa remove balance <player> <amount>` - Takes away a player's internal balance (used with internal method on reward-excess-points).
  * `/bpa set balance <player> <amount>` - Sets a player's internal balance (used with internal method on reward-excess-points).
  * `/bpa set pass <player> <pass type>` -> Sets a players pass type.
  * `/bpa set pass online/all <pass type>` -> Mass set lots of players' pass types.
  * `/bpa set points <player> <points>` -> Set a players points.
  * `/bpa give points <player> <points>` -> Give a player points.
  * `/bpa delete user <player>` -> Delete all data of a user.
  * `/bpa quest ids <week>` -> List all of the weeks quest ids and their names.
  * `/bpa daily quest ids` -> List all of the daily quest ids and their names.
  * `/bpa reset quest <player> <week> <id>` -> Resets a specific quest of a player.
  * `/bpa progress quest <player> <week> <quest id> <amount>` -> Progress a specific quest of a player.
  * `/bpa progress daily quest <player> <quest id> <amount>` -> Progress a specific quest of a player.
  * `/bpa refresh daily quests` -> Refresh daily quests.
  * `/bpa new season` -> Resets user tiers, pending rewards and points.
  * `/bpa material <block/item>` -> Get the config name of the item you're holding or block you're looking at.
  * `/bpa bypass locked quests <player>` -> Allows the player to bypass week locks and complete quests anyway.
* /bpd (/battlepassdebug)
  * `/bpd start` - Starts debug logging until it is stopped.
  * `/bpd stop` - Stops debug logging.
  * `/bpd create` - Dumps a debug log including data for every online user.
  * `/bpd create <player>` - Creates a debug log including data for the specified player only.
  * `/bpd clear` - Clears the contents of the current debug logger.
