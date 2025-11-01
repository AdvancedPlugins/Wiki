# Creating & Configuring challenges

Challenges can be created / configured in [category config](./categories.md)

## Configuration

```yaml
name: "My New challenge" # Challenge display name
start-date: "31/07/2025 12:00" # Date from which challenge will be available
end-date: "31/07/2030 12:00" # Date to which challenge will be available
repeat: true # If enabled, after completing challenge it will level up until max-level
max-level: 3 # Max level for repeated challenges
group: "daily" # Menu group (may be used in different categories to combine multiple categories into one menu)
required-permission: "" # Required permission to do a challenge
manual: false # If enabled, player has to join the challenge in the menu before making a progress
join-fee: 0 # If manual is enabled, player has to pay that amount of money before making a progress (Vault is required)
required-points: 1000 # Required points to progress the challenge
whitelisted-servers: [] # Whitelisted servers (config.yml -> multiple-servers-support.server-tag)
blacklisted-servers: [] # Blacklisted ^
whitelisted-worlds: [] # Whitelisted worlds
blacklisted-worlds: [] # Blacklisted ^
whitelisted-regions: [] # Whitelisted WorldGuard regions
blacklisted-regions: [] # Blacklisted ^
# List of steps required to complete a challenge
steps:
    1:
        type: block-break # Action type (https://wiki.advancedplugins.net/actions/actions)
        variable: oak_log # Variable (https://wiki.advancedplugins.net/actions/setting-up-and-using-variables)
        required-progress: "20 * %level%" # Required progress to complete the step. %level% placeholder returns current challenge level
        info: # Info for %info% placeholder in icon's lore
            - "Chop %required_progress% oak logs"
        rewards: ["1"] # List of rewards
        points: "%level% *  200" # Base number of given points after completing the step. The final given points is modified by player's contribution to that step
# Challenge icon
icon:
    type: IRON_AXE
    name: "&6Daily Challenge - Chop wood (%level%/%max_level%) s. %step%/%steps%"
    lore:
        - "&7Goal: %info%"
        - "&7Ends in %end%"
        - "&7%percentage_progress%% (%progress%/%required_progress%)"
        - "Progress: %progress_bar%"
        - "&7Your contribution: %contribution_percentage%% (%contribution%/%max_contribution%)"
        - "&7Contribution: %contribution_bar%"
        - "&7Rewards: %rewards%"
        - "%permission_info%"
        - "%server_info%"
        - "%points_info%"
        - "%booster_info%"
        - "%manual_info%"
```

## Icon's placeholders

`%level%` - Current level
`%max_level%` - Max level
`%step%` - Current step
`%steps%` - Number of steps
`%info%` - Step information
`%end%` - Time to challenge end
`%progress%` - Current progress points
`%required_progress%` - Required progress points
`%percentage_progress%` - Progress %
`%progress_bar%` - Progress bar
`%contribution%` - Current player's contribution points
`%max_contribution%` - Max player's contribution points
`%contribution_percentage%` - Player's contribution %
`%contribution_bar%` - Player's contribution progress bar
`%rewards%` - List of rewards for completing the step
`%permission_info%` - Automatic information about required permission
`%server_info%` - Automatic information about whitelisted/blacklisted servers
`%points_info%` - Automatic information about required points
`%booster_info%` - Automatic information about current boosters
`%manual_info%` - Automatic information about join / fee requirement
