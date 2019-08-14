![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

Since we have quite often experienced regressions, this document aims at specifying both a minimal and a more comprehensive list of test-cases that should be executed (manually) before releasing minor or major versions of uSkyBlock.

# Basic Usage
These tests verifies the most basic usage of the plugin.

## Single Player - Creation, Challenges and Restart

__Pre:__ No island
  * `/is` - Check that the UI is shown
  * `/is create` - Verify that an island can be created.

__Pre:__ Island exists
* `/is` - Verify the island menu
  * Verify the availability of sub-menus
  * Verify it's possible to complete a challenge using the menu
* `/c c co<tab>` - Verify tab-completion
* `/c c cobblestonegenerator` - Verify message when items are missing

__Pre:__ 64 cobblestone
* `/c c cobblestonegenerator` - Verify message and rewards on first completion

__Pre:__ Less than 66 cobblestone
* `/c c cobblestonegenerator` - Verify message when items are missing

__Pre:__ More than 66 cobblestone
* `/c c cobblestonegenerator` - Verify message and rewards for 2nd completion

__Pre:__ Make sure theres stuff in inventory and armor in armor-slots and entites on the ground and that the island has blocks in all direction (preferably to all 4 corners + blocks at 0 + 255).
* `/is restart` - Restart island
  * Verify inventory and armory has been cleared.
  * Verify there is no entities on the ground.
  * Verify that the island blocks were cleared (all the way to all boundaries).
* `/is level` - Verify the level is shown
* `/is info` - Verify a list of blocks on the island is shown

## Party

## Others / Top / Warp
