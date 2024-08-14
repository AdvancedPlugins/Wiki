# Commands & Permissions

### Number of Jobs Permission

{% hint style="success" %}
**To specify how many jobs a player is able to have, use permission** `advancedjobs.slots.<number>`
{% endhint %}

### Premium Pass

**Premium jobs pass permission**: `advancedjobs.premium`

### Per-Job Permission

You can enable per-job permissions by adding `permission: 'permission'` setting to each of the job files, e.g. like this:

<div align="left">

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

</div>

### Player Commands

#### /advancedjobs (aliases: /aj, /jobs)

* **Permission**: `jobs.use`
* **Description**: Opens the jobs interface, allowing players to browse and select jobs.

### Administrative Commands

Administrative commands offer a range of functionalities from reloading configurations to managing user job data. These commands require the `jobs.admin` permission.

#### /advancedjobsadmin (aliases: /ajadmin)

* **Permission**: `jobs.admin`
* **Description**: Access base command for admin functionalities.

#### /ajadmin reload

* **Description**: Reloads all configurations and job files.

#### /ajadmin delete user

* **Description**: Deletes a user's job data.

#### /ajadmin give points

* **Description**: Awards job points to a user.

#### /ajadmin levelup

* **Description**: Manually level up a user in a specific job.

#### /ajadmin editor

* **Description**: Opens the in-game quest editor.

#### /ajadmin refresh jobs

* **Description**: Refreshes daily jobs for all players.

#### /ajadmin reset jobs

* **Description**: Resets all job progress for all players.

#### /ajadmin set points

* **Description**: Sets a user's job points to a specific amount.

#### /ajadmin sync jobs

* **Description**: Synchronizes job data across bungee or MySQL servers.

These commands are designed to give server administrators full control over the AdvancedJobs plugin, enabling them to customize the job system to fit their server's needs.
