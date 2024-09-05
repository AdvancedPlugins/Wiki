---
description: Learn how to script with Abilities
---

# Scripting

With new abilities v2, we've added scripting support for effects. Variables are are reset with server restarts.

## `SET_VARIABLE:<NAME><VALUE>`

Create a custom variable globally, not per user. To create a variable that could be user for a user, you can include user's name in the variable's name, e.g. `customVar%attacker name%`

## `INVERT_VARIABLE:<NAME>`

Invert a custom variable's boolean. If no variable was set before, it will default to `false`

## Use variable in effects and conditions

Due to nature of these variables and naming, you can create global or per-player variables. To use them in effects and conditions, add a `%custom_` prefix and then name your variable.&#x20;

### Global variables

E.g. if we create a variable:

```yaml
SET_VARIABLE:myVariable:awesome
```

We can use this variable in effects later like this:

```
MESSAGE:You are %custom_myVariable%
```

This would send a message to the player `You are awesome`.

### Per-player variables

Creating per-player variables is still as simple and easy! Just include the player name variable inside the variable's name, e.g.:

```
SET_VARIABLE:customValue%attacker name%:50
```

Then later we can retrieve it in a message like this as well:

```
MESSAGE:I have %custom_customValue%attacker name%% dollars
```

This would message `I have 50 dollars`

### Conditions

It works the same, but an example would be:

```
conditions:
  - '%custom_customValue%attacker name%% = 50 %allow%'
```

### Null / Unitialized variables

If an attempt is made to retrieve a variable which doesn't exist, default value will be `0`

## Examples

In this example, we use RIGHT\_CLICK trigger to count how many times user right clicks. If they click more than 5 times, they will not be able to activate the message again.

{% code lineNumbers="true" %}
```yaml
RIGHT_CLICK:
  conditions:
    - '%custom_nameof%attacker name%% = 5 : %stop%'
  effects:
    - 'SET_VARIABLE:clicks%attacker name%:<math>%custom_clicks%attacker name%%+1</math>'
    - 'MESSAGE:You clicked %custom_clicks%attacker name%% times'
```
{% endcode %}
