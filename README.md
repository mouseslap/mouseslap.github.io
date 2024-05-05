# CS2 KZ BINDS / ALIASES

**Content:**  
[General info and disclaimer](#general-info-and-disclaimer)  
[How to use CFG](#how-to-use-cfg)  
[General de-subtick binds](#general-desubtick-binds)  
[Alias of W](#alias-of-w)  
[Crouch jump bind](#crouch-jump-bind)  
[W release bind in keys](#w-release-bind-in-keys)  
[Null](#null)  
[Jump bug bind](#jump-bug-bind)

## General info and disclaimer

This document summarises all the known (or variation) or binds/aliases used in CS2 KZ to stat or to map run. Note that some of them may get you banned from some servers (not gbanned).
Some of them might be questionable. Use AT YOUR OWN RISK (from getting banned from servers, not gbanned).

All of those are better if you create a .cfg file to exec them through your console. Note that all aliases will be gone once you restart your CS2. This can make some of your keys useless and you will need to re-bind them appropriately.

For any aliases/binds, copy and paste EACH line ONE BY ONE into your console. Replace <key> with your key (e.g bind <key> +lj becomes bind mouse1 +lj)

If you have anything and want to share, let me know (redmoon, discord - redmoontv)

You can acquire additional resources from GMC discord: [Global Map Coverage](https://discord.gg/xJXhMjHcGV) 

Shoutout to Redmoon, Exa, Gliptal, and zer0.k for the help and others for letting me show their binds.
## How to use CFG

Commands from a .cfg file can be executed (exec) through your console by typing exec <filename>. This is very useful for things like long jump binds which have multiple lines to be imputed in the console.

How to make one:  
Go to steam client > right click Counter-Strike 2 > manage (browse local files) > game > csgo > cfg.
In this folder, create a notepad and name it however you’d like with .cfg at the end (notice the dot).
From there, you can write any commands line by line.
## General desubtick binds:

Desubtick binds are essential for cs2 kz, the usage of subtick bind can provide a better consistency in both height in jump and strafe. This doc will list out all the desubtick binds that can be potentially used in cs2, but only some of them are useful in kz (movement, jump, duck). You can put all of them in your autoexec.cfg to automatically exec it when you launch cs2. Note: The binds of key below are set defaultly, you need to change to your binds of key if you have specific changes in binds/aliases. (The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)
```
bind mouse1 +attack_
bind mouse2 +attack2_
bind space +jump_
bind mwheeldown "jomp"
bind mwheelup "jomp"
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
## General kz commands/binds

The KZ menu is temporarily disabled in cs2 kz, so you need to have binds of tp/cp in cs2 in order to feature them in cs2, you can also type kz_help in console in a cs2 kz server.

To use these commands, you can type:  
"bind <key> kz_<command name>" in your console, or type !<command name> or /<command name> in the chat.
For example: "bind 1 kz_cp" or "!cp" or "/cp"

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

## Alias of W
Many advanced cs2 binds (jump bug bind, w release bind) will require a change in bind and alias of w, so the latest bind/alias will cover the orginal bind/alias of w, which makes the alias very chaotic. To prevent the case happening, a consistent alias of w is recommanded. The following binds in this doc will keep using the alias of +w/-w, and if there are any additions to commands in the following binds about alias of w, just add command directly in the alias of w, instead of realiasing the entire thing.  

For example:  
When I say: Add `alias checkw _checkw` in `+w`, you need to change alias of +w from `alias +w "+forward_"` to `alias +w "+forward_; alias checkw _checkw"`, which is adding `; alias checkw _checkw` without deleting anything from its orginal alias.

Note: Remember to delete `bind w +forward_` in the list of desubtick binds if you are using it, because `"bind w +forward_"` would change the bind of w, which covers `bind w +w` every time you launch the game.

**Desubtick version**
```
alias +w "+forward_";
alias -w "checkw";
alias checkw "-forward_"
```
**Subtick version**
```
alias +w "+forward; alias checkw _checkw";
alias -w "checkw";
alias checkw "-forward"
```

## Crouch jump bind
This bind gives you a perfect crouch jump (which gives you more height) on pressing a single key. Binding long jumps is what is referred to as “binding” in VNL.  
Note: The bind doesn't include the function of w-release, the w-release version will be shown in the following binds.

**Desubtick version**
```
alias +lj "+duck_; +jump_";
alias -lj "-duck_; -jump_";
bind <key> +lj
```
**Subtick version**
```
alias +lj "+duck; +jump";
alias -lj "-duck; -jump";
bind <key> +lj
```
## W release bind in keys
This bind gives you a perfect timing of w-release in every jump, this feature can be used in both CJ and normal jump. (The following binds are made by gliptal and modified from its orginal bind, shoutout to Gliptal for permission of the bind)

**CJ w-release desubtick version**
```
alias _checkw "-forward_; alias checkw";
alias +lj "+jump_; +duck_; checkw";
alias -lj "-jump_; -duck_";
bind <key> +lj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**CJ w-release subtick version**
```
alias _checkw "-forward; alias checkw";
alias +lj "+jump; +duck; checkw";
alias -lj "-jump; -duck";
bind <key> +lj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Normal jump w-release desubtick version**
```
alias _checkw "-forward_; alias checkw";
alias +lj "+jump_; ; checkw";
alias -lj "-jump_";
bind <key> +lj
```
> Add `alias checkw _checkw` in `+w`(check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Normal jump w-release subtick version**
```
alias _checkw "-forward; alias checkw";
alias +lj "+jump; checkw";
alias -lj "-jump";
bind <key> +lj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)
## Null
Null is an alias bind that makes you can't press A and D at the same time. (The following binds are made by ss and modified from its orginal bind, shoutout to ss for permission of the bind)

Note: Remember to delete `bind a +left_` and `bind d +right_` in the list of desubtick binds if you are using it, because they would change the bind of a/d, which covers `bind a +fa` and `bind d +fd` from null every time you launch the game.

**Null desubtick version**
```
bind a +fa
bind d +fd

alias "+fa" "o_lh1"
alias "-fa" "lh1_o"
alias "+fd" "o_rh1"
alias "-fd" "rh1_o"

alias "o_lh1" "+left_;alias -fa lh1_o;alias +fd lh1_lh2"
alias "lh1_o" "-left_;alias +fd o_rh1;alias +fa o_lh1"

alias "o_rh1" "+right_;alias -fd rh1_o;alias +fa rh1_rh2"
alias "rh1_o" "-right_;alias +fa o_lh1;alias +fd o_rh1"

alias "lh1_lh2" "+right_;-left_;alias -fd lh2_lh1;alias -fa lh2_rh1"
alias "lh2_lh1" "-right_;+left_;alias -fa lh1_o;alias +fd lh1_lh2"

alias "rh1_rh2" "+left_;-right_;alias -fa rh2_rh1;alias -fd rh2_lh1"
alias "rh2_rh1" "-left_;+right_;alias -fd rh1_o;alias +fa rh1_rh2"

alias "rh2_lh1" "alias -fa lh1_o;alias +fd lh1_lh2"
alias "lh2_rh1" "alias -fd rh1_o;alias +fa rh1_rh2"
```
**Null subtick version**
```
bind a +fa
bind d +fd

alias "+fa" "o_lh1"
alias "-fa" "lh1_o"
alias "+fd" "o_rh1"
alias "-fd" "rh1_o"

alias "o_lh1" "+left;alias -fa lh1_o;alias +fd lh1_lh2"
alias "lh1_o" "-left;alias +fd o_rh1;alias +fa o_lh1"

alias "o_rh1" "+right;alias -fd rh1_o;alias +fa rh1_rh2"
alias "rh1_o" "-right;alias +fa o_lh1;alias +fd o_rh1"

alias "lh1_lh2" "+right;-left;alias -fd lh2_lh1;alias -fa lh2_rh1"
alias "lh2_lh1" "-right;+left;alias -fa lh1_o;alias +fd lh1_lh2"

alias "rh1_rh2" "+left;-right;alias -fa rh2_rh1;alias -fd rh2_lh1"
alias "rh2_rh1" "-left;+right;alias -fd rh1_o;alias +fa rh1_rh2"

alias "rh2_lh1" "alias -fa lh1_o;alias +fd lh1_lh2"
alias "lh2_rh1" "alias -fd rh1_o;alias +fa rh1_rh2"
```
## Low jump bind
Low jump also known as the minijump, 48 height jump or 1 tick bind, this bind allows you to consistently get 48 height jumps. For some reasons, the bind will eventually make the jump desubticked, but the doc will still provide both desubtick and subtick format of lowjump bind. (The following binds are made by gliptal and modified from its orginal bind, shoutout to Gliptal for permission and further explanation of the bind)

**Low jump desubtick version (no w-release)**
```
alias +mj "+jump_;+duck_;-jump_;-jump_;-duck_;-duck_"
alias -mj ""
bind <key> +mj
```
**Low jump subtick version (no w-release)**
```
alias +mj "+jump;+duck;-jump;-jump;-duck;-duck"
alias -mj ""
bind <key> +mj
```
**Low jump desubtick version with w-release**
```
alias _checkw "-forward_; alias checkw";
alias +mj "+jump_;+duck_;-jump_;-jump_;-duck_;-duck_;checkw"
alias -mj ""
bind <key> +mj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Low jump subtick version with w-release**
```
alias _checkw "-forward; alias checkw";
alias +mj "+jump;+duck;-jump;-jump;-duck;-duck;checkw"
alias -mj ""
bind <key> +mj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

## Jump bug bind
Jump bug can give you maintained velocity and same height as CJ when you hit it. You need to jump, crouch at the air and release the crouch with a specific timing when you land, it can be done by both manually and bind. But because of the effect of subtick, manual jb seems to be more inconsistent and difficult in cs2. The doc will provide jb bind the format of key and mouse wheel.

**Jump bug bind with key desubtick version**
```
alias +jb "-duck_;+jump_"
alias -jb "-jump_"
bind <key> "+jb"
```
**Jump bug bind with key subtick version**
```
alias +jb "-duck;+jump"
alias -jb "-jump"
bind <key> "+jb"
```
> To use this bind, you need to manually press crouch at the air in any time, and press the key of +jb when the moment you feel you have landed.

**Jump bug bind with mouse wheel desubtick version**
```
alias tick1 "+duck_;bind mwheelup tick2"
alias tick2 "-duck_;+jump_;-jump_"
bind mwheelup "tick1"
```
> Add `bind mwwheelup tick1` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Jump bug bind with mouse wheel subtick version**
```
alias tick1 "+duck_;bind mwheelup tick2"
alias tick2 "-duck_;+jump_;-jump_"
bind mwheelup "tick1"
```
> Add `bind mwwheelup tick1` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

> To use this bind, you don't need to manually press crouch at the air in any time, just scroll the mouse wheel when the moment you feel you have landed. The bind above uses mwheelup as an example, change it to mwheeldown if you use mwheelup to jump.

## Turn bind
This bind can automatically turn your camera left or right with a specfic angular velocity, not really useful in map-running, might be used in some specfic cases.
```
bind <key> "+turnleft";
bind <key> "+turnright"
```

