# Using AdvancedChallenges with proxy (bungee / velocity etc.)

AdvancedChallenges supports networks of servers which use common proxies like BungeeCord, Velocity and their forks. The only requirement for proxy to be supported is to support `BungeeCord` messages channel (it has to be enabled in proxy settings).

## Plugin configuration

To make everything work, you have to make some adjustments in `plugins/AdvancedChallenges/config.yml` file:

-   Make sure to use MySQL or PostgreSQL as `storage-method` and configure same database
-   Enable multiple-servers-support
-   Set **only one** server as `main-server` in that section. Other servers set to `false`. This server will be used to generate new challenges
-   Set server's saving offset (`challenges-offset-ticks`). Each server should have different offset. It's recommended to keep at least 15-30s offset between servers
-   If you want, you can set different tags for your servers (`server-tag`). It's used mainly in whitelisted / blacklisted servers list in challenges / rewards configuration
-   If you want, you can adjust `boosters-refresh-ticks` - boosters will be refreshed between servers every that time (in ticks)

## Current downsides of proxy support

-   Challenge progress is refreshed every few minutes unless there is an important change (like step up, level up, reset etc). It causes desynchronization between servers and make progressing challenge longer.
-   Boosters are refreshed every some time, so adding global booster will take some time to be added on all the servers
-   Player's contribution may not be calculated fully accurate
-   **You shouldn't start / stop all the server in the same time. It's really recommended to make some 10s offset**
