# CS2 KZ BINDS / ALIASES

**Content:**  
[General info and disclaimer](#general-info-and-disclaimer)  
[How to use CFG](#how-to-use-cfg)  
[General kz commands](#general-kz-commands)  
[General de-subtick binds](#general-desubtick-binds)  

## General info and disclaimer

This website summarises all the known (or variation) or binds/aliases used in cs2 kz to stat or to map-running with a detailed instruction of how to use them. Some of them might be questionable, use it **AT YOUR OWN RISK**.

All of those are better if you create a .cfg file to exec them through your console. Note that all aliases will be gone once you restart your cs2. This can make some of your keys useless and you will need to re-bind them appropriately.

For any aliases/binds, copy and paste each line **ONE BY ONE** into your console. Replace <key> with your key (e.g bind <key> +lj becomes bind mouse1 +lj)

If you have anything and want to share, let me know (redmoon, discord - redmoontv)

You can acquire additional resources from GMC discord: [Global Map Coverage](https://discord.gg/xJXhMjHcGV) 

Shoutout to Gliptal, SS and others for letting me show their binds. Huge thanks to Exa for his assistance to construct this website and Redmoon for the promotion of this website.
## How to use CFG

Commands from a .cfg file can be exec through your console by typing exec <filename>. This is very useful for things like long jump binds which have multiple lines to be imputed in the console.

How to make one:  
Go to steam client > right click Counter-Strike 2 > manage (browse local files) > game > csgo > cfg.  
For exmaple: `D:\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg`  

In this folder, create a notepad and name it however you’d like with .cfg at the end (notice the dot).
From there, you can write any commands line by line.
## General kz commands

The kz menu is temporarily disabled in cs2 kz and unlikely to be available in any time soon, so you need to have those binds in cs2 in order to feature kz plugin in cs2, you can also type `kz_help` in console in a cs2 kz server, if you don't understand English, type `kz_language` to change the language to the one that you familiar with.

To use these commands, you can type:  
"bind <key> kz_<command name>" in your console, or type !<command name> or /<command name> in the chat.

For example: `bind 1 kz_cp` or `!cp` or `/cp`

**Main cs2 kz bind:**

`kz_vnl`: Switch to Vanilla mode.  
`kz_hidelegs`: Hide your legs in the first person.  
`kz_hide`: Hide other players.  
`kz_restart`: Restart.  
`kz_r`: Restart.  
`kz_hideweapon`: Hide weapon viewmodel.  
`kz_checkpoint`: Set a checkpoint on ground or on a ladder.  
`kz_cp`: Set a checkpoint on ground or on a ladder.  
`kz_teleport`: Teleport to the current checkpoint.  
`kz_tp`: Teleport to the current checkpoint.  
`kz_prevcp`: Teleport to the last checkpoint.  
`kz_nextcp`: Teleport to the next checkpoint.  
`kz_pcp`: Teleport to the last checkpoint.  
`kz_ncp`: Teleport to the next checkpoint.  
`kz_setstartpos`: Set your custom start position to your current position.  
`kz_ssp`: Set your custom start position to your current position.  
`kz_clearstartpos`: Clear your custom start position.  
`kz_csp`: Clear your custom start position.  
`kz_jsbroadcast`: Change jumpstats minimum threshold for broadcasting.  
`kz_jssound`: Change jumpstats minimum threshold for sound effects.  
`kz_togglestats`: Toggle jumpstats reporting.  
`kz_togglejs`: Toggle jumpstats reporting.  
`kz_jsalways`: Toggle the always-on jumpstats.  
`kz_stop`: Stop timer.  
`kz_pause`: Toggle timer pause.  
`kz_noclip`: Toggle noclip.  
`kz_nc`: Toggle noclip.  
`noclip`: Toggle noclip.  
`kz_panel`: Toggle centre panel display.  
`kz_language`: Switch current language.  
`kz_mode`: List or change mode.  
`kz_style`: List or change style.  
`kz_tips`: Toggle tips.  
`kz_ckz`: Switch to Classic mode.  
`kz_help`: Show this help message.  

The document will provide a preset templete of commands for cs2 kz map-running. But you can create your own cfg based on the explanation above.
```
bind 1 kz_cp
bind 2 kz_tp
bind 3 kz_prevcp
bind 4 kz_nextcp
bind 5 kz_pause
bind 6 kz_r
```
## General desubtick binds
Desubtick bind is an new feature for cs2, it can provide a better consistency in both height in jump and strafe, which cancel the effect of subtick. This doc will list out all the desubtick binds that can be potentially used in cs2, but only some of them are useful in kz (e.g. movements, jump, duck). You can copy all of them in your `autoexec.cfg` to automatically exec it when you launch cs2. 

**In the following binds/aliases except general server commands, the website will provide both subtick version and desubtick version in different pages, check the top right corner select the one you feel preferable.**  

Note: The binds below are set defaultly, you need to change to your binds if you have specific changes. For example: you might like to change `bind mwheeldown "jomp"` to `bind mwheelup "jomp"` due to your habit.  

(The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)
```
bind mouse1 +attack_
bind mouse2 +attack2_
bind space +jump_
bind mwheeldown "jomp"
bind ctrl +duck_
bind shift +sprint_
bind w +forward_
bind a +left_
bind s +back_
bind d +right_
bind v +runthrow

alias +attack_ "+attack;+attack"
alias -attack_ "-attack;-attack;-attack"
alias +attack2_ "+attack2;+attack2"
alias -attack2_ "-attack2;-attack2"

alias +jump_ "+jump;+jump"
alias -jump_ "-jump;-jump;-jump"
alias +duck_ "+duck;+duck"
alias -duck_ "-duck;-duck;-duck"
alias +sprint_ "+sprint;+sprint"
alias -sprint_ "-sprint;-sprint"

alias +forward_ "+forward;+forward"
alias -forward_ "-forward;-forward;-forward"
alias +left_ "+left;+left"
alias -left_ "-left;-left;-left"
alias +back_ "+back;+back"
alias -back_ "-back;-back;-back"
alias +right_ "+right;+right"
alias -right_ "-right;-right;-right"

alias jomp "+jump_;-jump_"
alias jumpthrow "jomp; -attack_; -attack2_"
alias +runthrow "+forward_; jumpthrow"
alias -runthrow "-forward_"
```
