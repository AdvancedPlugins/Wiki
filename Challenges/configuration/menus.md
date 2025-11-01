# Creating & Configuring menus

AdvancedChallenges offers fully customizable menus. There are 2 types of them:

-   Preconfigured required menus: Leaderboard Menu, Rewards Menu, Streak Menu
-   Custom made menus: (by default, but you can create more) portal menu, streaks overview menu, common challenges menu, temporary challenges menu

## Preconfigured required menus

These menus are required to make plugin work and they can be configured in `plugins/AdvancedChallenges/menus` folder. You can't delete them or add new ones.

## Custom menus

These menus can be fully customized. You can create new ones, remove existing ones etc. They are in `plugins/AdvancedChallenges/menus/custom` folder.

To make them fully functional, you can use challenge specific options, but you don't have to and you can use it as "static" menu to i.e. show some information or navigate players to other menus.

```yaml
menu-title: "Common Challenges" # Menu display name
menu-rows: 4 # Number of rows (1-6)

# Configuration of challenges shown in that menu
# If you don't want to show them in that menu, set challenges-groups to []
show-challenges-from-different-servers: true # Show challenges which can't be comleted on that server
challenges-groups: ["common"] # List of groups which can be shown in that menu (group option in challenge configuration)
challenges-slots:
    slots: "10...16,19...25" # Slotes in which challenges will be shown

# List of static items
menu:
    "27":
        item:
            type: arrow
            name: "&ePrevious Page &7(Click)"
            lore:
                - ""
                - "&7&o(( Click to go to the previous page ))"
        actions:
            - "[menu](page = 1) {portal}"
            - "[menu](page ! 1) {previous-page}"
    "35":
        item:
            type: arrow
            name: "&eNext Page &7(Click)"
            lore:
                - ""
                - "&7&o(( Click to go to the next page ))"
        actions:
            - "[menu] {next-page}"
```

**You can change defualt menu in `plugins/AdvancedChallenges/config.yml` file. Section: `default-menu`**
