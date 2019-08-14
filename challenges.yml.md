![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

The `challenges.yml` file contains both some default configuration of challenges, as well as the actual challenges and ranks.

# Common Setup
The first section of the configuration file is used to setup default-values and various common configuration parameters.

# Ranks
Ranks consist of some basic information (`name`, `displayItem`) and a list of challenges.

A rank can have some requirements (`requires`) to under which circumstances it becomes available.

# About the Challenge GUI

The challenge GUI does now support paging.<br>
To goto the next page, with the default setup, you can click on the "rank" blocks.<br>
The top 3 are going back a page, the bottom 3 are going forward a page.
When adding challenges into the config, the config will automatic put them into pages and create the next page if needed.<br>
We have changed the format slightly to make use of challenges "groups" (ChallengeGroupX). Each group can now be custom named to accomplice the challenges.<br>
I hope with the added explanation (at the bottom of the file) server owners can now easily create their own challenges and if they want share them with us.<br>
If we like the challenge(s) we might even add them to the plugin ;)

You can, from version uskyblock v2.4.7, add more then 8 challenges per rank. When using more then 8, it will continue on the next line except using the first slot. All other challenges will then move down accordingly or to the next page.

A new section is added to support custom challenges not being overwritten when updating the plugin. Uncomment the 2 lines (top line is explanation only) to activate this for custom challenges.
```
# this will ignore a the challenges from updating
#merge-ignore:
#  - 'ranks'
```

# Challenges
Challenges define a contract, between what items are required, how they are required and what *rewards* are rewarded upon completion.

Challenges are customized skyblock goals that a player can complete on his island for a reward.<br>
To be able to use the challenges your players need the _**usb.island.challenges**_ permission.<br>
Access the challenges by using **/challenge** or **/c**. See information about a challenge by using **/challenge [challengename]**.<br>
Attempt to complete a challenge by using **/challenge complete [challengename]** or **/c c [challengename]** for short.

This is the default challenges.yml.<br> 

