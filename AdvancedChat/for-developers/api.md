# API

The `AdvancedChatAPI` provides a comprehensive interface for developers to interact with and extend the functionalities of the AdvancedChat plugin. Located within the `net.advancedplugins.chat.api` package, this API class is the gateway to integrating custom chat features, such as channels, games, formats, and rules, into your Minecraft server.&#x20;

{% hint style="info" %}
**API** is located in `net.advancedplugins.chat.api.AdvancedChatAPI` class.
{% endhint %}

All API Methods

Here are the all API methods, with documentation included

{% code title="AdvancedChatAPI" lineNumbers="true" fullWidth="true" %}
```java
package net.advancedplugins.chat.api;
public class AdvancedChatAPI {
    @Getter
    private static final AdvancedChatAPI api = new AdvancedChatAPI();

    /**
     * Retrieves a chat channel by its name.
     *
     * @param channelName The name of the chat channel.
     * @return The chat channel if found, otherwise null.
     */
    public @Nullable ChatChannel getChatChannel(@NotNull String channelName) {}

    /**
     * Checks if a chat channel exists by its name.
     *
     * @param channelName The name of the chat channel.
     * @return True if the chat channel exists, otherwise false.
     */
    public boolean isChatChannel(@NotNull String channelName) {}

    /**
     * Retrieves a list of all chat channels.
     *
     * @return A list of all chat channels.
     */
    public @NotNull List<ChatChannel> getChatChannels() {}

    /**
     * Retrieves a list of chat channels allowed for a command sender.
     *
     * @param sender The command sender.
     * @return A list of allowed chat channels for the sender.
     */
    public @NotNull List<ChatChannel> getAllowedChatChannels(@NotNull CommandSender sender) {}

    /**
     * Retrieves the chat channel of a player by their UUID.
     *
     * @param uuid The UUID of the player.
     * @return The player's chat channel if found, otherwise null.
     */
    public @Nullable ChatChannel getPlayerChatChannel(@NotNull UUID uuid) {}

    /**
     * Checks if a player is in a chat channel.
     *
     * @param uuid The UUID of the player.
     * @return True if the player is in a chat channel, otherwise false.
     */
    public boolean isPlayerInChannel(@NotNull UUID uuid) {}

    /**
     * Attempts to make a player join a chat channel by their UUID and channel name.
     *
     * @param uuid        The UUID of the player.
     * @param channelName The name of the chat channel.
     * @return True if the player successfully joined the channel, otherwise false.
     */
    public boolean joinChatChannel(@NotNull UUID uuid, @NotNull String channelName) {}

    /**
     * Makes a player join a chat channel by their UUID and channel object.
     *
     * @param uuid    The UUID of the player.
     * @param channel The chat channel object.
     * @return True if the player successfully joined the channel, otherwise false.
     */
    public boolean joinChatChannel(@NotNull UUID uuid, @NotNull ChatChannel channel) {}

    /**
     * Makes a player leave their current chat channel.
     *
     * @param uuid The UUID of the player.
     */
    public void leaveChatChannel(@NotNull UUID uuid) {}

    /**
     * Makes a player leave a specific chat channel by their UUID and channel name.
     *
     * @param uuid        The UUID of the player.
     * @param channelName The name of the chat channel.
     * @return True if the player successfully left the channel, otherwise false.
     */
    public boolean leaveChatChannel(@NotNull UUID uuid, @NotNull String channelName) {}

    /**
     * Makes a player leave a specific chat channel by their UUID and channel object.
     *
     * @param uuid    The UUID of the player.
     * @param channel The chat channel object.
     * @return True if the player successfully left the channel, otherwise false.
     */
    public boolean leaveChatChannel(@NotNull UUID uuid, @NotNull ChatChannel channel) {}

    /**
     * Retrieves a set of channels spied by a player.
     *
     * @param player The player.
     * @return A set of channels spied by the player.
     */
    public @NotNull Set<String> getSpiedChannels(@NotNull Player player) {}

    /**
     * Enables or disables spying on all channels for a player.
     *
     * @param player The player.
     * @param enable True to enable, false to disable.
     */
    public void setAllChannelSpy(@NotNull Player player, boolean enable) {}

    /**
     * Checks if a player is spying on all channels.
     *
     * @param player The player.
     * @return True if the player is spying on all channels, otherwise false.
     */
    public boolean isSpyingOnAllChannels(@NotNull Player player) {}

    /**
     * Checks if a player is spying on a specific channel by name.
     *
     * @param player      The player.
     * @param channelName The name of the chat channel.
     * @return True if the player is spying on the channel, otherwise false.
     */
    public boolean isSpyingOnChannel(@NotNull Player player, @NotNull String channelName) {}

    /**
     * Checks if a player is spying on a specific channel by chat channel object.
     *
     * @param player  The player.
     * @param channel The chat channel object.
     * @return True if the player is spying on the channel, otherwise false.
     */
    public boolean isSpyingOnChannel(@NotNull Player player, @NotNull ChatChannel channel) {}

    /**
     * Removes a channel spy for a player by channel name.
     *
     * @param player      The player from whom to remove the spy.
     * @param channelName The name of the channel to remove from spying.
     * @return True if the spy was removed successfully, otherwise false.
     */
    public boolean removeChannelSpy(@NotNull Player player, @NotNull String channelName) {}

    /**
     * Removes a channel spy for a player by chat channel object.
     *
     * @param player The player from whom to remove the spy.
     * @param channel The chat channel to remove from spying.
     * @return True if the spy was removed successfully, otherwise false.
     */
    public boolean removeChannelSpy(@NotNull Player player, @NotNull ChatChannel channel) {}

    /**
     * Adds a channel spy for a player by channel name.
     *
     * @param player      The player to add the spy.
     * @param channelName The name of the channel to spy on.
     * @return True if the spy was added successfully, otherwise false.
     */
    public boolean addChannelSpy(@NotNull Player player, @NotNull String channelName) {}

    /**
     * Adds a channel spy for a player by chat channel object.
     *
     * @param player The player to add the spy.
     * @param channel The chat channel to spy on.
     * @return True if the spy was added successfully, otherwise false.
     */
    public boolean addChannelSpy(@NotNull Player player, @NotNull ChatChannel channel) {}

    /**
     * Retrieves a set of ignored players for a given player.
     *
     * @param player The player whose ignored players are to be retrieved.
     * @return A set of ignored players.
     */
    public @NotNull Set<String> getIgnoredPlayers(@NotNull Player player) {}

    /**
     * Ignores all players for a given player.
     *
     * @param player The player who will ignore all other players.
     */
    public void setAllPlayerIgnore(@NotNull Player player) {}

    /**
     * Removes all player ignore settings for a given player.
     *
     * @param player The player whose ignore settings are to be removed.
     */
    public void removeAllPlayerIgnore(@NotNull Player player) {}

    /**
     * Checks if a player is ignoring all other players.
     *
     * @param player The player to check.
     * @return True if the player is ignoring all other players, otherwise false.
     */
    public boolean hasAllPlayersIgnored(@NotNull Player player) {}

    /**
     * Checks if a player is ignoring another player by name.
     *
     * @param player      The player to check.
     * @param playerName  The name of the player to check against the ignore list.
     * @return True if the player is ignoring the specified player, otherwise false.
     */
    public boolean hasPlayerIgnored(@NotNull Player player, @NotNull String playerName) {}

    /**
     * Removes an ignored player for a given player.
     *
     * @param player      The player from whom to remove the ignored player.
     * @param playerName  The name of the player to remove from the ignore list.
     * @return True if the ignored player was removed successfully, otherwise false.
     */
    public boolean removePlayerIgnore(@NotNull Player player, @NotNull String playerName) {}

    /**
     * Adds an ignored player for a given player.
     *
     * @param player      The player to add the ignored player.
     * @param playerName  The name of the player to add to the ignore list.
     * @return True if the ignored player was added successfully, otherwise false.
     */
    public boolean addPlayerIgnore(@NotNull Player player, @NotNull String playerName) {}

    /**
     * Checks if a permissible entity can bypass the ignore list.
     *
     * @param permissible The permissible entity to check.
     * @return True if the permissible entity can bypass the ignore list, otherwise false.
     */
    public boolean canBypassIgnore(@NotNull Permissible permissible) {}

    /**
     * Retrieves a set of spied players for a given player.
     *
     * @param player The player whose spied players are to be retrieved.
     * @return A set of spied players.
     */
    public @NotNull Set<String> getSpiedPlayers(@NotNull Player player) {}

    /**
     * Sets a player to spy on all other players.
     *
     * @param player The player who will spy on all other players.
     */
    public void setAllPlayerSpy(@NotNull Player player) {}

    /**
     * Removes spy settings for all players for a given player.
     *
     * @param player The player whose spy settings are to be removed.
     */
    public void removeAllPlayerSpy(@NotNull Player player) {}

    /**
     * Checks if a player is spying on all other players.
     *
     * @param player The player to check.
     * @return True if the player is spying on all other players, otherwise false.
     */
    public boolean isSpyingOnAllPlayers(@NotNull Player player) {}

    /**
     * Checks if a player is spying on another player by name.
     *
     * @param player      The player to check.
     * @param playerName  The name of the player to check against the spy list.
     * @return True if the player is spying on the specified player, otherwise false.
     */
    public boolean isSpyingOnPlayer(@NotNull Player player, @NotNull String playerName) {}

    /**
     * Removes a spy setting for a specific player for a given player.
     *
     * @param player      The player from whom to remove the spy setting.
     * @param playerName  The name of the player to stop spying on.
     * @return True if the spy setting was removed successfully, otherwise false.
     */
    public boolean removePlayerSpy(@NotNull Player player, @NotNull String playerName) {}

    /**
     * Adds a spy setting for a specific player for a given player.
     *
     * @param player      The player to add the spy setting.
     * @param playerName  The name of the player to start spying on.
     * @return True if the spy setting was added successfully, otherwise false.
     */
    public boolean addPlayerSpy(@NotNull Player player, @NotNull String playerName) {}

    /**
     * Retrieves the custom chat color of a player.
     *
     * @param player The player whose custom chat color is to be retrieved.
     * @return The custom chat color of the player, or null if not set.
     */
    public @Nullable CustomChatColor getPlayerCustomColor(@NotNull Player player) {}

    /**
     * Retrieves a custom chat color by its name.
     *
     * @param colorName The name of the custom chat color.
     * @return The custom chat color if found, otherwise null.
     */
    public @Nullable CustomChatColor getCustomColor(@NotNull String colorName) {}

    /**
     * Retrieves a set of players from a cross-server context.
     *
     * @return A set of player names from cross-server.
     */
    public @NotNull Set<String> getCrossServerPlayers() {}

    /**
     * Checks if a command or alias is a custom command.
     *
     * @param cmdOrAlias The command or alias to check.
     * @return True if the command is custom, otherwise false.
     */
    public boolean isCustomCommand(@NotNull String cmdOrAlias) {}

    /**
     * Registers a custom command.
     *
     * @param key           The key for the custom command.
     * @param customCommand The custom command object.
     * @return True if registration was successful, otherwise false.
     */
    public boolean registerCustomCommand(@NotNull String key, @NotNull CustomCommand customCommand) {}

    /**
     * Unregisters a custom command.
     *
     * @param name The name of the custom command to unregister.
     * @return True if the command was unregistered, otherwise false.
     */
    public boolean unregisterCustomCommand(@NotNull String name) {}

    /**
     * Retrieves a map of all custom commands.
     *
     * @return A map containing all custom commands.
     */
    public @NotNull Map<String, CustomCommand> getCustomCommands() {}

    /**
     * Adds a chat format to the formatting handler.
     *
     * @param formatName The name of the chat format.
     * @param format     The chat format object.
     */
    public void addChatFormat(@NotNull String formatName, @NotNull ChatFormat format) {}

    /**
     * Retrieves the chat format for a sender.
     *
     * @param sender The command sender.
     * @return The chat format for the sender.
     */
    public @NotNull ChatFormat getSenderChatFormat(@NotNull CommandSender sender) {}

    /**
     * Retrieves a chat format by its name.
     *
     * @param formatName The name of the chat format.
     * @return The chat format if found, otherwise null.
     */
    public @Nullable ChatFormat getChatFormat(@NotNull String formatName) {}

    /**
     * Checks if chat games are enabled.
     *
     * @return True if chat games are enabled, otherwise false.
     */
    public boolean areChatGamesEnabled() {}

    /**
     * Retrieves the running chat game.
     *
     * @return The running chat game if exists, otherwise null.
     */
    public @Nullable ChatGame getRunningChatGame() {}

    /**
     * Checks if any chat game is currently running.
     *
     * @return True if a chat game is running, otherwise false.
     */
    public boolean isChatGameRunning() {}

    /**
     * Starts a specific chat game.
     *
     * @param game The chat game to start.
     */
    public void startChatGame(@NotNull ChatGame game) {}

    /**
     * Starts a random chat game.
     *
     * @param game The chat game to start.
     */
    public void startRandomChatGame(@NotNull ChatGame game) {}

    /**
     * Retrieves all chat games.
     *
     * @return A map containing all chat games.
     */
    public @NotNull HashMap<String, ChatGame> getChatGames() {}

    /**
     * Retrieves the join message format for a player.
     *
     * @param player The player to get the join message format for.
     * @return The join message format if set, otherwise null.
     */
    public @Nullable JoinMessage getJoinMessageFormat(@NotNull Player player) {}

    /**
     * Opens the chat color menu for a player.
     *
     * @param player The player to open the menu for.
     */
    public void openChatColorMenu(@NotNull Player player) {}

    /**
     * Opens the chat tags menu for a player.
     *
     * @param player The player to open the menu for.
     */
    public void openChatTagsMenu(@NotNull Player player) {}

    /**
     * Retrieves the list of swear words.
     *
     * @return A set of swear words.
     */
    public @NotNull Set<String> getSwearWordList() {}

    /**
     * Processes a message for swear words.
     *
     * @param sender The player sending the message.
     * @param msg    The message to process.
     * @return The result after processing the swear words.
     */
    public @NotNull TextResult processMessageSwear(@NotNull Player sender, @NotNull String msg) {}

    /**
     * Adds a chat rule to the rule handler.
     *
     * @param ruleName The name of the chat rule.
     * @param rule     The chat rule object.
     */
    public void addChatRule(@NotNull String ruleName, @NotNull ChatRule rule) {}

    /**
     * Retrieves a chat rule by its name.
     *
     * @param ruleName The name of the chat rule.
     * @return The chat rule if found, otherwise null.
     */
    public @Nullable ChatRule getChatRule(@NotNull String ruleName) {}

    /**
     * Retrieves all chat rules.
     *
     * @return A map containing all chat rules.
     */
    public @NotNull Map<String, ChatRule> getChatRules() {}

    /**
     * Retrieves a chat tag by its name.
     *
     * @param tagName The name of the chat tag.
     * @return The chat tag if found, otherwise null.
     */
    public @Nullable ChatTag getChatTag(@NotNull String tagName) {}

    /**
     * Retrieves the chat tag name for a player.
     *
     * @param player The player to get the chat tag name for.
     * @return The chat tag name if set for the player, otherwise null.
     */
    public @Nullable String getPlayerChatTagName(@NotNull Player player) {}

    /**
     * Retrieves the chat tag associated with a player.
     *
     * @param player The player to retrieve the chat tag for.
     * @return The chat tag associated with the player, or null if not found.
     */
    public @Nullable ChatTag getPlayerChatTag(@NotNull Player player) {}

    /**
     * Sets a chat tag for a player using the tag name.
     *
     * @param player  The player to set the chat tag for.
     * @param tagName The name of the chat tag to set.
     */
    public void setChatTag(@NotNull Player player, @NotNull String tagName) {}

    /**
     * Sets a chat tag for a player using a ChatTag object.
     *
     * @param player The player to set the chat tag for.
     * @param tag    The ChatTag object to set.
     */
    public void setChatTag(@NotNull Player player, @NotNull ChatTag tag) {}

    /**
     * Retrieves a map of custom variables.
     *
     * @return A map containing custom variables.
     */
    public @NotNull Map<String, CustomVariable> getCustomVariables() {}

    /**
     * Registers a custom variable for a JavaPlugin.
     *
     * @param plugin   The JavaPlugin registering the custom variable.
     * @param variable The custom variable to register.
     */
    public void registerCustomVariable(@NotNull JavaPlugin plugin, @NotNull CustomVariable variable) {}
}
```
{% endcode %}
