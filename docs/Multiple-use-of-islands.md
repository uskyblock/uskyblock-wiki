![uSkyblock-Revived](http://i.imgur.com/JbSV18m.png)

**OBSOLETE: Using config-options only available before Bukkit 1.13 SHOULD BE UPDATED!**

I got a question in github but it's best to be explained here so everyone can have the benefits of it.
>
alepalma wrote:<br>
I've seen the config and I'm not sure I get it. What I understood from the config file is that you can change the default island with a schematic you want, and items in the chest you want etc... What I was wondering if there's a way to make more than one island, because I want to assign an island to each rank<br>

>For example<br>
Default  > island_default.schematic ; items in chest: 3 10 11<br>
Iron  > island_iron.schematic ; items in chest 3 10 11 15 17<br>
Gold > island_gold.schematic ; items in chest 3 10 11 15 17 18<br>

>and so on and so on. This is just an example of what i would like to be able to do ( IDK if i m already able to) with of course all the specifiactions already included in the uSkyBlock config>island section<br>

>Thank You very much!


All this is possible with uSkyblock.

I'll put it in sections as discribed above (Default, Iron, Gold).

Default:<br>
For this you have to do the minimum changes.<br> In the config you only change the default "chest" items:
```yml
chestItems: 3:1 10:1 11:1
```
To let everybody starts off with a custom default island you change in the config:
```yml
schematicName: island_default
```
There is no need for a permission here as this applies to everybody.<br>
Which gives 1 of each default item and the island island_default.

If you use the default uSkyblock island you dont need to change the "schematicName"

Iron:<br>
Players that can have this must have the permission `usb.schematic.island_iron`(this overwrite the island_default).<br>
To give them the extra items you have to work with the "extraPermissions" from the config.You can alter the default "extraPermissions" that are present in the config or you can add your own ones. For this explanation I alter a default "extra-smallbonus". <br>
```yml
    extraPermissions:
      smallbonus: 15:1 17:1
```
To let players have these "extra" items they need the permission `usb.smallbonus`.<br>
Which gives 1 of each item + the default items and the island island_iron.<br>

Gold:<br>
Players that can have this must have the permission `usb.schematic.island_gold`(this overwrite the island_default).<br>
This works the same as in "Iron" to give the "extra" items.<br>
For this explanation I use "my own" extra.<br>
```yml
    extraPermissions:
      myowntext: 15:1 17:1 18:1
```
To let players have these "extra" items they need the permission `usb.myowntext`.<br>
Which gives 1 of each item + the default items and the island island_gold.<br>

As both Iron and Gold get the "default" chest items you don't need to add these to the "extraPermission" bonusses.<br>
If an island from the previous rank is still given you might need to negate the previous island before it gives the new island.