![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

The `config.yml` file holds all the basic configuration of the uSkyBlock plugin.

This is the default config.yml.<br>

```
# The language used in the plugin (en is default).
language: en
options:
  general:
    # [integer] The max number of players allowed in a single party. (including the leader)
    maxPartySize: 4

    # [integer] The time in seconds before a player can use the /island info command again. (note: cooldowns are reset when the plugin is reloaded)
    cooldownInfo: 20

    # [integer] The time in seconds before a player can use the /island restart command again.
    cooldownRestart: 30

    # [integer] The time in seconds before a player can use the /island biome command again.
    biomeChange: 180

    # [string] The default biome assigned to new islands
    defaultBiome: OCEAN

    # [integer] The number of milliseconds between the same notification is sent to the player.
    # This is used when events are triggered heavily - i.e. item-pickup-prevention, damage-prevention etc.
    maxSpam: 2000

    # [string] The name of the skyblock world, will be automatically generated if it doesn't exist.
    worldName: skyworld

    # [integer] Area around 0,0 where islands will not be created to protect spawn.
    spawnSize: 64

  island:
    # [integer] The y-coordinate (height) where islands are spawned.
    height: 150

    # [integer] The number of blocks between islands.
    distance: 128

    # [integer] The size of the protective region for each island. Can't be higher than 'distance'
    # and MUST be divisible by 32 if you intend to use nether.
    protectionRange: 128

    # [filename] The schematic to use for island generation.
    # Put your schematic in the 'uSkyBlock/schematics' folder, you don't need to add the '.schematic' part below.
    schematicName: default

    # [true/false] If true, remove all hostile mobs when a player teleports back to their island.
    removeCreaturesByTeleport: false

    # [item list] The list of items to place in the chest when a player starts a new island. ITEM_ID:HOW_MANY.
    # default is 2 ice, 1 watermelon, 1 cactus, 1 lava bucket, 1 red & brown mushroom, 1 pumpkin seed, 1 sugar cane, 1 sign.
    chestItems: 79:2 360:1 81:1 327:1 40:1 39:1 361:1 338:1 323:1

    # [true/false] If true, add extra items to a chest when a player starts a new island. (for donors and special players)
    addExtraItems: true

    # [integer] The delay in seconds before teleporting to an island. Affects /is home, /is warp, /is spawn
    islandTeleportDelay: 2

    # Allow PvP on the island
    allowPvP: deny

    #[true/false] Allow players to completely lock their islands so non-party members can't enter. (locking still requires permission usb.lock)
    allowIslandLock: true

    # [true/false] If true, use island levels/ranks (/island info) - may have a slight impact on performance
    # Set to false if you have performance issues
    useIslandLevel: true

    # [true/false] Whether or not /is top should be available.
    useTopTen: true

    # [integer] The time in minutes for how often the top-ten list will be re-generated when doing /is top
    topTenTimeout: 20

    # [integer] The time in minutes for refreshing/recalculating the score for players on their island
    # set to 0 to disabled
    autoRefreshScore: 0

    # [true/false] Whether or not to include island-members on the top-ten scoreboard
    topTenShowMembers: true

    # [true/false] Whether or not to try and fix flat-land issues when players join the server
    # Note: will make the PlayerJoin event take longer.
    fixFlatland: false

    # The format used in /islandtalk chat messages
    chat-format: '&9SKY &r{DISPLAYNAME} &f>&d {MESSAGE}'

    # How many entries to remember in the island-log
    log-size: 10

    # Limits the spawning
    spawn-limits:
      # [true/false] if true, the limits below will limit spawning
      enabled: true

      # how many animals can be spawned within an island
      animals: 48

      # how many monsters can be spawned on an island
      monsters: 50

      # how many villagers can be spawned on an island
      villagers: 16

      # how many snowmen and iron-golems can be spawned on an island
      golems: 5

    # [permission] The name of the permissions to check if extra items are added to the chest, you can change these or add more
    # Only checked if 'addExtraItems' is set to true.
    # [permission:item list] The list of extra items to add to the chest, will only be added if the player has the permission. ITEM_ID:HOW_MANY
    # When granting the permission, prefix it with "usb." so the full permission to add would be usb.smallbonus
    extraPermissions:
      smallbonus: '4:16 320:5'
      mediumbonus: '50:16 327:1'
      largebonus: '3:5 12:5'
      giantbonus: '2:1 110:1'
      extremebonus: '352:8 263:4'
      donorbonus: '261:1 262:32 272:1'

  extras:
    # [true/false] If true, return players that don't have an island (this includes players removed from a party while offline), to the server spawn when they login.
    # NOTE: Requires EssentialsSpawn or another plugin with the "/spawn" command
    sendToSpawn: false

    # [true/false] If true, a player can right-click on a block of obsidian on their island while holding an empty bucket to remove the obsidian and fill the bucket with lava. This is useful for people that accidently
    # turn their lava into obsidian with a bad cobblestone generator design. Will only work on the player's island and if there are no other obsidian blocks nearby (so can't be used on portals).
    obsidianToLava: true

  # Contains flags for enabling PROTECTION of various mechanics.
  protection:

    # Whether or not, items dropped on the ground should be limited to party-members.
    item-drops: true

    # If true, only creepers targeting party-members will explode
    creepers: true

    # If true, Withers will be limited to harming island-members/island blocks.
    withers: true

    # Whether or not the plugin will try to protect the player from accidentally extinguishing lava
    protect-lava: true

    # Whether or not portalling to the nether roof should be blocked.
    nether-roof: true

    visitors:
      # Protect visitors from trampling your crop
      trampling: true

      # Protect against visitors attacked animals
      kill-animals: true

      # Protect against visitors attacking monsters
      kill-monsters: true

      # Protect from shearing
      shearing: true

      # Protect from villager-trading
      villager-trading: true

      # Whether or not visitors are protected from fall damage
      fall: true

      # Whether or not visitors are protected from fire damage (incl. lava)
      fire-damage: true

      # Whether or not visitors should be allowed to drop items
      item-drops: true

      # Warns online members when a player visits the island.
      warn-on-warp: true

      # Whether or not to actively block banned players from entering an island (by walking/flying).
      block-banned-entry: true

      # Whether or not visitors can use portals (default: false)
      use-portals: false

  party:
    # The number of ticks before an invite timeouts (20 ticks per sec.)
    invite-timeout: 600

    # The format used in /partytalk chat messages
    chat-format: '&9PARTY &r{DISPLAYNAME} &f>&b {MESSAGE}'

  # This section provide some performance tweaking configs
  advanced:
    # If true, display-name is looked up (might be performance intensive).
    useDisplayNames: false

    # [number] The threshold for purging islands.
    # any island with a level above this, is spared.
    purgeLevel: 10

    # [seconds] The number of seconds for confirming a command by
    # re-executing it (/is leave, /is restart).
    confirmTimeout: 10

  # Section about restarting your island (or accepting an invite).
  restart:
    # Clears the player's inventory on island create/restart
    clearInventory: true
    # Clears the player's armor on island create/restart
    clearArmor: true
    # Clears the player's enderchest on island create/restart
    clearEnderChest: true

    # [ticks] The number of ticks to wait, before porting the player back
    # on /is restart or /is create (default: 40)
    teleportDelay: 20

    # [true/false] Whether or not the player should be auto teleported to the island when it's ready
    teleportWhenReady: true

    # list of commands to execute after island-creation
    # i.e.
    # - me Jumps with &ajoy
    extra-commands: []

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
    # optional, default true (true enabled in GUI, false disabled in GUI)
    enabled: true
    # optional, must be listed in ascending order
    index: 2
    # optional extra's that can be given per island
    extraItems: ''
    maxPartySize: 4
    animals: 48
    monsters: 50
    villagers: 16
    golems: 5
  skySMP:
    permission: usb.schematic.skysmp
    description: The original SkySMP island
    displayItem: GRASS
    extraItems: 'OBSIDIAN:14 FLINT_AND_STEEL:1'
    # Only get 90% of the normal score
    scoreMultiply: 0.9
    # But start with an offset of 40
    scoreOffset: 40

# This section allows donors to get specific perks
#donor-perks:
#  usb:
#    donor:
#      example:
#        # permission: usb.donor.example will give the below extra items
#        maxPartySize: 5
#        schematics: [LargeIsland]
#        animals: 60
#        monsters: 100
#        villagers: 24
#        rewardBonus: 0.5
#        hungerReduction: 0.5

confirmation:
  # [true/false] Whether to require confirmation (i.e. repeating the command twice).
  is leave: true

  # [true/false] Whether to require confirmation (i.e. repeating the command twice).
  is restart: true

asyncworldedit:
  # Supports disabling the detection of AWE
  enabled: true

  # Show progress to the user every 5 seconds
  progressEveryMs: 5000

  # Or 20pct (what-ever comes first)
  progressEveryPct: 20

  watchDog:
    # The maximum time to wait for AWE paste to complete (2m, 3m20s, etc.)
    timeout: 15s
    # The number of ms between each heartbeat
    heartBeatMs: 2000

worldguard:
  entry-message: true
  exit-message: true


nether:
  enabled: true

  terraform-enabled: true

  # The distance to search for valid terra-form location.
  terraform-distance: 7

  height: 75

  lava_level: 7

  activate-at:
    level: 100

  schematicName: uSkyBlockNether

  # The probability of forming blocks
  terraform:
    NETHERRACK:
      - '{p=0.7}NETHERRACK'
      - '{p=0.15}NETHERRACK'
      - '{p=0.05}QUARTZ_ORE'
      - '{p=0.05}SOUL_SAND'
    QUARTZ_ORE:
      - '{p=0.50}QUARTZ_ORE'
      - '{p=0.10}QUARTZ_ORE'
    SOUL_SAND:
      - '{p=0.70}SOUL_SAND'
      - '{p=0.10}SOUL_SAND'
    GRAVEL:
      - '{p=0.60}GRAVEL'
      - '{p=0.10}GRAVEL'
      - '{p=0.05}SOUL_SAND'
    GLOWSTONE:
      - '{p=0.85}GLOWSTONE'
      - '{p=0.15}GLOWSTONE'

  spawn-chances:
    enabled: true
    wither: 0.20
    skeleton: 0.10
    blaze: 0.20

tool-menu:
  enabled: true
  tool: SAPLING
  commands:
    CHEST: 'island'
    BEDROCK: 'island spawn'
    WORKBENCH: 'challenges'

# Placeholders - enable these to get placeholder substitution
# usb_version
# usb_island_level, usb_island_rank, usb_island_partysize_max, usb_island_partysize
# usb_island_leader, usb_island_bans, usb_island_members, usb_island_trustees
# usb_island_biome, usb_island_schematic
# usb_island_location, usb_island_location_x, usb_island_location_y, usb_island_location_z
# usb_island_golems_max, usb_island_monsters_max, usb_island_animals_max, usb_island_villagers_max,
# usb_island_golems, usb_island_monsters, usb_island_animals, usb_island_villagers
placeholder:
  # Hooks into MVdWPlaceholderAPI
  mvdwplaceholderapi: false
  # uSkyBlock native placeholders for chat messages and format
  chatplaceholder: false
  # uSkyBlock native placeholders for server-commands
  servercommandplaceholder: false

# DO NOT TOUCH THE FIELDS BELOW
version: 51
force-replace:
  options.party.invite-timeout: 100
  options.island.islandTeleportDelay: 5
  options.island.useOldIslands: false
  options.island.schematicName: yourschematichere
move-nodes:
  options.restart.confirmation: confirmation.is restart
  options.party.leave.confirmation: confirmation.is leave
```
In case of added custom island in the `island-schemes` section you can add the following code to prevent it from updating
```
# this will ignore island-schemes from updating
merge-ignore:
  - 'island-schemes'
```