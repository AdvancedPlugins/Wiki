# Multiple Conditions

You can make multiple condition lines, and have different comparisons and outcomes for each one.\
Example:

```yaml
conditions:
  - '%attacker health% <= 5 : %allow%'
  - '%victim health% >= 15 : %allow%'
effects:
  - 'INCREASE_DAMAGE:100'
```

You can make conditions even more advanced by having multiple different types of conditions on one line.\
Use `&&` to make combine two conditions on one line and require both of them to be fit the comparison for your outcome to happen.\
Additionally, you can use `OR` to make at least one of these conditions fit for it to parse.\
Examples:

<pre class="language-yaml"><code class="lang-yaml"><strong>conditions:
</strong>  - '%attacker health% &#x3C;= 5 &#x26;&#x26; %victim health% >= 15 : %allow%'
effects:
  - 'INCREASE_DAMAGE:100'
</code></pre>

```yaml
conditions:
  - '%mob type% = RAVAGER OR %mob type% = POLAR_BEAR : %allow%'
effects:
  - 'INCREASE_DAMAGE:<random number>5-15</random number> %attacker%'
```

You can have up to as many of these in a line as you want, for example:

```yaml
conditions:
  - '%mob type% = SKELETON : %allow% OR %mob type% = ZOMBIE : %allow% OR %mob type% = ZOMBIE_VILLAGER : %allow% OR %mob type% = WITHER : %allow% OR %mob type% = WITHER_SKELETON : %allow% OR %mob type% = ZOMBIFIED_PIGLIN : %allow% OR %mob type% = SKELETON_HORSE : %allow% OR %mob type% = ZOMBIE_HORSE : %allow% OR %mob type% = STRAY : %allow% OR %mob type% = HUSK : %allow% OR %mob type% = PHANTOM : %allow% OR %mob type% = DROWNED : %allow% OR %mob type% = ZOGLIN : %allow%
effects:
  - 'ADD_HARM:<math>%level%*1.5</math> %victim%'
```
