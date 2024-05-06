# SUBTICK PAGE FOR BINDS / ALIASES
### **If you are in this page, you should have the desubtick binds in your autoexec.cfg file.**
### Content:
[Alias of W](#alias-of-w)  
[Crouch jump bind](#crouch-jump-bind)  
[W release bind with key](#w-release-bind-with-key)  
[Null](#null)  
[Low jump bind](#low-jump-bind)  
[Jump bug bind](#jump-bug-bind)  
[Remove immobility and input errors bind](#remove-immobility-and-input-errors-bind)  
[Turn bind](#turn-bind)


## Alias of W
Many advanced cs2 binds (jump bug bind, w release bind) require a change in bind and alias of w, so the latest bind/alias will cover the orginal bind/alias of w, which makes the alias very chaotic. To prevent the case happening, a consistent alias of w is recommanded. The following binds in this doc will keep using the alias of +w/-w, and if there are any additions to commands in the following binds relevant with the alias of w, just add command directly in the alias of w, instead of realiasing the entire thing.  

For example:  
When I say: Add `alias checkw _checkw` in `+w`, you need to change alias of +w from `alias +w "+forward_"` to `alias +w "+forward_; alias checkw _checkw"`, which is only adding `; alias checkw _checkw` without deleting anything from its initial alias.

Note: Remember to add semicolons between each command within an alias.

Note: Remember to delete `bind w +forward_` in the list of desubtick binds if you are using it, because `"bind w +forward_"` would change the bind of w, which covers `bind w +w` every time you launch the game.

```
alias +w "+forward_"
alias -w "checkw"
alias checkw "-forward_"
```
## Crouch jump bind
This bind gives you a perfect crouch jump (which gives you more height) on pressing a single key. Binding long jumps is what is referred to as “binding” in VNL.  
Note: The bind doesn't include the function of w-release, the w-release version will be shown in the following binds.
```
alias +lj "+duck_;+jump_"
alias -lj "-duck_;-jump_"
bind <key> +lj
```
## W release bind with key
This bind gives you a perfect timing of w-release in every jump, this feature can be used in both CJ and normal jump.

(The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)

**CJ w-release desubtick version**
```
alias _checkw "-forward_;alias checkw"
alias +lj "+jump_;+duck_;checkw"
alias -lj "-jump_;-duck_"
bind <key> +lj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Normal jump w-release desubtick version**
```
alias _checkw "-forward_;alias checkw"
alias +lj "+jump_;checkw"
alias -lj "-jump_"
bind <key> +lj
```
> Add `alias checkw _checkw` in `+w`(check [Alias of W](#alias-of-w) if you don't understand what does it mean)
## Null
Null is an alias bind that makes you can't press A and D at the same time. It will provide you a consistent 0 overlap in movement, you can't complete advanced jumpstats technique such as **onekey** without using it. 

Note: Remember to delete `bind a +left_` and `bind d +right_` in the list of desubtick binds if you are using it, because they would change the bind of a/d, which covers `bind a +fa` and `bind d +fd` from null every time you launch the game.

(The following binds are made by ss, shoutout to ss for permission of the bind)
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

## Low jump bind
Low jump also known as the minijump, 48 height jump or 1 tick bind, this bind allows you to consistently get 48 height jumps.

(The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)

**Low jump (no w-release)**
```
alias +mj "+jump_;+duck_;-jump_;-jump_;-duck_;-duck_"
alias -mj ""
bind <key> +mj
```
**Low jump with w-release**
```
alias _checkw "-forward_; alias checkw";
alias +mj "+jump_;+duck_;-jump_;-jump_;-duck_;-duck_;checkw"
alias -mj ""
bind <key> +mj
```
> Add `alias checkw _checkw` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)
## Jump bug bind
Jump bug can give you maintained velocity and same height as CJ when you hit it. You need to jump, crouch at the air and release the crouch with a specific timing when you land, it can be done by both manually and bind. But because of the effect of subtick, manual jb seems to be more inconsistent and difficult in cs2. The doc will provide jb bind the format of key and mouse wheel.

**Jump bug bind with key**
```
alias +jb "-duck_;+jump_"
alias -jb "-jump_"
bind <key> "+jb"
```
> To use this bind, you need to manually press crouch at the air in any time, and press the key of +jb when the moment you feel you have landed.

**Jump bug bind with mouse wheel 1**
```
alias tick1 "+duck_;bind mwheelup tick2"
alias tick2 "-duck_;+jump_;-jump_"
bind mwheelup "tick1"
```
> Add `bind mwwheelup tick1` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

> To use this bind, you don't need to manually press crouch at the air in any time, just scroll the mouse wheel when the moment you feel you have landed, it will automatically crouch for a tick and release your crouch and try to jump. The bind above uses mwheelup as an example, change it to mwheeldown if you use mwheelup to jump.

**Jump bug bind with mouse wheel 2**
```
alias tick1 "-duck_;+jump_;-jump_"
bind mwheelup "tick1"
```
> To use this bind, you need to manually press crouch at the air in any time, and scroll the mouse wheel when the moment you feel you have landed, it will automatically release your crouch and try to jump. The bind above uses mwheelup as an example, change it to mwheeldown if you use mwheelup to jump.

## Remove immobility and input errors bind
The input rule in cs2 is more strict than csgo. If the input of + in a same command exceeds 1, it will be accumulated and you can't do anything until you input amount of - that greater than its +. The bind is used to resolve the situation stuck in map-running, press the key will input 10x of - for regular movement binds.
```
bind <key> "-jump;-jump;-jump;-jump;-jump;-jump;-jump;-jump;-jump;-jump;-duck;-duck;-duck;-duck;-duck;-duck;-duck;-duck;-duck;-duck;-left;-left;-left;-left;-left;-left;-left;-left;-left;-left;-right;-right;-right;-right;-right;-right;-right;-right;-right;-right;-forward;-forward;-forward;-forward;-forward;-forward;-forward;-forward;-forward;-forward;-back;;-back;-back;-back;-back;-back;-back;-back;-back;-back"
```

## Turn bind
This bind can automatically turn your camera left or right with a specfic angular velocity, not really useful in map-running, might be used in some specfic cases.
```
bind <key> "+turnleft"
bind <key> "+turnright"
```