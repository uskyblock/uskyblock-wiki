![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

uSkyBlock supports custom-islands by world-edit (or mcedit) schematics.

Rules:
* Schematic must be placed in `/plugins/uSkyBlock/schematics`
* Schematic must contain
  * 1 (and only ONE) BEDROCK (obsolete from v2.6.0)
  * 1 (or more) Chests (the one closest to bedrock defines the spawn point).
    * The chest should be within 15 blocks of the bedrock

## Creating a Schematic
* Create an island following the above rules.
* Use World-Edit to mark the island (`//wand` or what-ever suits you).
* Copy the island using World-Edit (`//copy`)
  * Note: The place you stand at the time of copy, will be the center of the island.
* Save the copy as a schematic (`//schem save MyIsland`)

Now World-Edit will have placed a schematic in your `/plugins/WorldEdit/schematics` folder.

## Installing a custom default Schematic in uSkyBlock

* Copy the schematic to your `/plugins/uSkyBlock/schematics` folder.
* Make sure to change the `config.yml` to name the schematic:
```yml
      island:
        # [filename] The schematic to use for island generation.
        # Put your schematic in the 'uSkyBlock/schematics' folder,
        # you don't need to add the '.schematic' part below.
        schematicName: MyIsland
```
* You need to add your custom island to the config as explained in the next section for "multiple islands".
* Reload config `/usb reload`

Tada, now players should get your custom made schematic when they do `/is create`.

## Adding multiple islands

You can now add multiple island and choose one from a GUI. 
```yml
# List of selections for /is create and /is restart
# the nodes under island-schemes must match the schematic-names from the schematics folder.
island-schemes:
  # name of the schematic
  default:
    # permission needed to use island
    permission: usb.island.create
    # small discription of the island
    description: The default uSkyBlock island
    # item to display in the GUI
    displayItem: SAPLING
    # optional, default true
    enabled: true
    # optional, must be listed in ascending order
    index: 2
    # optional extra's that can be given per island
    extraItems: ''
    maxPartySize: 4
    animals: 48  # animal limit per island
    monsters: 50  # monster limit per island
    villagers: 16  # villager limit per island
    golems: 5 # golem limit per island
    rewardBonus: 0.5  # currency bonus per island
    hungerReduction: 0.5  # hunger depletion per island
    extraItems: '43:8'  # extra items per island per island
```
Copy for each island the default example and paste it back into the config. Rename "default" to your own custom name (without the _.schematic_). You can add up to 52 different custom island with for each island custom value's.

## Controlling access to custom-islands

uSkyBlock will chose the "best-match" as an island for any player performing `/is create`.

The rules will follow this:
* Does the player have permission `usb.schematic.<schematic-name>`?
  * Use this schematic as island
* Does any of the schematics match the `options.island.schematicName` name?
  * Use this schematic as island
* Is `options.island.useOldIslands` set?
  * Generate a skySMP like island
* Else
  * Generate the default uSkyBlock island