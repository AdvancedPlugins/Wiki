# Job Join and Leave Conditions

## Job Leave Conditions, Variables and Commands

* By default disabled for job - meaning there's no conditions for joining and leaving
* Requires PlaceholderAPI

When player leaves a job, they need to meet specific conditions. After that plugin executes console commands with variables similar to variables in command rewards.

{% hint style="info" %}
This configuration must be added inside each job file you want to set up the conditions for.
{% endhint %}

### Example Configuration

```
# Requires PlaceholdersAPI
job-leave:
  # Conditions required to leave job.
  # Use placeholders from PlaceholdersAPI and >,<,==
  conditions:
    or: # At least one of these conditions must be meet
      - "%player_level% > 0"
      - "%player_has_permission_jobs.leave.bypass% == yes"
    and: [ ] # All of these conditions must be meet
  # Similar to variables in rewards
  variables:
    cost: "<if>%player_has_permission_jobs.leave.bypass% == yes ? 0 : -1</if>"
  # Commands to execute after leaving job
  commands:
    - "experience add %player% %cost% levels"
```

Using this configuration, player needs to have at least 1st experience level **OR** have permission `jobs.leave.bypass`. When player meet these conditions, they can leave job, but if they don't have that permission, they lose 1 level.

### Types of conditions

#### Or conditions

Player needs to meet at least one condition (same as `||` operator in Java)

#### And conditions

Player needs to meet all conditions (same as `&&` operator in Java)

## Job Join Conditions

The format is the same, but instead of `job-leave` it will use the `job-join` key.\
