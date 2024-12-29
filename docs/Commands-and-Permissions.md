```
Command                                                | Permission                  | Description                                      
-------------------------------------------------------+-----------------------------+--------------------------------------------------
/challenges|c                                          | usb.island.challenges       | complete and list challenges                     
/c complete|c <challenge>                              | usb.island.challenges       | try to complete a challenge                      
/c info|i <challenge>                                  |                             | show information about the challenge             
-------------------------------------------------------+-----------------------------+--------------------------------------------------
/island|is                                             | usb.island.create           | general island command                           
                                                       | usb.island.signs.place      | allows user to place [usb] signs                 
                                                       | usb.island.signs.use        | allows user to use [usb] signs                   
                                                       | usb.mod.bypasscooldowns     | allows user to bypass cooldowns                  
                                                       | usb.mod.bypassprotection    | allows user to bypass visitor-protections        
                                                       | usb.mod.bypassteleport      | allows user to bypass teleport-delay             
/is accept|reject                                      | usb.party.join              | accept/reject an invitation.                     
/is auto                                               | usb.island.create           | teleports you to your island (or create one)     
/is ban|unban <player>                                 | usb.island.ban              | ban/unban a player from your island.             
                                                       | usb.exempt.ban              | exempts user from being banned                   
/is biome|b <biome> [radius]                           |                             | change the biome of the island                   
                                                       | usb.biome.deep_ocean        | Let the player change their islands biome to     
                                                       |                             | DEEP_OCEAN                                       
                                                       | usb.biome.desert            | Let the player change their islands biome to     
                                                       |                             | DESERT                                           
                                                       | usb.biome.extreme_hills     | Let the player change their islands biome to     
                                                       |                             | EXTREME_HILLS                                    
                                                       | usb.biome.flower_forest     | Let the player change their islands biome to     
                                                       |                             | FLOWER_FOREST                                    
                                                       | usb.biome.forest            | Let the player change their islands biome to     
                                                       |                             | FOREST                                           
                                                       | usb.biome.hell              | Let the player change their islands biome to HELL
                                                       | usb.biome.jungle            | Let the player change their islands biome to     
                                                       |                             | JUNGLE                                           
                                                       | usb.biome.mushroom          | Let the player change their islands biome to     
                                                       |                             | MUSHROOM                                         
                                                       | usb.biome.ocean             | Let the player change their islands biome to     
                                                       |                             | OCEAN                                            
                                                       | usb.biome.plains            | Let the player change their islands biome to     
                                                       |                             | PLAINS                                           
                                                       | usb.biome.sky               | Let the player change their islands biome to SKY 
                                                       | usb.biome.swampland         | Let the player change their islands biome to     
                                                       |                             | SWAMPLAND                                        
                                                       | usb.biome.taiga             | Let the player change their islands biome to     
                                                       |                             | TAIGA                                            
                                                       | usb.exempt.cooldown.biome   | exempt player from biome-cooldown                
/is create|c [schematic]                               | usb.island.create           | create an island                                 
                                                       | usb.exempt.cooldown.create  | exempt player from create-cooldown               
/is home|h                                             | usb.island.home             | teleport to the island home                      
/is info [island]                                      | usb.island.info             | check your or another's island info              
                                                       | usb.island.info.other       | allows user to see others island info            
/is invite <oplayer>                                   | usb.party.invite            | invite a player to your island                   
/is kick|remove <player>                               | usb.party.kick              | remove a member from your island.                
/is leave                                              | usb.party.leave             | leave your party                                 
/is level [island]                                     | usb.island.level            | check your or anothers island level              
                                                       | usb.island.level.other      | allows user to query for others levels           
/is limits <player>                                    | usb.island.limit            | show the islands limits                          
/is lock|unlock                                        | usb.island.lock             | lock your island to non-party members.           
/is log|l                                              | usb.island.log              | display log                                      
/is makeleader|transfer <member>                       | usb.island.makeleader       | transfer leadership to another member            
/is party                                              |                             | show party information                           
/is party info                                         | usb.party.info              | shows information about your party               
/is party invites                                      | usb.party.invites           | show pending invites                             
/is party uninvite <player>                            | usb.party.uninvite          | withdraw an invite                               
/is perm <member> [perm]                               | usb.island.perm             | changes a members island-permissions             
/is restart|reset [schematic]                          | usb.island.restart          | delete your island and start a new one.          
                                                       | usb.exempt.cooldown.restart | exempt player from restart-cooldown              
/is sethome|tpset                                      | usb.island.sethome          | set the island-home                              
/is setwarp|warpset                                    | usb.island.setwarp          | set your island's warp location                  
/is spawn                                              | usb.island.spawn            | teleports you to the skyblock spawn              
/is togglewarp|tw                                      | usb.island.togglewarp       | enable/disable warping to your island.           
/is top [page]                                         | usb.island.top              | display the top10 of islands                     
                                                       | usb.admin.topten            | enables user to all-ways generate top-ten (no    
                                                       |                             | caching)                                         
/is trust|untrust [player]                             | usb.island.trust            | trust/untrust a player to help on your island.   
/is warp|w <island>                                    | usb.island.warp             | warp to another player's island                  
-------------------------------------------------------+-----------------------------+--------------------------------------------------
/islandtalk|istalk|it [message]                        | usb.island.talk             | talk to players on your island                   
-------------------------------------------------------+-----------------------------+--------------------------------------------------
/partytalk|ptalk|ptk [message]                         | usb.party.talk              | talk to your island party                        
-------------------------------------------------------+-----------------------------+--------------------------------------------------
/usb                                                   |                             | Ultimate SkyBlock Admin                          
/usb challenge|ch <player>                             | usb.mod.challenges          | Manage challenges for a player                   
/usb ch <player> complete <challenge>                  |                             | completes the challenge for the player           
/usb ch <player> rank <rank>                           |                             | complete all challenges in the rank              
/usb ch <player> reset <challenge>                     |                             | resets the challenge for the player              
/usb ch <player> resetall                              |                             | resets all challenges for the player             
/usb chunk                                             | usb.admin.chunk             | various chunk commands                           
/usb chunk load [x] [z] [r]                            |                             | load current chunk                               
/usb chunk regen [x] [z] [r]                           |                             | regenerate current chunk                         
/usb chunk unload [x] [z] [r]                          |                             | unload current chunk                             
/usb config|c [config]                                 | usb.admin.config            | open GUI for config                              
/usb c [config] search                                 |                             | searches config for a specific key               
/usb cooldown|cd                                       | usb.admin.cooldown          | Controls player-cooldowns                        
/usb cd clear|c <player> <command>                     |                             | clears the cooldown on a command (* = all)       
/usb cd list|l [player]                                |                             | lists all the active cooldowns                   
/usb cd restart|r <player>                             |                             | restarts the cooldown on the command             
/usb debug                                             | usb.admin.debug             | control debugging                                
/usb debug enable|disable                              |                             | toggle debug-logging                             
/usb debug flush                                       |                             | flush current content of the logger to file.     
/usb debug setlevel <level>                            |                             | set debug-level                                  
/usb doc [format] [arg]                                | usb.admin.doc               | saves documentation of the commands to a file    
/usb fix-flatland [player]                             | usb.admin.remove            | tries to fix the the area of flatland.           
/usb flush                                             | usb.admin.cache             | flushes all caches to files                      
/usb goto <player>                                     | usb.mod.goto                | teleport to another players island               
/usb import <format>                                   | usb.admin.import            | imports players and islands from other formats   
/usb info <player>                                     | usb.admin.info              | show player-information                          
/usb island|is                                         | usb.admin.island            | manage islands                                   
/usb is addmember|add <player> [island]                | usb.admin.addmember         | adds the player to the island                    
/usb is delete [leader]                                | usb.admin.delete            | delete the island (removes the blocks)           
/usb is get <player>                                   | usb.admin.get               | advanced command for getting island-data         
/usb is ignore <player>                                | usb.admin.ignore            | toggles the islands ignore status                
/usb is info <player>                                  | usb.admin.info              | print out info about the island                  
/usb is makeleader|transfer <leader> <oplayer>         | usb.admin.makeleader        | transfer leadership to another player            
/usb is protect <player>                               | usb.admin.protect           | protects the island                              
/usb is purge [leader]                                 | usb.admin.purge             | purges the island                                
/usb is register <player>                              | usb.admin.register          | set a player's island to your location           
/usb is remove <player>                                | usb.admin.remove            | removes the player from the island               
/usb is set <player>                                   | usb.admin.set               | advanced command for setting island-data         
/usb is setbiome [leader] <biome>                      | usb.admin.setbiome          | sets the biome of the island                     
/usb jobs|j                                            | usb.admin.jobs              | controls async jobs                              
/usb j stats|s                                         | usb.admin.jobs.stats        | show statistics                                  
/usb lang|l <language>                                 | usb.admin.lang              | changes the language of the plugin, and reloads  
/usb maintenance <true|false>                          | usb.admin.maintenance       | toggles maintenance mode                         
/usb nbt                                               | usb.admin.nbt               | advanced info about NBT stuff                    
/usb nbt add|a <nbttag>                                |                             | adds the NBTTag on the currently held item       
/usb nbt info|i                                        |                             | shows the NBTTag for the currently held item     
/usb nbt set|s <nbttag>                                |                             | sets the NBTTag on the currently held item       
/usb orphan                                            | usb.admin.orphan            | manage orphans                                   
/usb orphan clear                                      |                             | clear orphans                                    
/usb orphan count                                      |                             | count orphans                                    
/usb orphan list                                       | ?page                       | list orphans                                     
/usb perk                                              | usb.admin.perk              | shows perk-information                           
                                                       | group.memberplus            | additional perks rewBonus:0.05                   
                                                       | usb.donor.100               | additional perks rewBonus:0.5                    
                                                       | usb.donor.25                | additional perks rewBonus:0.15                   
                                                       | usb.donor.50                | additional perks rewBonus:0.2                    
                                                       | usb.donor.75                | additional perks rewBonus:0.3                    
                                                       | usb.donor.all               | additional perks rewBonus:0.1                    
                                                       | usb.donorbonus              | additional perks extraItems:[Bow, 32x Arrow,     
                                                       |                             | Stone Sword]                                     
                                                       | usb.extra.hunger            | additional perks hungerReduction:0.25            
                                                       | usb.extra.hunger2           | additional perks hungerReduction:0.5             
                                                       | usb.extra.hunger3           | additional perks hungerReduction:0.75            
                                                       | usb.extra.hunger4           | additional perks hungerReduction:1.0             
                                                       | usb.extra.partysize         | additional perks maxPartySize:8                  
                                                       | usb.extra.partysize1        | additional perks maxPartySize:5                  
                                                       | usb.extra.partysize2        | additional perks maxPartySize:6                  
                                                       | usb.extra.partysize3        | additional perks maxPartySize:7                  
                                                       | usb.extremebonus            | additional perks extraItems:[8x Bone, 4x Coal]   
                                                       | usb.giantbonus              | additional perks extraItems:[Dead Shrub,         
                                                       |                             | Mycelium]                                        
                                                       | usb.largebonus              | additional perks extraItems:[5x Dirt, 5x Sand]   
                                                       | usb.mediumbonus             | additional perks extraItems:[16x Torch, Lava     
                                                       |                             | Bucket]                                          
                                                       | usb.schematic.default       | additional perks schematics:[default]            
                                                       | usb.smallbonus              | additional perks extraItems:[16x Cobblestone, 5x 
                                                       |                             | Cooked Porkchop]                                 
/usb perk list                                         |                             | lists all perks                                  
/usb perk player <player>                              |                             | shows a specific players perks                   
/usb protectall                                        | usb.admin.protectall        | protects all islands (time consuming)            
/usb purge <time-in-days|stop|confirm> [level] [force] | usb.admin.purge             | purges all abandoned islands                     
/usb region|rg                                         | usb.admin.region            | region manipulations                             
/usb rg border                                         |                             | shows the non-chunk-aligned borders              
/usb rg chunk                                          |                             | shows the borders of the current chunk           
/usb rg hide                                           |                             | hides the regions again                          
/usb rg inner                                          |                             | shows the borders of the inner-chunks            
/usb rg outer                                          |                             | shows the borders of the outer-chunks            
/usb rg refresh                                        |                             | refreshes the existing animations                
/usb rg show                                           |                             | shows the borders of the current island          
/usb rg tick <integer>                                 |                             | set the ticks between animations                 
/usb reload                                            | usb.admin.reload            | reload configuration from file.                  
/usb topten                                            | usb.mod.topten              | manually update the top 10 list                  
/usb version|v                                         | usb.admin.version           | displays version information                     
/usb wg                                                | usb.admin.wg                | various WorldGuard utilities                     
/usb wg chunk                                          |                             | refreshes the chunk around the player            
/usb wg load                                           |                             | load the region chunks                           
/usb wg refresh                                        |                             | refreshes the chunks around the player           
/usb wg unload                                         |                             | load the region chunks                           
/usb wg update                                         |                             | update the WG regions                            
```