# Targets

Targets are the entities or blocks that will be affected by an ability. Examples of targets include the player using the ability, the victim of an attack, or a block that has been broken.

Here are some examples of targets:

* `@Victim`: Applies the effect to the victim of an event (such as an attack).
* `@Attacker`: Applies the effect to the attacker of an event (such as an attack).
* `@Block`: Applies the effect to the block that was interacted with (such as right-clicking).
* `@NearestPlayer{radius=0}`: Applies the effect to the nearest player within the specified radius.

You can use multiple targets in a single effect, separated by a space. For example: \
`@Victim @Attacker` would apply the effect to both the victim and the attacker of an event.

### Target Configuration

Targets can be configured with additional options. For example, you can use the `radius` option to specify the radius around a target to search for another target.

Here's an example of a target configuration using the `radius` option:

```yaml
effects:
- 'MESSAGE:you are the nearest player! @NearestPlayer{radius=10}'
```

This would apply the effect to the nearest player within a radius of 10 blocks.

### Target Reference Table

Here is a table of all available targets, along with their descriptions:

| Name                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                     |
| --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `@Victim`                                                                         | Applies the effect to the victim of an event (such as an attack).                                                                                                                                                                                                                                                                                                                                                               |
| `@Attacker`                                                                       | Applies the effect to the attacker of an event (such as an attack).                                                                                                                                                                                                                                                                                                                                                             |
| `@Self`                                                                           | Applies the effect to main entity (who activated it)                                                                                                                                                                                                                                                                                                                                                                            |
| `@Block`                                                                          | Applies the effect to the block that was interacted with (such as right-clicking).                                                                                                                                                                                                                                                                                                                                              |
| `@NearestPlayer{radius=0}`                                                        | Applies the effect to the nearest player within the specified radius.                                                                                                                                                                                                                                                                                                                                                           |
| `@EyeHeight`                                                                      | Applies the effect at entity's eye location                                                                                                                                                                                                                                                                                                                                                                                     |
| <p><code>@Trench{radius=0}</code><br><code>@Trench{radiuscustom=0x0x0}</code></p> | <p>Applies effect in square (e.g. 3x3x3) size area (commonly used for Trench). Only odd numbers allowed (e.g. 3, 5, 7, 9 etc..)<br><br>Use <code>{ignoretool=true}</code> to allow trench with tools which are not allowed to break blocks with. E.g. shovel on cobblestone</p>                                                                                                                                                 |
| `@BlockInDistance{distance=1}`                                                    | Gets block within distance (closest one or the furthest away location if no block is within distance)                                                                                                                                                                                                                                                                                                                           |
| `@Veinmine{depth=75}`                                                             | <p>Vein mine blocks. You must define whitelist of materials in <code>settings.whitelist</code> in the same block as chance, cooldown, etc.. <a href="https://pastebin.com/raw/fFZGUfD1">Example here.</a><br>Default depth is 75</p>                                                                                                                                                                                            |
| `@Add{x=0.0,y=0.0,z=0.0}`                                                         | Add distance to main entity's location                                                                                                                                                                                                                                                                                                                                                                                          |
| `@Aoe{radius=1,target=all}`                                                       | <p>Area of effect target. Radius is in what radius around a location entities are searched for. Targets are: <br>- ALL <br>- MOBS<br>- DAMAGEABLE (all entities that can damaged by user)<br>- UNDAMAGEABLE (all entities that can't be harmed by user, e.g. allies)<br>--------------------------------------------<br>You can also define a limit for number of entities affected adding option e.g. <code>limit=1</code></p> |
| `@EntityInSight{distance=20,angle=40,limit=5,target=ALL}`                         | Target entities in sight, specify max distance, limit of entities, targets and angle of vision for targeted entities.                                                                                                                                                                                                                                                                                                           |
| `@AllPlayers`                         | All players on the server                                     |



You can use aliases for parameters, which are more concise.

<table data-full-width="false"><thead><tr><th>Name</th><th>Alias</th><th data-hidden></th></tr></thead><tbody><tr><td>ignoretool</td><td>it</td><td></td></tr><tr><td>radius</td><td>r</td><td></td></tr><tr><td>radiuscustom</td><td>rc</td><td></td></tr><tr><td>target</td><td>t</td><td></td></tr><tr><td>limit</td><td>p</td><td></td></tr><tr><td>distance</td><td>d</td><td></td></tr><tr><td>depth</td><td>dp</td><td></td></tr><tr><td>points</td><td>p</td><td></td></tr><tr><td>angle</td><td>a</td><td></td></tr></tbody></table>
