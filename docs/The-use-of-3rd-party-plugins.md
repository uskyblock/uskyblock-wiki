![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

### uSkyblock 3rd party plugins

The uSkyblock 3rd party plugins Files contain folders with config files to enhance the uSkyblock experiance.<br>
This RAR file contains:

* Chest Command GUI configs (buy, donor and island_help YML's).
* TitleManager configs.
* Scavenger configs.
* A command YML.
* An explanation text file.

The download of these config files will be on the bottum of this page in RAR format.<br>
A link to these plugins can be found in the "explanation" file.

---
### Chest Command GUI.

The "Buy Perks" is a feature that can be used to let players buy items or special perks for their island.
To make use of this feature you need an aditional plugin called [Chest Command GUI](http://dev.bukkit.org/bukkit-plugins/chest-commands/).

![perks](http://i.imgur.com/Z4s0nX0.png?2)

When you have Chest Command GUI installed you will have to make a new file called "perks.yml" and place it in the "menu" folder from Chest Command GUI (see picture above).<br>
The easiest way is to take an excisting file from the menu folder and rename it "perks.yml". This way you have the right setup to start adding your own perks.<br>

![perks](http://i.imgur.com/4ou7i6n.png)

Each Chest Command GUI menu file has to have an unique name (see picture above). If this name isn't unique it will not work.<br>Configure the "items" to your liking. More information on how too can to be found on the Chest Command GUI [basic tutorial](http://dev.bukkit.org/bukkit-plugins/chest-commands/pages/tutorial/basics/) site.<br>

![perks](http://i.imgur.com/YJgXu7F.png)

This is an example picture similar as on the uSkyblock server.<br>The "Buy Donor Perks" (the enderchest in the GUI) can be used when the player or rank has the permission group.donor.<br> Make a donor.yml just as you did the perks.yml. This donor.yml can have all different items/perks.

![Imgur](http://i.imgur.com/0e113kT.png?1A)

This is an example picture similar as on the uSkyblock server.<br>The "island_help" (the wooden sign in the begin GUI).<br> Make an island_help.yml just as you did the perks.yml. This island_help.yml can have all the rules and info you would like your players to know.

---

### Scavenger

This is needed for the "sticky fingers" option in the second part of the perks file.
Not much setup needed for this as it's all command based and added automatic to the users file.
Just make sure you are using a version of ProtovolLib for 1.8.

---

### Title Manager

This plugin is abandoned but still works perfect for this.<br>
This is needed for the top row with the custom prefixes you can buy.<br>
Looking at the setup I made you'll see it will speak for itself.<br>
Due to the long command it has I have given them an alternative in the "commands.yml" in your main server folder. This was needed to make it all fit in the lore of the perk/donor items.<br>

All default ranks above the uSkyblock line are from my own server, adjust them to your own liking, not sure that when you delete that section your own ranks will be showing properly(I havent tested that as mine are set this way).

---
### Download
Click [here](http://debocraft.x10.mx/skyblock/downloads/uskyblock_extras.rar) for the download.<br>
This file has been updated on 07-04-2015.<br>
Change Log:
* Chest Command GUI
  * yml's updated to support spigot 1.8.x items.
  * Missing items added.
  * Some text changed.
  * Internal links fixed
  * Deleted "main-menu.yml" as this is not needed for USB use.
* Scavenger
  * no changes.
* TitleManager
  * no changes.