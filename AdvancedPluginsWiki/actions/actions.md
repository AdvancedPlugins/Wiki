---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Actions

<figure><img src="../.gitbook/assets/image.gif" alt=""><figcaption><p><a href="https://mintservers.com/?utm_source=gitbook_wiki&#x26;utm_medium=banner&#x26;utm_content=gitbook"><strong>Sponsored by MintServers. AdvancedPlugins.net integration &#x26; auto updates. Unlimited RAM plan for only $9.99!</strong></a></p></figcaption></figure>

## Internal Action Types (36)

* [**block-break**](actions.md#block-break) - Break backs
* [**block-place** ](actions.md#block-place)- Place blocks
* [**bucket-place**](actions.md#bucket-place) - Place bucket
* [**chat** ](actions.md#chat)- Say something in chat
* [**chat-stripped**](actions.md#chat-stripped) - Saying something in chat but stripped of colour codes _(since v3.0.6)_
* [**right-click**](actions.md#right-click) - Right-click anything
* [**left-click**](actions.md#left-click) - Left click anything
* [**right-click-block** ](actions.md#right-click-block)- Right click a block
* [**left-click-block**](actions.md#left-click-block) - Left click a block
* [**consume**](actions.md#consume) - Consume a consumable
* [**craft**](actions.md#craft) - Craft items
* [**damage-player**](actions.md#damage-player) - Deal damage to players
* [**enchant**](actions.md#enchant) - Enchant an item using an enchant table
* [**enchant-anvil**](actions.md#enchant-anvil) - Enchant an item using an anvil _(since v3.10)_
* [**enchant-all**](actions.md#enchant-all) - Enchant an item using an enchantment table OR anvil _(since v3.10)_
* [**execute-command**](actions.md#execute-command) - Execute a command in chat
* [**fish**](actions.md#fish) - Fishing
* [**gain-experience** ](actions.md#gain-experience)- Gain experience
* [**item-break**](actions.md#item-break) - Have an item break e.g pickaxe, sword
* [**fly** ](actions.md#fly)- Fly
* [**glide** ](actions.md#glide)- Glide
* [**sneak** ](actions.md#sneak)- Sneaking (Shifting)
* [**sprint** ](actions.md#sprint)- Sprinting
* [**swim** ](actions.md#swim)- Swimming
* [**move** ](actions.md#move)- Whenever you move a block regardless of how
* [**kill-mob**](actions.md#kill-mob) - Kill mobs (Use `advancedspawners_kill` for AdvancedSpawners mobs)
* [**kill-player**](actions.md#kill-player) - Kill players
* [**login** ](actions.md#login)**- Login**
* [**milk** ](actions.md#milk)- Milk a cow
* [**playtime** ](actions.md#playtime)- Time played measured in seconds. Must enable in `settings.yml`. _(since v3.10)_
* [**throw-projectile**](actions.md#throw-projectile) - When a player throws any projectile (egg, snowball, etc..). _(since v3.10)_
* [**regenerate** ](actions.md#regenerate)- Regenerate health
* [**ride-mob**](actions.md#ride-mob) - Ride a mob
* [**shear**](actions.md#shear)- Shear a sheep
* [**smelt** ](actions.md#smelt)- Smelt an item in a furnace
* [**tame** ](actions.md#tame)- Tame a pet (Ocelot/Wolf)
* [**honey-extract**](actions.md#honey-extract) - Extract honey
* [**honey-comb-extract**](actions.md#honey-comb-extract) - Extract honey comb with shears
* [**breed**](actions.md#breed) - Breed an entity
* [**brew**](actions.md#brew) - Brew a potion

## External Action Type (100+)

* **AdvancedSpawners (**[**https://advancedplugins.net/item/2**](https://advancedplugins.net/item/2)**)**
  * [**advancedspawners\_kill** ](https://as.advancedplugins.net/)- Killing custom mobs
* **McMMO** (New)
  * [**mcmmo\_gain\_exp**](actions.md#mcmmo-mcmmo_gain_exp) - Gain experience in skill
  * [**mcmmo\_level\_up\_skill**](actions.md#mcmmo-mcmmo_level_up_skill) - Level up an mcmmo skill
  * [**mcmmo\_level\_total\_skill**](actions.md#mcmmo-mcmmo_level_total_skill) - Level up an mcmmo skill (returns total level of skill)
* **MBedWars**
  * [**mbedwars\_break\_bed**](actions.md#mbedwars_break_bed) - When bed is broken
  * [**mbedwars\_kill**](actions.md#mbedwars_kill) - When kill is achieved
  * [**mbedwars\_stat\_change** ](actions.md#mbedwars_stat_change)- Stat changes
  * [**mbedwars\_buy\_item** ](actions.md#mbedwars_buy_item)- When item is bought
  * [**mbedwars\_join\_arena**](actions.md#mbedwars_join_arena) - When an arena is joined
  * [**mbedwars\_team\_eliminate** ](actions.md#mbedwars_team_eliminate)- When a teammate is eliminated
* **ChestShop**
  * [**chestshop\_create**](actions.md#chestshop-chestshop_create) - Placing/creating a chest shop.
  * [**chestshop\_buy**](actions.md#chestshop-chestshop_buy) - Buying items from a player's chest shop.
  * [**chestshop\_sell**](actions.md#chestshop-chestshop_sell) - Selling items to another player via a chest shop.
  * [**chestshop\_spend**](actions.md#chestshop-chestshop_spend) - Spending money at a chest shop.
  * [**chestshop\_profit**](https://app.gitbook.com/s/-MVKgJtPKw7gQhR_Osin/features/s#chestshop---chestshop_profit) - Making money from a chest shop.
  * **chestshop\_destroy** - Destroying a chest shop.
* **AdvancedEnchantments**
  * [**advancedenchantments\_enchant**](actions.md#advancedenchantments-advancedenchantments_enchant) - Adding a custom enchant to an item.
* **ASkyBlock**
  * [**askyblock\_create\_island**](actions.md#askyblock-askyblock_create_island) - Creating an island.
  * [**askyblock\_create\_warp**](actions.md#askyblock-askyblock_create_warp) - When a player creates a warp.
* **AuctionHouse by Kludge**
  * [**auctionhouse\_kludge\_list**](actions.md#auctionhouse-by-kludgemonkey-auctionhouse_list) - Listing an item on the auction house.
  * [**auctionhouse\_kludge\_list\_singular**](actions.md#auctionhouse-by-kludgemonkey-auctionhouse_list_singular) - Listing an item on the auction house.
  * [**auctionhouse\_kludge\_buy**](broken-reference/) - Buying an item from the auction house.
  * [**auctionhouse\_kludge\_buy\_singular**](broken-reference/) - Buying an item from the auction house.
  * [**auctionhouse\_kludge\_sell**](broken-reference/) - Successfully selling an item on the auction house.
  * [**auctionhouse\_kludge\_sell\_singular**](broken-reference/) - Successfully selling an item on the auction house.
  * [**auctionhouse\_kludge\_profit**](broken-reference/) - Making x money from selling.
  * [**auctionhouse\_kludge\_spend**](broken-reference/) - Spending x money on the auction house.
* **AutoSell**
  * [**autosell\_break**](actions.md#autosell-autosell_break) - Alternative to block\_break when autosell is applied (autosell breaks the normal action).
* **BedWars1058**
  * [**bedwars1058\_break\_beds**](actions.md#bedwars1058-bedwars1058_break_beds) - Breaking the beds of other teams.
  * [**bedwars1058\_kill\_players**](actions.md#bedwars1058-bedwars1058_kill_players) - Killing opponents.
  * **bedwars1058\_play\_games** - Playing BedWars games.
  * [**bedwars1058\_buy\_items**](actions.md#bedwars1058-bedwars1058_buy_items) - Buying items from the shop.
  * [**bedwars1058\_buy\_upgrades**](actions.md#bedwars1058-bedwars1058_buy_upgrades) - Buying team upgrades from the shop.
* **Benzimmer's KOTH**
  * [**koth\_capture**](actions.md#benzimmers-koth-koth_capture) - Capture for X seconds (time in seconds is progress).
  * [**koth\_win\_cap**](actions.md#benzimmers-koth-koth_win_cap) - Win the capture of a point.
* [**BuildBattle by Tigerpanzer**](https://www.spigotmc.org/resources/44703/)
  * [**buildbattle\_join**](actions.md#buildbattle-by-tiger-buildbattle_join) - Join a game.
  * [**buildbattle\_play**](actions.md#buildbattle-by-tiger-buildbattle_play) - Triggered for every player when a game starts.
  * [**buildbattle\_finish**](actions.md#buildbattle-by-tiger-buildbattle_play) - Triggered for every player when a game finishes.
* **ChatReaction**
  * [**chatreaction\_win**](actions.md#chatreaction-chatreaction_win) - Winning chat reaction games (repeat/unscramble).
* **Citizens**
  * [**citizens\_click**](actions.md#citizens-citizens_click) - Clicking a citizens NPC.
  * [**citizens\_damage**](actions.md#citizens-citizens_damage) - Damaging a citizens NPC.
  * [**citizens\_kill**](actions.md#citizens-citizens_kill) - Killing a citizens NPC.
* **Clans**
  * [**clans\_create**](actions.md#clans-clans_create) - Creating a clan.
  * [**clans\_join**](actions.md#clans-clans_join) - Joining a clan..
* **ClueScrolls**
  * [**cluescrolls\_complete\_clue**](https://app.gitbook.com/s/-MVKgJtPKw7gQhR_Osin/features/cluescrolls---cluescrolls_complete_clue) - Complete a clue.
  * [**cluescrolls\_complete\_scroll**](https://app.gitbook.com/s/-MVKgJtPKw7gQhR_Osin/features/cluescrolls---cluescrolls_complete_scroll) - Complete a scroll.
* **CrateReloaded**
  * [**cratereloaded\_open**](actions.md#cratereloaded-cratereloaded_open) - Opening a crate.
* **CratesPlus**
  * [**cratesplus\_open**](actions.md#cratesplus-cratesplus_open) - Opening a crate.
* **CrazyCrates**
  * [**crazycrates\_open**](actions.md#crazycrates-crazycrates_open) - Opening a crate.
* **CrazyEnvoy**
  * [**crazyenvoy\_open\_envoy**](actions.md#crazyenvoy-crazyenvoy_open_envoy) - Opening an envoy crate/drop.
  * [**crazyenvoy\_use\_flare**](actions.md#crazyenvoy-crazyenvoy_use_flare) - Using a flare to start an envoy.
* **DiscordMinecraft**
  * [**discordminecraft\_link**](actions.md#discordminecraft-discordminecraft_link-probably-broken) - Link your Discord account to Minecraft.
* **ExcellentCrates**
  * [**excellentcrates\_open**](actions.md#excellentcrates-excellentcrates_open) - Opening a crate.
* **FactionsUUID**
  * [~~**factionsuuid\_kill\_enemy**~~](broken-reference/) - **Disabled due to name issues**
* **Jobs**
  * [**jobs\_join**](actions.md#jobs-jobs_join) - Joining a job.
  * [**jobs\_gain\_exp**](actions.md#jobs-jobs_gain_exp) - Gaining experience from working.
  * [**jobs\_level\_up**](actions.md#jobs-jobs_level_up) - Leveling up.
* **Lands**
  * [**lands\_join**](actions.md#lands-lands_join) - Join a land.
  * [**lands\_leave**](actions.md#lands-lands_leave) - Leave a land.
  * [**lands\_create**](actions.md#lands-lands_create) - Create a land.
  * [**lands\_disband**](actions.md#lands-lands_disband) - Disband a land.
  * [**lands\_invited**](actions.md#lands-lands_invited) - Be invited to a land.
  * [**lands\_claim\_chunk**](actions.md#lands-lands_claim_chunk) - Claim a chunk for your land.
* **LobbyPresents**
  * [**lobbypresents\_find**](actions.md#lobbypresents-by-poompk-lobbypresents_find) - Find a lobby present.
* **MoneyHunters**
  * [**moneyhunters\_level\_up**](actions.md#moneyhunters-moneyhunters_level_up) - Leveling up.
  * [**moneyhunters\_gain\_exp**](actions.md#moneyhunters-moneyhunters_gain_exp) - Gaining experience from working.
* **MythicMobs**
  * [**mythicmobs\_kill\_mob**](actions.md#mythicmobs-mythicmobs_kill_mob) - Killing a MythicMobs mob.
* MMOCore
  * mmocore\_level\_up\_skill - Level up a skill
  * mmocore\_gain\_exp - Gain exp from a skill
* **PlaceholderAPI**
  * [**placeholderapi\_match\_placeholder**](placeholderapi-actions.md) - Value must match the variable
  * [**placeholderapi\_integer\_placeholder**](placeholderapi-actions.md) - Placeholder will be set to progress.
* **PlotSquared**
  * [**plotsquared\_claim**](actions.md#plotsquared-plotsquared_claim) - Claim a PlotSquared plot.
  * [**plotsquared\_visit**](actions.md#plotsquared-plotsquared_visit) - Visit a player's plot.
  * [**plotsquared\_trust\_player**](actions.md#plotsquared-plotsquared_trust_player) - Trust another player.
  * [**plotsquared\_become\_trusted**](actions.md#plotsquared-plotsquared_become_trusted) - Become a trusted player (must be online).
  * [**plotsquared\_rate**](actions.md#plotsquared-plotsquared_rate) - Rate a player's plot.
  * [**plotsquared\_teleport**](actions.md#plotsquared-plotsquared_teleport) - Teleport to a player's plot.
* **ProCosmetics**
  * [**procosmetics\_spend**](https://app.gitbook.com/s/-MVKgJtPKw7gQhR_Osin/features/procosmetics---procosmetics_spend) - Spend X amount on cosmetics.
  * [**procosmetics\_buy\_treasure**](actions.md#procosmetics-procosmetics_buy_treasure) - Buying treasures from ProCosmetics.
  * [**procosmetics\_open\_treasure**](actions.md#procosmetics-procosmetics_open_treasure) - Opening treasures from ProCosmetics.
  * [**procosmetics\_buy\_cosmetic**](actions.md#procosmetics-procosmetics_buy_cosmetic) - Buying cosmetics from ProCosmetics.
* **ShopGui+**
  * [**shopguiplus\_buy**](actions.md#shopguiplus-shopguiplus_buy) - When you purchase an item from the shop. The progress will be the amount purchased.
  * [**shopguiplus\_buy\_singular**](actions.md#shopguiplus-shopguiplus_buy_singular) - When you purchase an item from the shop. The progress will always be 1 per transaction.
  * [**shopguiplus\_spend**](actions.md#shopguiplus-shopguiplus_spend) - When you purchase an item from the shop. The progress will be however much it cost the player.
  * [**shopguiplus\_sell**](actions.md#shopguiplus-shopguiplus_sell) - When you sell an item to the shop. The progress will be the amount sold.
  * [**shopguiplus\_sell\_singular**](actions.md#shopguiplus-shopguiplus_sell_singular) - When you sell an item to the shop. The progress will always be 1 per transaction.
  * [**shopguiplus\_profit**](actions.md#shopguiplus-shopguiplus_profit) - When you sell an item to the shop. The progress will be however much the player gained.
* **EconomyShopGUI**
  * [**economyshopgui\_buy**](actions.md#economyshopgui_buy) - When you purhcase an item from shop
  * [**economyshopgui\_sell**](actions.md#economyshopgui_sell) - When you sell an item in shop
* **Shopkeepers**
  * [**shopkeepers\_trade**](actions.md#shopkeepers-shopkeepers_trade) - Trade an item with a shopkeeper.
  * [**shopkeepers\_open**](actions.md#shopkeepers-shopkeepers_open) - Open a shopkeeper's GUI.
* [**SkillAPI**](https://www.spigotmc.org/resources/skillapi.4824/)
  * [**skillapi\_damage**](broken-reference/) - Damage someone with a skill.
  * [**skillapi\_combo**](broken-reference/) - Get an x hit combo (combo length is progress).
  * [**skillapi\_upgrade**](broken-reference/) - Upgrade a skill.
  * [**skillapi\_unlock**](broken-reference/) - Unlock a skill.
  * [**skillapi\_loose\_mana**](broken-reference/) - When you loose mana for any reason.
  * [**skillapi\_reach\_level**](broken-reference/) - When you reach x level (level is the progress).
  * [**skillapi\_change\_class**](broken-reference/) - When you change your class.
* **Subside KoTH (King of The Hill)**
  * [**koth\_win\_cap**](actions.md#benzimmers-koth-koth_win_cap) - Win a KoTH and be the capping player.
  * [**koth\_capture**](actions.md#benzimmers-koth-koth_capture) - Capture a KoTH for X seconds (increments on time).
* **StrikePractice**
  * [**strikepractice\_host\_events**](broken-reference/) - Hosting an event for others to play.
  * [**strikepractice\_play\_games**](broken-reference/) - Playing matches.
  * [**strikepractice\_play\_bot\_games**](broken-reference/) - Playing matches against the bot.
  * [**strikepractice\_win\_games**](broken-reference/) - Winning matches.
  * [**strikepractice\_win\_bot\_games**](broken-reference/) - Winning matches against the bot.
  * [**strikepractice\_lose\_games**](broken-reference/) - Losing matches.
* **SuperiorSkyblock2**
  * [**superiorskyblock2\_create**](broken-reference/) - Creating an island.
  * [**superiorskyblock2\_join**](broken-reference/) - Joining a player's island.
  * [**superiorskyblock2\_upgrade**](broken-reference/) - Purchasing an island upgrade.
* **TokenEnchant**
  * [**tokenenchant\_gain**](broken-reference/) - Gain tokens.
  * [**tokenenchant\_enchant**](broken-reference/) - Enchant an item.
* **uSkyBlock**
  * [**uskyblock\_invite**](broken-reference/) - Inviting someone to your island.
  * [**uskyblock\_invited**](broken-reference/) - Being invited to an island.
  * [**uskyblock\_join**](broken-reference/) - Joining an island.
  * [**uskyblock\_island\_chat**](broken-reference/) - Talking in the island chat.
* **Votifier**
  * [**votifier\_vote**](broken-reference/) - Just... vote lol
* **RivalHarvesterHoes**
  * [**rivalharvesterhoes\_harvest**](actions.md#rivalharvesterhoes---rivalharvesterhoes_harvest) - When a player breaks crops using hoe from this plugin
* **AdvancedMobs**
  * [**advancedmobs\_kill\_mob**](actions.md#advancedmobs---advancedmobs_kill-mob) - When a player kills a mob from this plugin

#### `block-break`

**Triggered:** When a player breaks a block.

**Variable:** The block's material.

#### `block-place`

**Triggered:** When a player places a block.\
\
**Variable:** The block's material.

#### `bucket-place`

**Triggered**: When player places a bucket

**Variable**: bucket's material (e.g. lava bucket)

#### `brew`

**Triggered**: when potion is brewed

**Variables:**

* `root`: [Potion Type](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/potion/PotionType.html)
* `isExtended`: `true` if potion has extended time (on versions <1.20.2)
* `isUpgraded` : `true` if potion is upgraded (on versions <1.20.2)
* `item`: brewed potion

#### `chat`

**Triggered:** When a player sends a message in chat.\
\
**Variable:** The message sent (lower case)

#### `chat-stripped`

**Triggered:** When a player sends a message in chat - stripped from colour codes.\
\
**Variable:** The message sent (lower case)

#### `right-click`

**Triggered:** Whenever a player right clicks.\
\
**Variable:** none.

#### `left-click`

**Triggered:** Whenever a player left clicks.\
\
**Variable:** none.

#### `right-click-block`

**Triggered:** Whenever a player right clicks a block.\
\
**Variable:** The block's material.

### `left-click-block`

**Triggered:** Whenever a player left clicks a block.\
\
**Variable:** The block's material.

#### `consume`

**Triggered:** Whenever a player consumes (eats) something.\
\
**Variable:** The item's material.

#### `craft`

**Triggered:** Whenever a player crafts an item.\
\
**Variable:** The crafted item's material.

#### `damage-player`

**Triggered:** When a player deals damage to another player.\
\
**Variable:** none.

#### `enchant`

**Triggered:** When a player enchants an item using an enchantment table.\
\
**Variables:**

* `root`: The name of the enchantment (see [here](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/enchantments/Enchantment.html))
* `item`: The material of the enchanted item (e.g `diamond_sword`)
* `level`: The level of the enchantment
* `cost`: The level cost of enchanting

#### `breed`

**Triggered**: When player breeds a mob

Variables:

* root: EntityType
* name: Entity's custom name

#### `harvest-crops`

**Triggered**: When player harvests crops

Variables:

* root: Block type

#### `enchant-anvil`

**Triggered:** When a player enchants an item using an anvil.\
\
**Variables:**

* `root`: The name of the enchantment (see [here](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/enchantments/Enchantment.html))
* `item`: The material of the enchanted item, upper case (e.g `DIAMOND_SWORD`)
* `level`: The level of the enchantmente

#### `enchant-all`

**Triggered:** When a player enchants an item using an enchantment table OR an anvil.\
\
**Variables:**

* `root`: The name of the enchantment (see [here](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/enchantments/Enchantment.html))
* `level`: The level of the enchantment

#### `execute-command`

**Triggered:** When a player issues a server command (cannot be bungee).\
\
**Variable:**: The command executed (must be lower case).

#### `fish`

**Triggered:** When a player catches an item from fishing.\
\
**Variable:** The item caught from fishing.

#### `gain-experience`

**Triggered:** When a player gains exp.\
\
**Variable:** none.

#### `item-break`

**Triggered:** When the item a player is using breaks.\
\
**Variable:** The item's material.

#### `fly`

**Triggered:** When a player flies.\
**Extra Info:** Progression is measured in blocks flown.\
\
**Variable:** none.

#### `glide`

**Triggered:** When a player glides.\
**Extra Info:** Progression is measured in blocks glided.\
\
**Variable:** none.

#### `sneak`

**Triggered:** When a player moves a block sneaking.\
**Extra Info:** Progression is measured in blocks snuck.\
\
**Variables:**

* `isSwimming` - `true` / `false`
* `isGliding` - `true` / `false`
* `isFlying` - `true` / `false`
* `isSneaking` - `true` / `false`
* `isSprinting` - `true` / `false`

#### `sprint`

**Triggered:** When a player sprints a block.\
**Extra Info:** Progression is measured in blocks walked.\
\
**Variable:** none.

#### `swim`

**Triggered:** When a player swims a block.\
**Extra Info:** Progression is measured in blocks walked.\
\
**Variable:** none.

#### `move`

**Triggered:** When a player moves (basically just counting every other movement in one).\
**Extra Info:** Progression is measured in blocks walked.\
\
**Variable:** none.

#### `kill-mob`

**Triggered:** When a player kills a mob.\
\
**Variables:**

root: The type of mob.

* `spawn-reason` - [entity spawn reason](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/event/entity/CreatureSpawnEvent.SpawnReason.html)
* `custom-name` - Custom name of entity

#### `kill-player`

**Triggered:** When a player kills another player.\
\
**Variable:** The name of the killed player.

#### `login`

**Triggered:** When a player logs into the server.\
\
**Variable:** none.

#### `milk`

**Triggered:** When a player milks a cow.\
\
**Variable:** none.

#### `playtime`

**Triggered:** Progressed 1 for every second a user is online (done in 5 second chunks, you must enable this in the settings.yml)\
\
**Variable:** none.

#### `throw-projectile`

**Triggered:** When a player throws/shoots a projectile\
\
**Variable:** The projectile thrown (see [here](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/entity/EntityType.html)).

#### `regenerate`

**Triggered:** When a player regenerates health.\
\
**Variable:** The reason for regaining health (see [here](https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/event/entity/EntityRegainHealthEvent.RegainReason.html)).

#### `ride-mob`

**Triggered:** When a player rides a mob.\
\
**Variable:** The type of entity.

#### `shear`

**Triggered:** When a player shears a sheep.\
\
**Variable:** none.

#### `smelt`

**Triggered:** When a player smelts an item in a furnace.\
\
**Variable:** The material of the item received from smelting (e.g, iron\_ingot).

#### `tame`

**Triggered:** When a player tames a mob.\
\
**Variable:** The type of entity tamed.

#### `honey-extract`

**Triggered:** When a player extracts honey.

**Variable:** Bee Nest or Bee Hive

#### `honey-comb-extract`

**Triggered:** When a player extracts honey combs using shears.

**Variable:** Bee Nest or Bee Hive

### External Actions

#### McMMO - `mcmmo_gain_exp`

**Triggered**: When player gains exp in specific skill

**Variable**: Skill name.

#### McMMO - `mcmmo_level_up_skill`

**Triggered**: When player levels up a skill

**Variable**: Skill name.

#### McMMO - `mcmmo_level_total_skill`

**Triggered**: When player levels up a skill (returns total level of skill)

**Variable**: Skill name.

#### mbedwars\_break\_bed

**Triggered**: When bed is broken

Variable:

root: team name

arena: arena name

#### mbedwars\_kill

**Triggered**: When kill is achieved

root: team name

#### mbedwars\_stat\_change

**Triggered**: Stat changes

root: stat

progress: how much of stat has been gained

#### mbedwars\_buy\_item

**Triggered**: When item is bought

root: item name

arena: arena name

#### mbedwars\_join\_arena

**Triggered**: When an arena is joined

root: team name

cause: https://javadocs.mbedwars.com/de/marcely/bedwars/api/arena/AddPlayerCause.htm

#### mbedwars\_team\_eliminate

**Triggered**: When a teammate is eliminated

root: team name

#### ChestShop - `chestshop_create`

**Triggered:** When a player creates a chest shop.\
\
**Variable:** none.

#### ChestShop - `chestshop_buy`

**Triggered:** When a player makes a purchase from a chest shop.\
\
**Variables:**

* `root`: The owner of the chest shop's name.
* `item`: Bought item

#### ChestShop - `chestshop_sell`

**Triggered:** When a player sells something from their chest shop.\
\
**Variables:**

* `root`: The owner of the client
* `item`: Sold item

#### ChestShop - `chestshop_spend`

**Triggered:** When a player makes a purchase from a chest shop - the cost is the progress.\
\
**Variable:** The owner of the chest shop's name.

#### ChestShop - `chestshop_profit`

**Triggered:** When a player sells something from their chest shop - the cost is the progress.\
\
**Variable:** The name of the client.

#### AdvancedEnchantments - `advancedenchantments_enchant`

**Triggered:** When a player enchants any item.\
\
**Variable:**

* root: Name of enchant (e.g. glowing)
* level: Level of enchant (e.g. 1)

#### ASkyBlock - `askyblock_create_island`

**Triggered:** When you create a skyblock island.\
\
**Variable:** The name of the schematic of the island.

#### ASkyBlock - `askyblock_create_warp`

**Triggered:** When you create an island warp.\
\
**Variable:** none.

#### AuctionHouse by Kludgemonkey - `auctionhouse_list`

**Triggered:** When a player lists an item on the auction house (progressed by the amount of said item).\
\
**Variable:** The material of the item being listed.

#### AuctionHouse by Kludgemonkey - `auctionhouse_list_singular`

**Triggered:** When a player lists an item on the auction house (only progressed by 1)\
\
**Variable:** The material of the item being listed.

#### AuctionHouse by Kludgemonkey - `auctionhouse_buy`

**Triggered:** When a player buys an item on the auction house (progressed by the amount of said item bought).\
\
**Variable:** The material of the purchased item.

#### AuctionHouse by Kludgemonkey - `auctionhouse_buy_singular`

**Triggered:** When a player buys an item on the auction house (only progressed by 1)\
\
**Variable:** The material of the purchased item.

#### AuctionHouse by Kludgemonkey - `auctionhouse_sell`

**Triggered:** When a player successfully sells an item on the auction house (progressed by the amount of said item sold).\
\
**Variable:** The material of the sold item.

#### AuctionHouse by Kludgemonkey - `auctionhouse_sell_singular`

**Triggered:** When a player successfully sells an item on the auction house (only progressed by 1).\
\
**Variable:** The material of the sold item.

#### AuctionHouse by Kludgemonkey - `auctionhouse_profit`

**Triggered:** When a listed item is sold - the amount of money you make from it is the progress.\
\
**Variable:** The material of the sold item.

#### AuctionHouse by Kludgemonkey - `auctionhouse_spend`

**Triggered:** When you purchase an item from the auction house - the amount of money spent is the progress.\
\
**Variable:** The material of the item purchased.

#### AutoSell - `autosell_break`

**Triggered:** When you break a block whilst autosell is enabled.\
\
**Variable:** The material of the block broken.

#### BedWars1058 - `bedwars1058_break_beds`

**Triggered:** When a player breaks a team's bed.\
\
**Variable:** The team of the broken bed.

#### BedWars1058 - `bedwars1058_kill_players`

**Triggered:** When a player kills an enemy player.\
\
**Variable:** The cause of death (`UNKNOWN`, `EXPLOSION`, `VOID`, `PVP`, `PLAYER_SHOOT`)

#### BedWars1058 - `bedwars1058_buy_items`

**Triggered:** When a player purchases an item.\
\
**Variable:** none.

#### BedWars1058 - `bedwars1058_buy_upgrades`

**Triggered:** When a player buys a team upgrade.\
\
**Variable:** none.

#### Benzimmer's KOTH - `koth_capture`

**Triggered:** When a player captures a point for x time (the amount of time captured in seconds is the progress).\
\
**Variable:** The name of the KOTH.

#### Benzimmer's KOTH - `koth_win_cap`

**Triggered:** When a player wins the capture for a KOTH.\
\
**Variable:** The name of the KOTH

#### BuildBattle by Tiger - `buildbattle_join`

**Triggered:** When a player joins a BuildBattle game.\
\
**Variable:** The name of the map.

#### BuildBattle by Tiger - `buildbattle_play`

**Triggered:** When a player is in a game and it starts.\
\
**Variable:** The name of the map.

#### BuildBattle by Tiger - `buildbattle_finish`

**Triggered:** When a player is in a game when it finishes.\
\
**Variable:** The name of the map.

#### ChatReaction - `chatreaction_win`

**Triggered:** When a player wins a ChatReaction competition.\
\
**Variable:** none.

#### Citizens - `citizens_click`

**Triggered:** When a player click a citizens NPC.\
\
**Variable:** The name of the NPC.

#### Citizens - `citizens_damage`

**Triggered:** When a player damages a citizens NPC (normally requires Sentinel).\
\
**Variable:** The name of the NPC.

#### Citizens - `citizens_kill`

**Triggered:** When a player kills a citizens NPC (normally requires Sentinel).\
\
**Variable:** The name of the NPC.

#### Clans - `clans_create`

**Triggered:** When a player creates a clan.\
\
**Variable:** none.

#### Clans - `clans_join`

**Triggered:** When a player joins a clan.\
\
**Variable:** none.

#### ClueScrolls - `cluescrolls_complete_clue`

**Triggered:** When a player completes a clue.\
\
**Variable:** The type of clue.

#### ClueScrolls - `cluescrolls_complete_scroll`

**Triggered:** When a player completes a scroll.\
\
**Variable:** The tier type.

**MMOCore** - `mmocore_level_up_skill`

**Triggered**: When player levels up a skill

**Variable**: skill type name (e.g. ARCHERY)

**MMOCore** - `mmocore_gain_exp`

**Triggered**: when player gains exp from a skill

**Variable**: skill type name (e.g. ARCHERY)

#### CrateReloaded - `cratereloaded_open`

**Triggered:** When a player opens a CrateReloaded crate.\
\
**Variable:** The name of the crate opened.

#### CratesPlus - `cratesplus_open`

**Triggered:** When a player opens a CratesPlus crate.\
\
**Variable:** The name of the crate opened.

#### CrazyCrates - `crazycrates_open`

**Triggered:** When a player opens a CrazyCrates crate.\
\
**Variable:** The name of the crate opened.

#### CrazyEnvoy - `crazyenvoy_open_envoy`

**Triggered:** When a player opens an envoy crate.\
\
**Variable:** The name of the tier of crate.

#### CrazyEnvoy - `crazyenvoy_use_flare`

**Triggered:** When a player uses an envoy flare to start an envoy.\
\
**Variable:** none.

#### DiscordMinecraft - `discordminecraft_link` _(probably broken)_

**Triggered:** When a links their discord account.\
\
**Variable:** none.

#### ExcellentCrates - `excellentcrates_open`

**Triggered:** When a player opens a crate.

**Variable:** crate name.

#### FactionsUUID - `factions_kill_enemy`

**Triggered:** When a player kills another person from an enemy faction.\
\
**Variable:** none.

#### Jobs - `jobs_join`

**Triggered:** When a player joins a job.\
\
**Variable:** The name of the job.

#### Jobs - `jobs_gain_exp`

**Triggered:** When a player gains experience (progress is the exp gained).\
\
**Variable:** The name of the player's job.

#### Jobs - `jobs_level_up`

**Triggered:** When a player levels up (progress is set to this level).\
\
**Variable:** The name of the player's job.

#### Lands - `lands_join`

**Triggered:** When a player joins a land.\
\
**Variable:** none.

#### Lands - `lands_leave`

**Triggered:** When a player leaves a land.\
\
**Variable:** none.

#### Lands - `lands_create`

**Triggered:** When a player creates a land.\
\
**Variable:** none.

#### Lands - `lands_disband`

**Triggered:** When a player disbands their land.\
\
**Variable:** none.

#### Lands - `lands_invited`

**Triggered:** When a player is invited to a land.\
\
**Variable:** none.

#### Lands - `lands_claim_chunk`

**Triggered:** When a player claims a chunk for their land.\
\
**Variable:** none.

#### LobbyPresents by Poompk - `lobbypresents_find`

**Triggered:** When a player finds a present.\
\
**Variable:** The ID of the present.

#### MoneyHunters - `moneyhunters_level_up`

**Triggered:** When a player levels up (the progress is set to their level).\
\
**Variable:** The name of their job.

#### MoneyHunters - `moneyhunters_gain_exp`

**Triggered:** When a player tames a mob (the progress is increased by the given xp).\
\
**Variable:** The name of their job.

#### MythicMobs - `mythicmobs_kill_mob`

**Triggered:** When a player kills a MythicMobs mob.\
\
**Variable:** The name of the type of mob.

#### PlaceholderAPI - `placeholderapi_match_<PLACEHOLDER>`

**Description:** When the placeholder is resolved for the player, it will progress if the variable is the same as what the placeholder resolves to. E.g if the type was as `placeholderapi_match_essentials_flying` and the variable was true, if the player was flying the action would progress.

#### PlaceholderAPI - `placeholderapi_integer_<PLACEHOLDER>`

**Description:** Resolves the placeholder for the player and sets the progress of the action to the value of the placeholder (**the resolved value must be an integer, e.g 342653476**). An example would be the type as `placeholderapi_integer_gemseconomy_balance_default` with the variable none and the required progress 10000. When they get 10000 gems it will be completed.\
\
**Variable:** none.

#### PlotSquared - `plotsquared_claim`

**Triggered:** When a player claims their plot.\
\
**Variable:** auto or manual.

#### PlotSquared - `plotsquared_visit`

**Triggered:** When a player visits another player's plot.\
\
**Variable:** The owner of the plot's username or `none` if not found.

#### PlotSquared - `plotsquared_trust_player`

**Triggered:** When a player trusts another player.\
\
**Variable:** none.

#### PlotSquared - `plotsquared_become_trusted`

**Triggered:** When a player becomes trusted on another player's plot.\
\
**Variable:** none.

#### PlotSquared - `plotsquared_rate`

**Triggered:** When a player rates another player's plot.\
\
**Variable:** none.

#### PlotSquared - `plotsquared_teleport`

**Triggered:** When a player teleports to a plot.\
\
**Variable:** The owner of the plot's username or `none` if not found.

#### ProCosmetics - `procosmetics_spend`

**Triggered:** When a player spends coins on a cosmetic or treasure chest (the progress is the amount spent).\
\
**Variable:** `treasure-chest` or `cosmetic` depending on what was bought.

#### ProCosmetics - `procosmetics_buy_treasure`

**Triggered:** When a player buys a treasure.\
\
**Variable:** The name of the treasure.

#### ProCosmetics - `procosmetics_open_treasure`

**Triggered:** When a player opens a treasure.\
\
**Variable:** The name of the treasure.

#### ProCosmetics - `procosmetics_buy_cosmetic`

**Triggered:** When a player buys a cosmetic.\
\
**Variable:** The type of cosmetic.

#### ShopGuiPlus - `shopguiplus_buy`

**Triggered:** When a player purchases an item from the shop. The progress will be the amount of items purchased\
\
**Variables:**

* `root`: The item that was purchased (e.g iron\_sword:0)
* `shop`: The ID of the shop the item was purchased from (e.g foodstuffs)
* `item-id`: The ID of the item in the shop (e.g 2, 6, or 8)

#### ShopGuiPlus - `shopguiplus_buy_singular`

**Triggered:** When a player purchases an item from the shop. The progress will always be 1\
\
**Variables:**

* `root`: The item that was purchased (e.g iron\_sword:0)
* `shop`: The ID of the shop the item was purchased from (e.g foodstuffs)
* `item-id`: The ID of the item in the shop (e.g 2, 6, or 8)

#### ShopGuiPlus - `shopguiplus_spend`

**Triggered:** When a player purchases an item from the shop. The progress will be the amount it cost the user rounded up to the nearest real number (2.4 -> 3)\
\
**Variables:**

* `root`: The item that was purchased (e.g iron\_sword:0)
* `shop`: The ID of the shop the item was purchased from (e.g foodstuffs)
* `item-id`: The ID of the item in the shop (e.g 2, 6, or 8)

#### ShopGuiPlus - `shopguiplus_sell`

**Triggered:** When a player sells an item to the shop. The progress will be the amount of items sold.\
\
**Variables:**

* `root`: The item that was purchased (e.g iron\_sword:0)
* `shop`: The ID of the shop the item was purchased from (e.g foodstuffs)
* `item-id`: The ID of the item in the shop (e.g 2, 6, or 8)

#### ShopGuiPlus - `shopguiplus_sell_singular`

**Triggered:** When a player sells an item to the shop. The progress will always be 1.\
\
**Variables:**

* `root`: The item that was purchased (e.g iron\_sword:0)
* `shop`: The ID of the shop the item was purchased from (e.g foodstuffs)
* `item-id`: The ID of the item in the shop (e.g 2, 6, or 8)

#### ShopGuiPlus - `shopguiplus_profit`

**Triggered:** When a player sells an item to the shop. The progress will be the amount it cost the user rounded up to the nearest real number (2.4 -> 3)\
\
**Variables:**

* `root`: The item that was purchased (e.g iron\_sword:0)
* `shop`: The ID of the shop the item was purchased from (e.g foodstuffs)
* `item-id`: The ID of the item in the shop (e.g 2, 6, or 8)

#### EconomyShopGUI - `economyshopgui_buy`

**Triggered:** When a player purchases an item from the shop.\
**Variable:** The item that was purchased

#### EconomyShopGUI - `economyshopgui_sell`

**Triggered:** When a player sells an item in the shop.\
**Variable:** The item that was sold

#### Shopkeepers - `shopkeepers_trade`

**Triggered:** When a player trades with a shopkeeper.\
\
**Variable:** The UUID of the shopkeeper.

#### Shopkeepers - `shopkeepers_open`

**Triggered:** When a player opens a shopkeeper.\
\
**Variable:** The UUID of the shopkeeper.

#### SuperiorSkyBlock2 - `superiorskyblock2_upgrade`

**Triggered:** Purchasing an island upgrade.\
**Variable:** The name of an upgrade (`plugins\SuperiorSkyblock2\modules\upgrades`)

### RivalHarvesterHoes - `rivalharvesterhoes_harvest`

**Triggered:** When a player breaks crops using hoe from this plugin

**Variables:**

root: crop block

* `item` - Hoe item

#### AdvancedMobs - `advancedmobs_kill-mob`

**Triggered:** When a player kills mob from this plugin

**Variable:** The mob type
