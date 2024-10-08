# Menu Actions

BattlePass is powered in a lot of places by menu actions. Be aware that options like the next page may only be available in menus. The same goes for other dependent options.&#x20;

## Menu Action

The menu action can be used to open a menu for a player anywhere or if they have a menu open, go to the previous or next page.

The menu action also supports conditions. `=` is used to represent something is the same, `!` to represent when something is different.\
\
Additionally, instead of using the menu name, you can also use `close` to close their currently open menu.\
&#x20;Format: `[menu](condition) {menu-name}`\
&#x20;Examples:

```
actions:
  - '[menu](page = 1) {portal}' # If the page is 1, take them to the portal page
  - '[menu](page ! 1) {previous-page}' # If their page is not 1, take them to the previous page
  - '[menu] {next-page}' # Conditions are not required
  - '[menu] {close}' # Closes their currently opened menu
```

## Message Action

The message action is simple and can be used to send a message to a player.\
Where appropriate, you can use the %tier% placeholder such as in the default config.\
&#x20;Format: `[message] {message}`\
&#x20;Example:\
&#x20;![](https://zak.pink/2020/08/Thin-Hairstreak-8604.jpg)

## Sound Action

This will play a sound for a player. You can find a list of sounds for your version by googling Minecraft sound enum.\
\
You can optionally specify the volume and pitch of the sound (it doesn't work for all due to the way Minecraft works).\
&#x20;Format: `[sound]{sound:volume:pitch}` where you can remove volume/or pitch.\
&#x20;Examples:

```
actions:
  - '[sound] {BLOCK_ANVIL_USE}'
  - '[sound] {BLOCK_ANVIL_USE:2}'
  - '[sound] {DOOR_CLOSE:3:2}'
```

## Title/Subtitle Action

This will execute a Title or Subtitle to the player. You can use %player% to use the player's name.\
Format: `[title] {message}`\
&#x20;             `[subtitle] {message}`\
&#x20;Examples:

```
actions:
  - '[title] {Hello World!}'
  - '[subtitle] {Hello %player%}'
```

## Command Action (Since v3.4)

This will execute a command as the player it's triggered for.\
&#x20;You can use %player% to use the player's name.\
&#x20;Format: `[command] {the command}`\
&#x20;Examples:

```
actions:
  - '[command] {bp menu rewards}'
  - '[command] {some-command %player%}'
```

## Console Command Action (Since v3.4)

This will execute a command **as the console**.\
You can use %player% to use the triggered player's name.\
&#x20;Format: `[console-command] {some console command}`\
&#x20;Examples:

```
actions:
  - '[console-command] {bc &c%player% did some thing. IDK what.}'
  - '[console-command] {lp user %player% parent add some-group server="skyblock"}'
```

