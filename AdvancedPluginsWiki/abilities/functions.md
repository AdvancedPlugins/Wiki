# Functions

Functions are tags which can be used in effect lines to make them more dynamic. They are written in `<>` brackets and are used instead of a value for the effect.

Here is a list of available functions:

### `<chance>`

Sets a chance for this effect line to activate. The number inside the brackets is the percentage chance of the effect activating.

Example:

```yaml
effects:
- 'INCREASE_DAMAGE:5 <chance>50</chance>'
```

This will cause the entity to take 5% more damage 50% of the time.

### `<condition>`

Use in-line conditions for effects. Extremely handly to create dynamic mechanics.

Example:

```yaml
effects:
- 'ADD_HEALTH:5 <condition>%victim health% < 10 : %allow%</condition>'
```

This would add 2.5 hearts to victim's health if they had less than 5 hearts remaining.

### `<math>`

Performs a math operation using variables or numbers. The operation is written inside the brackets.

Example:

```yaml
effects:
- 'EXP:<math>%exp% * 2</math>'
```

This will drop double the amount of experience from event.

### `<random number>`

Picks a random number between two values. The values are written inside the brackets and separated by a dash `-`.

Example:

```yaml
effects:
- 'INCREASE_DAMAGE:<random number>1-5</random number>'
```

This will increase the damage to a random amount between 1 and 5.

### `<random word>`

Picks a random word from a list. The words are written inside the brackets and separated by a comma `,`.

Example:

```yaml
effects:
- 'MESSAGE:<random word>Hello,Goodbye,Hi</random word>'
```

This will send a message with a random word from the list.

### `<round>`

Rounds a number to the nearest whole number. The number is written inside the brackets.

Example:

```yaml
effects:
- 'EXP:<round><math>%exp% * 2.5</math></round>'
```

This will give the entity an amount of experience that is 2.5 times their current amount, rounded to the nearest whole number.

### **`<int>`**

Converts a floating-point number to an integer by removing any fractional parts. The number to be converted is written inside the brackets.

**Example:**

`effects:`

* `'EXP:<int><math>%exp% * 1.5</math></int>'`

In this example, if the entity has an experience value (`%exp%`), multiplying it by 1.5 might result in a floating-point number. The `<int></int>` tags ensure that the final experience value given to the entity is an integer by removing any decimals.

### **`<scramble>`**&#x20;

Randomly rearranges the characters within the text placed inside the brackets. This can be used to create scrambled text effects.

**Example:**

`effects:`

* `'Message:<scramble>Welcome!</scramble>'`

In this example, the text "Welcome" will be scrambled into a random arrangement, such as "cme!lWe!" (Note: The actual scrambled output will vary each time it's generated.)
