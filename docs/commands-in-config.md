![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

**OBSOLETE: Using config-options only available before Bukkit 1.13 SHOULD BE UPDATED!**

In various places, the uSkyBlock plugin supports the server-administrator to configure specific custom commands.

These include:
* _rewards_ on challenges (See [[Challenges]])
* _extra-menu-items_ in the main menu (See [[Config]])
* _tool-menu_ commands when interacting with blocks using a sapling (See [[config.yml]])
* and when creating an island (See [[config.yml]])

# Syntax

```
[{p=<prob>}] [{d=<delay>}] [op:|console:] <command>
```
The `[]` denotes optional arguments, the order IS significant, and `|´ denotes one OR the other.

Here `probability` is a decimal-number between `0` and `1` - i.e. `{p=0.2}` will execute the command 20% of the times.

The `delay` is an integral number of ticks, note that 1 second is 20 ticks.

`op:` will execute the command as the player, but OPed.

`console:` will execute the command from the console.

## Placeholders

| Placeholder | Meaning |
| ----------- | -------- |
| `{player}` | The name of the player |
| `{playerName}` | The display name of the player (including pre and postfix, and formatting codes) |
| `{position}` | The position of the player in the format `world:x,y,z:yaw:pitch` |
| `{party}` | Will execute the command once for each member of the party, replacing `{party}` with the member-name |

## Examples
```
commands:
  # Regen for 10 seconds, then jump-boost for another 10
  - 'op:effect {party} 10 10'
  - '{d=200}op:effect {player} 8 10'
```