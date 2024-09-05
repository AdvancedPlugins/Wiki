# Pointers

**Pointers** are a new mechanic introduced in AdvancedEnchantments to specify the event or situation under which an effect is activated or applied. They are concise, easy to read, and help in providing context to the enchantment effects.

{% hint style="info" %}
Pointers will still obey triggers set by your ability. Meaning you cannot add additional triggers to your abilities with just pointers.
{% endhint %}

### Overview

A pointer is a short string prefixed by `~`. It indicates when an effect should be activated. For instance, `~ATTACK` signifies the effect is activated during an attack. Negative pointers, prefixed by `~!`, indicate when an effect should NOT be activated. For example, `~!ATTACK` implies the effect is not to be activated during an attack.

### Usage

To use a pointer, append it to the effect line in the enchantment definition. Here are some examples:

```graphql
DECREASE_DAMAGE:40 @Attacker ~DEFENSE
```

Multiple pointers can be combined for more complex conditions:

```graphql
EFFECT_NAME ~ATTACK ~!DEFENSE
```

This would mean the effect is activated during an attack but not during defense.

### Conclusion

Pointers provide a powerful and flexible way to specify the context under which enchantment effects are activated. They streamline enchantment definitions and make them more readable and intuitive for users. By adopting pointers, enchantment designers have a more granular control over when and how their effects are triggered.
