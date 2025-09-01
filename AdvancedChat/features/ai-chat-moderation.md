---
description: Learn more about AI powered moderation designed to ease your day!
---

# 🤖 AI Chat Moderation

<div data-full-width="true"><figure><img src="https://advancedplugins.net/img/ac/ai-filter.gif" alt=""><figcaption></figcaption></figure></div>

## Explanation

Elevate your server with AI-Powered Chat Moderation, a game-changing feature that utilizes OpenAI's GPT to maintain a safe and inclusive community. It goes beyond traditional moderation by understanding the context of chat messages, efficiently identifying and removing content that is sexual, hateful, harmful, or promotes self-harm. This moderation is passive and operates seamlessly to ensure a secure environment for all players. **It's currently limited to English language** content but offers comprehensive coverage across several types of violations.

We believe the server chat should be a safe space for everyone, and by implementing these changes

This is a passive chat filter, and sends chat messages to a server where it is processed. No data is or will ever be stored.&#x20;

This AI chat moderation tool is a forward-thinking solution designed to create a safer online environment, enabling server customization to match community standards while offering ease of management.

## Violations

Current violations, checked and categorized by AI:

* swearing
* sexual
* hate
* harassment
* self-harm
* violence

## Configuration: `ai.yml`

### Enabling AI Chat Filter

```yaml
# AI Powered chat handling
# Powered by OpenA

enabled: true
```

Setting `enabled: true` activates the AI chat filter. This feature can be completely toggled off if desired.

### Handling Multiple Violations

```yaml
multiple-violations: false
```

Determines if a player should be punished for each violation within a single message or just once. `false` implies a single action will be taken regardless of the number of violations.

### Filters and Actions

The `filters` section defines various types of content to monitor and the corresponding actions to take when violations are detected. Each category (e.g., swearing, sexual content, hate speech) can be individually enabled and linked with specific actions such as warning the player.

{% code fullWidth="true" %}
```yaml
filters:
  swearing:
    enabled: true
    # This sets the confidence threshold for the AI to flag violation in messages, with a range from 0.0 to 1.0.
    # A higher threshold means the AI needs to be more confident that the message contains swearing before taking action.
    # We recommend keeping this value at 0.9 or higher.
    threshold: 0.9
    action:
      - "warn %player% Swearing is not allowed!"
  # Additional filters follow the same structure

```
{% endcode %}

Actions are customizable. `%player%` will be replaced with the violator's name, and `%message%` (not shown but applicable) with the offending message.

### Logging

```yaml
logging:
  enabled: true
```

When enabled, all filtered messages, along with details of the violation, are logged to the console. This aids in monitoring and adjusting the filter's effectiveness.

\
