# PlaceholderAPI Placeholders

## `%battlepass_points%`

Gives the amount of points a player currently has.

## `%battlepass_points_formatted%`

Gives the formatted amount of points a player currently has.

## `%battlepass_balance%` or `%battlepass_currency%`

Gives the formatted amount of currency a player currently has.

## `%battlepass_balance_base%` or `%battlepass_currency_base%`

Gives the amount of currency a player currently has.

## `%battlepass_tier%`

Gives the current tier of the player.

## `%battlepass_pass_type%`

Gives the name of the pass the player currently has.

## `%battlepass_pass_id%` - Since 3.0.1

Gives the ID of the pass the player currently has (internal name).

## `%battlepass_completed_quests%` - Since 3.10

Displays the amount of quests a user has currently completed.

## `%battlepass_completed_quests_CATEGORY%` - Since 3.10

Displays the amount of quests a user has currently completed in a specific category. If in a menu where the %week% placeholder is available, it is sometimes possible to do `%battlepass_completed_quests_week-%week%%` to display quests done in that week.

## `%battlepass_quest_amount%` - Since 3.10

Gives the total amount of quests in the battlepass.

## `%battlepass_week%` - Since 3.10

Gives the current week of the battlepass

## `%battlepass_time_to_daily_reset%` - Since 3.10

Gives a formatted time until daily quests reset.

## `%battlepass_time_to_next_week%` - Since 3.10

Gives a formatted time until the next week unlocks.

## `%battlepass_time_to_season_end%` - Since 3.10

Gives a formatted time until the season ends.

## `%battlepass_next_tier_points_total_free%`

Gives the amount of points the user currently have for the next tier.

## `%battlepass_next_tier_points_required_free%`

Gives the amount of points the user needs in order to tier up.

## `%battlepass_next_tier_points_total_premium%`

Gives the amount of points the user currently have for the next tier. (premium pass)

## `%battlepass_next_tier_points_required_premium%`

Gives the amount of points the user needs in order to tier up. (premium pass)

## %battlepass\_has\_booster\_\<SERVER/PLAYER/ANY>_\<PROGRESS/POINTS/REWARDS/ANY>_\<PERCENT\*/ANY>\_\<AFFECTS\*/ANY>%

Check whether a booster is active

* PERCENT - Booster percent
* AFFECTS - Affects condition same as in booster command

Examples:

1. %battlepass\_has\_booster\_player\_any\_any\_week-1-2% - Returns `true` if player has any booster which affects exactly 2nd quest in 1st week.
2. %battlepass\_has\_booster\_player\_POINTS\_10\_all% - Returns `true` if player has points booster which adds 10% to all quests
3. %battlepass\_has\_booster\_SERVER\_ANY\_100\_ANY% - Returns `true` if server has any booster which adds 100%
