---
description: Coming soon.
---

# Skills

Set up pre-made skills to be used in effects, instead of having to declare each time. They will have dynamic variables and could be used like this: &#x20;

{% code lineNumbers="true" %}
```yaml
effects:
  - 'SKILL:extremeDamage[damage=2]'
```
{% endcode %}

And in skills.yml file, you would be define a skill like this:

<pre class="language-yaml" data-overflow="wrap" data-line-numbers><code class="lang-yaml"><strong>skills:
</strong>  extremeDamage:
    effects:
    - 'DO_HARM:[damage] @Victim'
    - 'LIGHTNING @Victim'
    - 'MESSAGE:&#x26;cYou were hit with &#x26;lextreme damage&#x26;c! @Victim'
</code></pre>
