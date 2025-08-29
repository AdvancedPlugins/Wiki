# PlaceholderAPI Placeholders

## AdvancedJobs PlaceholderAPI Placeholders

AdvancedJobs integrates seamlessly with PlaceholderAPI, offering a wide array of placeholders that provide dynamic information about jobs. These placeholders can be used in various parts of your server, such as in chat, on scoreboards, or within GUIs, to display job-specific data for each player. Below is a table outlining the available placeholders and their functions:

<table data-full-width="true">
    <thead>
        <tr>
            <th>Placeholder</th>
            <th>Explanation</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>%advancedjobs_limit%</code></td>
            <td>The maximum number of jobs a player can have.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_in_jobs%</code></td>
            <td>The current number of active jobs a player is part of.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_active%</code></td>
            <td>List of all player's jobs</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_current_points%</code></td>
            <td>The current points a player has accumulated.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_&#x3C;job>%</code><br><code>%advancedjobs_&#x3C;job>_level%</code></td>
            <td>The player's level in the specified job.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_&#x3C;job>_name%</code></td>
            <td>The name of the specified job.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_&#x3C;job>_active%</code></td>
            <td>Whether the player currently has the specified job active (<code>true</code> or <code>false</code>).</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_&#x3C;job>_percentage_progress%</code></td>
            <td>The player's progress percentage towards the next level in the specified job.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_&#x3C;job>_required_points%</code></td>
            <td>The total points required to reach the next level in the specified job.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_&#x3C;job>_required_points_left%</code></td>
            <td>The points a player needs to accumulate to reach the next level in the specified job.</td>
        </tr>
        <tr>
            <td><code>%advancedjobs_daily_refresh_time%</code></td>
            <td>Shows time left to daily refresh</td>
        </tr>
    </tbody>
</table>

-   `<job>` - An ID of job **OR** the slot number (from 0) of player's active job. I.e. `%advancedjobs_0_name%` is a name of player's first active job

## Leaderboards

```
%advancedjobs_top_points_name_PLACE%
%advancedjobs_top_points_value_PLACE%
%advancedjobs_top_points_place_me%
%advancedjobs_top_points_value_me%

%advancedjobs_top_level_name_PLACE_JOB%
%advancedjobs_top_level_value_PLACE_JOB%
%advancedjobs_top_level_place_me_JOB%
%advancedjobs_top_level_value_me_JOB%
```
