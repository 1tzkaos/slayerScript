<h1 align="center">Hypixel Skyblock Slayer Script 👋</h1>
 
 
## Table of Contents
- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [Questions](#questions) 
- [License](#license)
 
# Description
This script uses Entity Iterator paired with baritone to find mobs, pathfind, and kill them. The script requires MVP+.
# Installation
💾 
Download and unzip the folder, place the 'macros' folder into an instance.

I will make these files (requested by Iceshades)
- add to "onBetterChat"

```$${ifcontains(%CHATCLEAN%,"[OPEN MENU]");   strip(&chat_json,"%CHATJSON%");   regexreplace(&chat_json,"\"","'");           match("%&chat_json%","'action':'run_command'\W'value':'(/cb [a-z0-9-]+)'",&match,1);   log("&7The following &emaddox-code &7has been matched out of the &eJSON-string&7: &d%&match%");   echo("%&match%");endif;}$$```

- add to "onChat" 

```$${ifcontains(%CHATCLEAN%,"SLAYER QUEST FAILED!");exec("restart.txt","restart");endif;ifcontains(%CHATCLEAN%,"NICE! SLAYER BOSS SLAIN!");log("&8[&7&ka&2Server&7&ka&8] &7Boss Slain!");exec("bossslain.txt","Slain");endif;ifcontains(%CHATCLEAN%,"You are AFK. Move around to return from AFK.");log("&8[&7&ka&2Server&7&ka&8] &7You are AFK!");wait(5);look(0,50,0.2);key(attack);wait(1);endif;match("%CHATCLEAN%","\+(\d+)\s\w+\s\((\d+)\,(\d+)\.?\d?\/(\d+)\,(\d+)\)",{@#xp_per_kill,@#current_level_xp,@#current_level_xp_decimals,@#total_to_next_level,@#total_to_next_level_decimals});setlabel(LABEL 259,"&7XP per kill: &d%@#xp_per_kill%\n&7Current XP: &d%@#current_level_xp%,%@#current_level_xp_decimals%\n&7Total XP for next level: &d%@#total_to_next_level%,%@#total_to_next_level_decimals%00");}$$```

# Usage
💻  

- Have Swrod in 1st slot, and Madox Box in 3rd slot

Change variables in 'SLAYERSTART.txt' to your desired settings.
## Settings

3 Different slayer modes: 
- 0 = No slayers, just xp (Crypt Ghouls) **WORK IN PROGRESS**
- 1 = Revenent Horrors (best xp)
- 2 = Svens **WORK IN PROGRESS**

4 Different Slayer Levels
- 1 = Level 1
- 2 = Level 2 
- 3 = Level 3
- 4 = Level 4

Webhook

![image](https://cdn.discordapp.com/attachments/784920430946287627/807032252798074890/webhookimage.PNG)

# Contributing
Iceshades#2451 | Helped with regular expressions as well as webhooks. Also helped with a lot of other problems I was facing.

JTReddin#8648 | Moral Support :)

# Questions

Requirements: MVP+ rank (VIP coming soon)
- Why does the script REQUIRE MVP+ or VIP:

The Script requires MVP+ ATM and VIP in the future due to a key feature only available to ranked members. The script uses priate hub lobbies for the lowest possible ditection rate. The script is not Watch Dog detected, so the only way of gettign banned is either by player or staff ie. Player sees you and reports you. Therefore private lobbies are used to lower the risk. The script also needs MVP+ for fastest transprtation as MVP+ has permission to use scrolls to Castle and Crypt Cave.

# License

- **NOT FOR COMMERCIAL USE**
