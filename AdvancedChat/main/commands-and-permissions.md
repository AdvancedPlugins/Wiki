# ⚒️ Commands & Permissions

## /advancedchat

Main plugin command.

**Alias**: /ac

<table data-full-width="true"><thead><tr><th>Command</th><th>Description</th><th>Permission</th></tr></thead><tbody><tr><td>/ac</td><td>Shows help menu.</td><td>advancedchat.use</td></tr><tr><td>/ac announce</td><td>Announce a message across server.</td><td>advancedchat.command.announce</td></tr><tr><td>/ac reload</td><td>Reloads configuration .</td><td>advancedchat.command.reload</td></tr><tr><td>/ac clear</td><td>Clears the chat.</td><td>advancedchat.command.clear</td></tr><tr><td>/ac info</td><td>Shows basic info.</td><td>advancedchat.command.info</td></tr><tr><td>/ac commands</td><td>Shows list of custom commands.</td><td>advancedchat.command.commands</td></tr></tbody></table>

## /tags

Opens Chat Tags GUI



<table data-full-width="true"><thead><tr><th>Command</th><th>Description</th><th>Permission</th></tr></thead><tbody><tr><td>/tags</td><td>Use the /tags command.</td><td>advancedchat.command.tags</td></tr><tr><td>/tags create &#x3C;id> &#x3C;tag> [material]</td><td>Create a tag from in-game (material is optional)</td><td>advancedchat.command.tags.create</td></tr><tr><td>/tags list [page]</td><td>List all tags</td><td>advancedchat.command.tags.list</td></tr><tr><td>/tags delete &#x3C;id></td><td>Delete a tag</td><td>advancedchat.command.tags.delete</td></tr><tr><td>/tags apply &#x3C;player> &#x3C;tag></td><td>Apply a tag to user (ignores permissions)</td><td>advancedchat.command.tags.apply</td></tr><tr><td></td><td>Access to the specified tag.</td><td>advancedchat.tag.&#x3C;name></td></tr></tbody></table>

## /chatcolor

Opens the Chat Color GUI

<table data-full-width="true"><thead><tr><th>Permission</th><th>Description</th></tr></thead><tbody><tr><td>advancedchat.command.chatcolor</td><td>Use the /chatcolor command.</td></tr><tr><td>advancedchat.chatcolor.&#x3C;name></td><td>Access to the specified chat color.</td></tr></tbody></table>

## /channel

**Alias:** /ch

<table data-full-width="true"><thead><tr><th width="230">Command</th><th width="333">Description</th><th>Permission</th></tr></thead><tbody><tr><td>/channel</td><td>Join / Leave chat channels.</td><td>No permission</td></tr><tr><td>/channels</td><td>List all available channels to the player.</td><td>advancedchat.channels</td></tr><tr><td>/channel join &#x3C;name></td><td>Join a channel</td><td>advancedchat.command.channel.join</td></tr><tr><td>/channel leave &#x3C;name></td><td>Leave a channel</td><td>advancedchat.command.channel.leave</td></tr><tr><td>/channelspy</td><td>Spy on channels </td><td>advancedchat.command.channel.spy</td></tr><tr><td>/channelspy &#x3C;channel/all></td><td>Spy on channels</td><td>advancedchat.command.channel.spy</td></tr><tr><td>/channelunspy &#x3C;channel/all></td><td>Unspy on channels</td><td>advancedchat.command.channel.unspy</td></tr><tr><td>-</td><td>Have access to a specific channel</td><td>advancedchat.channel.join.&#x3C;name></td></tr></tbody></table>

## /message

**Alias**: /msg, /m, /w, /pm

**Permission**: advancedchat.command.msg

## /reply

**Alias**: /r

**Permission**: advancedchat.command.reply

## /ignore

**Permission**: advancedchat.command.ignore

## /spy

**Permission**: advancedchat.command.spy

## /warn

**Permission**: advancedchat.command.warn

## /alertstaff

**Permission**: advancedchat.command.alert

## All Permissions

