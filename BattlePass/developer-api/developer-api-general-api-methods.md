# General API Methods

`BattlePlugin.getPlugin().getActionRegistry()` -> Returns the ActionRegistry which should be used to register internal & external quests.

`CompletableFuture<Optional<User>> getUser(UUID)` -> Returns a completable future of a user (the optional will be present/not present based on whether they were in the cache)

`CompletableFuture<User> getOrLoadUser(UUID)` -> Returns a completable future of a user from the cache, loaded or created (since v3.13).

`Optional<Reward<?>> getReward(String id)` -> Returns a Reward if a command or Reward if an item wrapped in an optional. It will not be present if the reward could not be found.

`long currentWeek()` -> Returns the current week of the battlepass.

`void setPassId(User user, String passId)` -> Sets the pass type of the specified user and gives rewards if set to premium.

`Tier getTier(int tier, String passId)` -> Gets the Tier object for the specified tier and pass type.

`int getRequiredPoints(int tier, String passId)` -> Gets the number of points required to reach the specified tier of a specified pass type.

`void givePoints(User user, int points)` -> Gives the set amount of points to the user.

`void reward(User user, int tier, boolean ignoreRestrictions)` -> Gives the rewards of a specified tier for every pass type to the user (it verifies they have that pass type).

`void reward(User user, String passId, int tier, boolean ignoreRestrictions)` -> Gives the rewards of a specified tier for a specific pass type to the user (it verifies they have that pass type).