```
# [true/false] Enable the use of the challenges command.
allowChallenges: true

# [island/player] Whether challenges are tracked per player, or per island
challengeSharing: island

# [true/false] If true, first time challenge completions are broadcast to the whole server.
broadcastCompletion: true

# [text] The color/formatting of the broadcast text when showing first time completions.
broadcastText: §6

# [true/false] If true, challenges in higher level ranks require challenges in lower level ranks to be completed.
requirePreviousRank: true

# [integer] The number of tasks per rank that can be left uncompleted to advance to the next rank. For example, if you have 4 easy challenges
# with a rankLeeway of 1, a player would only need to complete 3 to advance to the next rank.
# A rankLeeway of 0 would require them all.
rankLeeway: 1

#[integer] The time in hours before required items reset to default. (only if not specified in the challenges below)
defaultResetInHours: 20

#[color code] The color to use for uncompleted challenges in the list.
challengeColor: §e

#[color code] The color to use for completed challenges in the list. (non-repeatable)
finishedColor: §2

#[color code] The color to use for completed challenges in the list. (repeatable)
repeatableColor: §a

#[true/false] If true, enables vault to handle currency rewards.
enableEconomyPlugin: true

# [true/false] If false, challenges are not reset on island creation (or restart)
resetChallengesOnCreate: true

# Material to show for locked challenges (i.e. STAINED_GLASS_PANE:14 for a red glass-pane, or 160:14)
lockedDisplayItem: STAINED_GLASS_PANE:14

# this will ignore a the challenges from updating
#merge-ignore:
#  - 'ranks'
    
#===============================================
# An explanation to setup your own challenges 
# can be found at the bottom of this file.
#===============================================

ranks:
  ChallengeGroup1:
    name: '&aDefault Challenges'
    displayItem: 4
    resetInHours: 20
    challenges:
      cobblestonegenerator:
        name: '&aCobble Stone Generator'
        description: Mine from a cobblestone generator.
        type: onPlayer
        requiredItems: '4:64;+2'
        repeatable: true
        displayItem: 1
        resetInHours: 12
        takeItems: true
        reward:
          text: 3 leather, 20% chance to get a book
          items:
          - '334:3'
          - '{p=0.02}340:1'
          permission: none
          currency: 10
          xp: 10
          commands:
          - op:effect {playername} 10
        repeatReward:
          text: 1 leather, 10% chance to get a book
          items:
          - '334:1'
          - '{p=0.01}340:1'
          currency: 5
          xp: 5    
     
#===============================================
       
  ChallengeGroup2:
    name: '&aFarmer Challenges'
    displayItem: 290
    resetInHours: 20
    requires:
      rankLeeway: 5
      challenges:
      - cobblestonegenerator
    challenges:
      applecollector:
        name: '&aApple Collector'
        description: Collect apples from trees.
        type: onPlayer
        requiredItems: '260:2;+1'
        repeatable: true
        displayItem: 260
        resetInHours: 6
        takeItems: true
        reward:
          text: 1 of each sapling, (4 dark oak)
          items:
          - '6:0:1'
          - '6:1:1'
          - '6:2:1'
          - '6:3:1'
          - '6:4:1'
          - '6:5:4'
          - '{p=0.2}6:3:3'
          permission: none
          currency: 20
          xp: 20
        repeatReward:
          text: 1 of each sapling (4 dark oak)
          items:
          - '6:0:1'
          - '6:1:1'
          - '6:2:1'
          - '6:3:1'
          - '6:4:1'
          - '6:5:4'
          - '{p=0.1}6:3:3'
          currency: 10
          xp: 10
      
#===============================================  
# The full list of challenges will linked at the bottom
#===============================================
#
# Here follows the format and explanation for the challenge group and challenges setup. The single commented (#) are the most used settings 
# while the double commented (##) are optionnal if you like to use those settings.
#
#ranks:
#  # [text] name of the challenge Rank.
#  ChallengeGroupX:
#    #[text] The name of the challenge rank that shows up when you do /challenges (this supports capitals and colorcodes).
#    name: '&aCuston Challenges rank name'
#    # [itemid] The itemid of the item to be displayed in the challenge menu for complete challenges.
#    displayItem: 3
#        # [integer] The time in hours before required items reset to default (tis overwrites the Main reset time)
#    resetInHours: 20
#    # The requierments will allow when a challenge groups will be available to see and complete for players.
#    requires:
#      # [integer] The number of tasks per rank that can be left uncompleted to advance to the next rank. For example, if you have 4 challenges
#      # with a rankLeeway of 1, a player would only need to complete 3 to advance to the next rank.
#      # A rankLeeway of 0 would require them all.
#      rankLeeway: 8
#      # [text] Challenges that has to be completed before this group will show in the Challenges GUI
#      challenges:
#      - a challenge name
#===============================================
#    challenges:
#      #[text] The name of the challenge. All challenge names should be lower case.
#      defaultchallengename:
#      #[text] The name of the challenge that shows up when you do /challenges (this supports capitals and colorcodes).
#        name: '&a'
#        # [text] What the player sees when they do /challenges <challengename>
#        description:
#        # [onIsland/onPlayer/islandLevel] This tells whether the required blocks/items should be in the player's inventory or on their island
#        # When using onIsland, the player must be 10 blocks away from the required blocks on his island.
#        # When using onIsland, the default radius distance is set to 10, all items requierd must be within this distance.
#        # When using islandLevel, the 'requiredItems' field should be the island level required. The player must use /island level first to update his level.
#        type: onPlayer
##        type: islandLevel
##        type: onIsland
#        # To override the default radius when using onIsland, uncommend the "radius: " and fill in your own value.
##        radius:
#        # [itemid list] The itemid:count of the items required for the challenge.
#        requiredItems: ''
#        # [true/false] If the challenge can repeated or not.
#        repeatable: true
#        # [itemid] The itemid of the item to be displayed in the challenge menu for complete challenges.
#        displayItem:
##        tool:
#        # [integer] The time in hours before required items reset to default (this overwrites the Main and Ranks reset times).
##        resetInHours:
#        # [true/false] Take required items on completing a challenge.
#        takeItems: true
#        # reward section to reward the player for completing the challenge.
#        reward:
#          # [text] Description of the reward. If omitted §4Unknown will be shown.
#          text:
#          # [itemid list] The itemid:<datavalue>:count of the reward to give the player for completing the challenge.
#          items:
##          # [permission node] A permission granted for completion. Multiple permissions are space-separated, i.e. - "test.1 test.2" (use none to not give a permission)
#          permission: none
#          # [integer] How much currency to give for the first time completion. (requires an economy plugin)
#          currency: 0
#          # [integer] How much xp to give to the player for the first time completion.
#          xp: 0
#          # Executes the given command upon completion. Prepend with "op" or "console" to run the commands as OP or from the Console. Examples:
#          # commands:
#          # - 'op: me are the GOD of things'
#          # - 'console: give {party} aweseomestuff 32'
#           # Possible command arguments are:
#           # {player}     - The name of the player
#           # {playerName} - The display name of the player
#           # {challenge}  - The name of the challenge
#           # {position}   - The position of the player
#           # {party}      - Execute the command once for each member of the party (substituting the name)
##          commands:
##          - op:
##          - console:
#        # reward section to reward the player for completing a repeated challenge.
#        repeatReward:
#          # [text] Description of the reward. If omitted §4Unknown will be shown.
#          text:
#          # [itemid list] The itemid:<datavalue>:count of the reward to give the player for completing the challenge.
#          items:
##          # [integer] How much currency to give for the first time completion. (requires an economy plugin)
#          currency: 0
#          # [integer] How much xp to give to the player for the first time completion.
#          xp: 0
#          # Executes the given command upon completion. Prepend with "op" or "console" to run the commands as OP or from the Console. Examples:
#          # commands:
#          # - 'op: me are the GOD of things'
#          # - 'console: give {party} aweseomestuff 32'
#           # Possible command arguments are:
#           # {player}     - The name of the player
#           # {playerName} - The display name of the player
#           # {challenge}  - The name of the challenge
#           # {position}   - The position of the player
#           # {party}      - Execute the command once for each member of the party (substituting the name)
##          commands:
##          - op:
##          - console:
#
# DO NOT CHANGE!
version: 19
```

Link to the full challenges.yml can be found [here](https://github.com/rlf/uSkyBlock/blob/master/uSkyBlock-Core/src/main/resources/challenges.yml)