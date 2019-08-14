![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

This page tries to list the features provided by uSkyBlock.

It might not be complete, but it will out-line the major features.

# Features

* [Advanced Graphical User Interface](#gui)
* [Customizable Challenges](#customizable-challenges)
* [Customizable Island Scoring](#island-score)
* [Social Party Features](#party)
* [Advanced Grief Prevention](#grief-prevention)
* [Nether](#nether)
* [Custom Schematics](#custom-schematics)

## GUI
The plugin has a user-friendly Graphical User Interface (GUI), which can be accessed by either invoking the `/is` command, or by right-clicking a `chest` with an `oak sapling`.

## Customizable Challenges
Challenges can be accessed either by invoking the `/c` command, accessing it clicking on the `diamond ore` in the main menu, or finally, by right-clicking a `workbench` with an `oak sapling`.

Challenges comes in two variants, `onIsland`; where you are required to have a specific number of blocks or entities in an area around you, or `onPlayer` where you are required to carry a specific combination of items.

Usually, completing a challenge for the first time, will give you a reward which is important for completing other challenges (i.e. items you can not get "naturally" from your island).

Most `onPlayer` challenges are repeatable, meaning you can turn in an increasing number of items for a smaller repeat-reward.

## Island Score
All islands get a score depending on the blocks placed within the island-region.

The score each block gives can be fully customized by the server-owners, by editing the `levelConfig.yml` file (for *advanced use ONLY*).

Blocks can be *grouped* together, so say all block-ids representing *planks* share the same score and limits.

Groups can be *limited*, either by imposing a hard limit (`blockLimits`) or by setting a `diminishingReturns` at which point the score per block will decrease.

## Party
Island-owners can cooperate with other players, either by inviting them to join their island (`/is invite <name>`) or by allowing them to build/farm/help on their island `/is trust <name>`.

Additionally, an *island wide chat* or *party wide chat* is available using `/istalk` or `/ptalk`.

## Grief Prevention
A detailed feature-set allows server-owners to disable certain types of griefing.

Only `members` or `trustees` can:
* break blocks or build on an island
* pickup dropped items on an island
* shear sheep
* trade villagers
* take portals
* trample crops
* make a creeper explode
* kill monsters/animals
* hatch eggs
* take fall damage
* take fire damage
* drop items

Additionally server-owners can control how many mobs of different types, each island is allowed to spawn. This can also be controlled using [perks](#advanced-perk-system).

## Nether
uSkyBlock supports allowing the player to also get a "skyblock feeling" when entering the Nether.

A custom-schematic can be provided, and a custom "terra-forming" (fully configurable) allows players to randomly generate new blocks, when they mine the existing ones in the nether.

Additionally, server-admins can control custom-spawning on nether-bricks, allowing players to build their own nether-fortresses, and farm wither-skulls, blazes and similar mobs on their own "nether-island".

## Custom Schematics
Server owners can supply custom-schematics, to either change the default skyblock game-play, or allow for different starting points. These can also have custom nether-counter-parts for when the player reaches the nether.

To counter the disadvantage such schematics can have on the [island scoring](#island-score), each custom-schematic can be assigned both a `scoreMultiply` and a `scoreOffset` - to allow differently sized starting-islands, to still compete on the top-10 list.

## Advanced Perk System
Almost all perks that can be configured in the plugin, can be controlled by adding permission-nodes to the `config.yml`.
That is, access to:
* Biomes
* Schematics
* ExtraItems - get some extra goodies in the starting chest
* Max-Mobs (animals, mobs, golems, villagers)
* Reduced Hunger
* Bonus on XP/Currency rewards