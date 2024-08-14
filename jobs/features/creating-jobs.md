# 🎓 Creating Jobs

AdvancedJobs allows for the creation and customization of jobs in two primary ways: through direct configuration files or via an intuitive, state-of-the-art in-game GUI editor. This flexibility ensures that server administrators can tailor jobs to the unique needs and playstyles of their server community, whether they prefer working with files or graphical interfaces.

## Configuration Files

Jobs can be manually created and customized by editing YAML configuration files located in the `/plugins/advancedjobs/jobs` folder. This method is ideal for those who prefer direct control over job parameters and enjoy working with text-based configurations.

#### Steps:

1. Navigate to `/plugins/advancedjobs/jobs`.
2. Create or edit a `.yml` file for your job (e.g., `miner.yml`, `farmer.yml`).
3. Define job attributes according to the plugin's job configuration schema, including actions, rewards, levels, and more.
4. Save your changes and reload the plugin to apply them.

## Special Cases Progress

You can specify different cases progress, e.g. with kill-mob action, to assign different progress points: [https://wiki.advancedplugins.net/actions/special-progress-custom-types-progress](https://wiki.advancedplugins.net/actions/special-progress-custom-types-progress)

## Job Permissions

You can add permissions to jobs using the guide here: [#per-job-permission](../general/commands-and-permissions.md#per-job-permission "mention")

## In-Game GUI Editor

For those who prefer a more visual approach, AdvancedJobs offers an EASY TO USE, in-game GUI editor. This tool eliminates the need to directly edit configuration files, providing a user-friendly interface for creating and modifying jobs.

#### Accessing the Editor:

* Use the command `/ajadmin editor` to open the in-game job editor.

#### Features:

* **Intuitive Design**: The GUI is designed to be user-friendly, making job creation accessible to everyone.
* **Real-Time Editing**: Make changes and see them reflected immediately in-game, allowing for dynamic adjustments.
