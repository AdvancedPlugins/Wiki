# 🌈 Gradients, Toasts & more

## MiniMessage ----------

AdvancedChat has a full support of MiniMessage - syntax to use gradients, hover, clickable messages and other tricks.

### Gradient

Gradient colored text

`<gradient:[color1]:[color...]:[phase]>`

<div align="left"><figure><img src="https://docs.advntr.dev/_images/gradient_1.png" alt=""><figcaption></figcaption></figure></div>

### Transition

Transitions between colors. Similar to a gradient, but everything is the same color and the phase chooses that color

`<transition:[color1]:[color...]:[phase]>`

<div align="left"><figure><img src="https://docs.advntr.dev/_images/transition_1.png" alt=""><figcaption></figcaption></figure></div>

To learn more about MiniMessage, you can check out this page: [https://docs.advntr.dev/minimessage/format.html](https://docs.advntr.dev/minimessage/format.html)

### Font

Allows to change the font of the text

`<font:key>`

#### Examples

* `Nothing <font:uniform>Uniform <font:alt>Alt </font> Uniform`

<div align="left"><figure><img src="https://docs.advntr.dev/_images/font_1.png" alt=""><figcaption></figcaption></figure></div>

### Small Caps

Convert text to small caps font

`<sc>Example of Small Caps</sc>`

**Examples:**

<div align="left"><figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure></div>

### Selector

`<selector:_sel_[:_separator_]>`

#### Arguments

* `_sel_`, the selector pattern to insert
* `_separator_` (optional), the separator to insert between values the selector matches

#### Examples

* `Hello <selector:@e[limit=5]>, I'm <selector:@s>!`

<div align="left"><figure><img src="https://docs.advntr.dev/_images/selector_1.png" alt=""><figcaption></figcaption></figure></div>

### Insertion

Allow insertion of text into chat via shift click

`<insertion:_text_>`

#### Arguments

* `_text_`, the text to insert

#### Examples

* `Shift-click <insert:test>this</insert> to insert!`

![The result of parsing \`\`Shift-click \<insert:test>this\</insert> to insert!\`\`, shown in-game in the Minecraft client's chat window](https://docs.advntr.dev/_images/insertion_1.png)

### Click

Allows doing multiple things when clicking on the component.

`<click:_action_:_value_>`

#### Arguments

* `_action_`, the type of click event, one of [this list](https://jd.advntr.dev/api/latest/net/kyori/adventure/text/event/ClickEvent.Action.html#enum.constant.summary)
* `_value_`, the argument for that particular event, refer to [the minecraft wiki](https://minecraft.wiki/w/Raw_JSON_text_format)

#### Examples

* `<click:run_command:/seed>Click</click> to show the world seed!`

![The result of parsing \`\`\<click:run\_command:/seed>Click\</click> to show the world seed!\`\`, shown in-game in the Minecraft client's chat window](https://docs.advntr.dev/_images/click_1.png)

### Reset

Close all currently open tags, resetting color/decoration/etc. The reset tag cannot be closed.

`<reset>`

And so much more! Visit the wiki page with full explanation here: [https://docs.advntr.dev/minimessage/format.html](https://docs.advntr.dev/minimessage/format.html)

Some text and messages here are provided from Kyori's Adventure wiki post. Big thanks to them for creating the library.

## Toast Messages -------

AdvancedChat lets you send your message in the form that you wish! You can use this anywhere in the plugin, from locale file to announcements.

### Chat Message

**Example**: `This is a chat message!`

### Action Bar

**Example**: `[ACTION_BAR]This is an action bar message!`

### Title

**Example**: `[TITLE]This is a title!`

### Subtitle

**Example**: `[SUBTITLE]And this is a subtitle!`

### Boss Bar

**Arguments**:

* progress - number with decimal, from 0.0 to 1.0, define progress of bossbar
* color - [https://hub.spigotmc.org/javadocs/spigot/org/bukkit/boss/BarColor.html](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/boss/BarColor.html)
* overlay - PROGRESS, NOTCHED\_6, NOTCHED\_10, NOTCHED\_12, NOTCHED\_20

**Example**: `[BOSS_BAR:1.0:GREEN:PROGRESS]Important announcement here!`

### Achievement

**Arguments**:

* icon - item or block material to be shown
* style - GOAL, TASK, CHALLENGE
* background - background of the announcement. By default `minecraft:textures/gui/advancements/backgrounds/adventure.png`

**Example**: `[ACHIEVEMENT:TOTEM_OF_UNDYING:GOAL]<white>Hey<newline><yellow>%player_name%!`
