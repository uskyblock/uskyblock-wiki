![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

# How do I get a SkyGrid gameplay?

If you want to try out SkyGrid gameplay using UltimateSkyBlock, this is doable from v2.5.9 and onwards.

# Installation Guide

## Before you begin
You will need the following:

1. The jar files for uSkyBlock and UltimateSkyGrid
1. A minimal valid uSkyBlock schematic (1 chest + 1 spawn block), called [mini.schematic](schematics/mini.schematic)
1. A minimal/empty/portal schematic for uSkyBlock in nether, called [netherMini.schematic](schematics/netherMini.schematic)
1. A spawn world different than the skyworld.

## Installing
1. Download and install the UltimateSkyGrid plugin (https://dev.bukkit.org/bukkit-plugins/ultimate-skygrid/files/19-ultimate-sky-gridv-0-2-31/)
1. Download and install UlimateSkyBlock >= v2.7.2
1. Start server
1. Shutdown server
1. Edit the configuration files as described below and place the schematics under `uSkyBlock/schematics`.
1. Delete `skyworld` and `skyworld_nether` worlds (this is imperative to get the SkyGrid worlds generated!)
1. Start the server

## Configuration of UltimateSkyGrid
1. Set the `AllBlocksOneWorld` to `false`
1. Optionally set the `World_Height` to something above `128` (will have a performance impact).

## Configuration of uSkyBlock
1. Edit the `config.yml` file in an appropriate editor (Notepad++)
1. Locate `options.general` section
  1. Set `spawnSize: 0`
1. Locate `options.island` section
  1. Set `height: 65`
  1. Set `schematicName: mini`
  1. Set `chestItems: ''` - No additional items to begin with (grid-playstyle)
  1. Set `addExtraItems: false`
  1. Set `useIslandLevel: false` - the `/is info|level|top` doesn't make sense in SkyGrid.
1. Locate `options.extras` section
  1. Set `sendToSpawn: true` - So we can have islands form around spawn.
1. Locate `options.advanced` section - IMPORTANT!
  1. __Add__ (in one line) `chunk-generator: com.gmail.labuff.shane.UltimateSkyGrid.UltimateSkyGridGenerator`
1. Locate `nether` section
  1. Make sure `enabled: true` - we want the chunk-generator to be active
  1. Set `schematicName: netherMini` - we don't want the full nether island
  1. Set `terraform-enabled: false`  - we don't want terraforming in nether
  1. __Add__ `chunk-generator: com.gmail.labuff.shane.UltimateSkyGrid.UltimateSkyGridGenerator`
  1. Set `spawn-chances.enabled: false` - No additional spawning on netherbricks

Start the server again, and you should get a SkyGrid play-style controlled by uSkyBlock.

## Further Configuration
If you want to include entitites from Bukkit 1.8+, edit the UltimateSkyGrid configurations to include blockIds as you see fit.

## TroubleShooting
__I get the wrong island??__
Perhaps you are OPed, and have more than one schematic? The `schematicName` for the normal island will only come into play, if you do not have any of the specific schematic permission nodes for any of the other schematics (including the empty nether schematic, that is essentially an invalid overworld schematic).