<table data-full-width="true"><thead><tr><th>Permission</th><th>Description</th></tr></thead><tbody><tr><td><code>advancedchat.chat.talk</code></td><td>Allows players to talk in chat.</td></tr><tr><td><code>advancedchat.chat.mention.allow</code></td><td>Allows players to be mentioned in chat.</td></tr><tr><td><code>advancedchat.chat.mention.use</code></td><td>Allows players to use mentions in chat.</td></tr><tr><td><code>advancedchat.chat.colors</code></td><td>Grants access to use colored text in chat messages.</td></tr><tr><td><code>advancedchat.chat.magic</code></td><td>Grants access to use 'magic' formatting (obfuscated text) in chat.</td></tr><tr><td><code>advancedchat.use</code></td><td>General permission for using AdvancedChat features.</td></tr><tr><td><code>advancedchat.command.alert</code></td><td>Allows sending alerts through AdvancedChat.</td></tr><tr><td><code>advancedchat.channels</code></td><td>Grants access to chat channels features.</td></tr><tr><td><code>advancedchat.command.channel.spy</code></td><td>Allows spying on chat channels.</td></tr><tr><td><code>advancedchat.command.channel.spy.all</code></td><td>Permits spying on all chat channels.</td></tr><tr><td><code>advancedchat.command.channel.spy.channel</code></td><td>Allows spying on a specific chat channel.</td></tr><tr><td><code>advancedchat.command.channel.spy.list</code></td><td>Allows listing all spied chat channels.</td></tr><tr><td><code>advancedchat.command.channel.unspy</code></td><td>Permits stopping spying on chat channels.</td></tr><tr><td><code>advancedchat.command.channel.unspy.all</code></td><td>Allows stopping spying on all chat channels.</td></tr><tr><td><code>advancedchat.command.channel.unspy.channel</code></td><td>Permits stopping spying on a specific chat channel.</td></tr><tr><td><code>advancedchat.command.msg</code></td><td>Allows sending private messages to players.</td></tr><tr><td><code>advancedchat.command.reply</code></td><td>Enables players to reply to the last private message.</td></tr><tr><td><code>advancedchat.command.spy</code></td><td>Grants the ability to spy on private messages.</td></tr><tr><td><code>advancedchat.command.spy.all</code></td><td>Allows spying on all private messages.</td></tr><tr><td><code>advancedchat.command.spy.list</code></td><td>Enables listing all spied conversations.</td></tr><tr><td><code>advancedchat.command.spy.player</code></td><td>Permits spying on private messages of a specific player.</td></tr><tr><td><code>advancedchat.command.unspy</code></td><td>Allows stopping the spying on private messages.</td></tr><tr><td><code>advancedchat.command.unspy.all</code></td><td>Permits stopping spying on all private messages.</td></tr><tr><td><code>advancedchat.command.unspy.player</code></td><td>Allows stopping spying on a specific player's private messages.</td></tr><tr><td><code>advancedchat.command.ignore</code></td><td>Enables players to ignore messages from other players.</td></tr><tr><td><code>advancedchat.command.ignore.list</code></td><td>Allows players to list all ignored players.</td></tr><tr><td><code>advancedchat.command.ignore.all</code></td><td>Grants permission to ignore messages from all players.</td></tr><tr><td><code>advancedchat.admin.command.ignore.all</code></td><td>Admin permission to ignore all players.</td></tr><tr><td><code>advancedchat.command.ignore.player</code></td><td>Allows ignoring messages from a specific player.</td></tr><tr><td><code>advancedchat.admin.command.ignore.player</code></td><td>Admin permission to ignore a specific player.</td></tr><tr><td><code>advancedchat.command.unignore</code></td><td>Permits players to stop ignoring messages from players.</td></tr><tr><td><code>advancedchat.command.unignore.all</code></td><td>Allows players to stop ignoring all players.</td></tr><tr><td><code>advancedchat.admin.command.unignore.all</code></td><td>Admin permission to stop ignoring all players.</td></tr><tr><td><code>advancedchat.command.unignore.player</code></td><td>Permits stopping ignoring messages from a specific player.</td></tr><tr><td><code>advancedchat.admin.command.unignore.player</code></td><td>Admin permission to stop ignoring a specific player.</td></tr><tr><td><code>advancedchat.command.chatcolor</code></td><td>Allows players to change their chat color.</td></tr><tr><td><code>advancedchat.command.tags</code></td><td>Grants access to chat tags features.</td></tr><tr><td><code>advancedchat.command.warn</code></td><td>Permits warning players for chat violations.</td></tr><tr><td><code>advancedchat.command.warn.notify</code></td><td>Notifies staff members of issued warnings.</td></tr><tr><td><code>advancedchat.command.announce</code></td><td>Allows making server-wide announcements.</td></tr><tr><td><code>advancedchat.command.clear</code></td><td>Grants the ability to clear the chat.</td></tr><tr><td><code>advancedchat.command.commands</code></td><td>Provides access to AdvancedChat's command list.</td></tr><tr><td><code>advancedchat.command.info</code></td><td>Permits viewing AdvancedChat plugin information.</td></tr><tr><td><code>advancedchat.command.reload</code></td><td>Allows reloading the AdvancedChat configuration without restarting the server.</td></tr><tr><td><code>advancedchat.ai.bypass.swearing</code><br><code>advancedchat.ai.bypass.sexual</code><br><code>advancedchat.ai.bypass.hate</code><br><code>advancedchat.ai.bypass.harrassment</code><br><code>advancedchat.ai.bypass.self-harm</code><br><code>advancedchat.ai.bypass.violence</code></td><td>Allows to bypass specific AI filters</td></tr><tr><td><code>advancedchat.bypass.rule.RULE_NAME</code></td><td>Allows to bypass specific rule. RULE_NAME is the file name without extension</td></tr><tr><td><code>advancedchat.ignorejoinformat.FORMAT</code><br><code>advancedchat.ignorequitformat.FORMAT</code></td><td>Allows to ignore seeing join messages. FORMAT is the join/quit message format from joinMessages.yml<br><br><em>Set this permission to false for the OP group/players. For example, with LuckPerms, use the command: <code>/lp user GC permission set advancedchat.ignorejoinformat.default</code> to view join/leave messages</em></td></tr><tr><td><code>advancedchat.bypass.hidechat</code></td><td>Allows the sender's chat message to be seen even for players with hidden chat enabled</td></tr></tbody></table>

