![uSkyblock-Revived](http://i.imgur.com/ayEiaCi.jpg|uSkyblock-revived)

# This page is outdated and needs updating

###Setting up the Nether-World.

For the setup with Multiverse you need also the [Multiverse-NetherPortals](http://dev.bukkit.org/bukkit-plugins/multiverse-netherportals) plugin

When using Mutiverse, use the command:
* /mv create skyworld_nether NETHER.

This will create your nether world special for the skyblock game. By default, when creating a Nether-Portal in the skyworld, the portal is looking for a netherworld called "skyworld_nether" hens the name I use.

###Custom named Nether-World

You can give the nether any name you like but then you need to "link" the skyworld to your custom named netherworld.<br>
This can be done with the commands from Multiverse-NetherPortals plugin:
* /mvnp link nether skyworld [your custom named world] and 
* /mvnp link nether [your custom named world] skyworld.

You need to run both commands as linking goes only 1 way (and your players like to get back to their island too).<br>
To go to the new created nether-world use the command:
* /mvtp skyworld_nether.

This is needed as you have to set the scale in the skyworld_nether.

###Set the scaling

When in the skyworld_nether do the following command to set the scale right:
* /mvm set scale 1.0.

The default scale is for the netherworld is 8.0 but when left it will make the return portal in mid air. (see pic below)
![portal](http://i.imgur.com/9ykYdBx.png?1)

Restart the server after to let the scale take effect (or it wont work).

###Using Multiworld _(not recommended)_

When using Multiworld, use the command:
* /mw create skyworld_nether nether

After that you need to link the 2 worlds with:
* /mw link skyword skyworld_nether
* /mw link skyworld_nether

_As there is limited information about this plugin I can't give you anything more then I can find. I'm not sure when linking the 2 worlds if it's 1 way or both ways. The other thing I cant find is how to set the scale from 8.0 to 1.0. As this is very important I can not recommend this option. (if anybody has this info plz message me here or at the forum)._