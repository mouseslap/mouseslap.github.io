# SUBTICK PAGE FOR BINDS / ALIASES
**If you are in this page, you should not have any desubtick binds in your autoexec.cfg file.**
## Content:  
[Alias of W](#alias-of-w)  
[Crouch jump bind](#crouch-jump-bind)  
[W release bind with key](#w-release-bind-with-key)  
[W release bind with mouse wheel](#w-release-bind-with-mouse-wheel)  
[Null](#null)  
[Low jump bind](#low-jump-bind)  
[Jump bug bind](#jump-bug-bind)  
[Remove immobility and input errors bind](#remove-immobility-and-input-errors-bind)  
[Turn bind](#turn-bind)  
[Spam CP Bind](#spam-cp-bind)

## Alias of W
Many advanced cs2 binds (jump bug bind, w-release bind) require a change in bind and alias of w, so the latest bind/alias will cover the orginal bind/alias of w, which makes the alias very chaotic. To prevent the case happening, a consistent alias of w is recommanded. The following binds in this doc will keep using the alias of +w/-w, and if there are any additions to commands in the following binds relevant with the alias of w, just add command directly in the alias of w, instead of realiasing the entire thing. 

**I recommand to copy the bind below into your autoexec.cfg file.**

For example:  
When I say: Add `bind mwheelup tick1` in `+w`, you need to change alias of +w from `alias +w "+forward;alias checkw _checkw"` to `alias +w "+forward;alias checkw _checkw;bind mwheelup tick1"`, which is only adding `;bind mwheelup tick1` without deleting anything from its initial alias.

Note: Remember to add semicolons between each command within an alias.

(The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)
```
alias _checkw "-forward;alias checkw"
alias +w "+forward;alias checkw _checkw"
alias -w "checkw"
```
## Crouch jump bind
This bind gives you a perfect crouch jump (which gives you more height) on pressing a single key. Binding long jumps is what is referred to as “binding” in VNL.

Note: The bind doesn't include the function of w-release, the w-release version will be shown in the following binds.
```
alias +lj "+duck;+jump"
alias -lj "-duck;-jump"
bind <key> +lj
```
## W release bind with key
This bind gives you a perfect timing of w-release in every jump, this feature can be used in both CJ and normal jump. 

**The w-release function needs the alias of w to activate.** (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

(The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)

**CJ with w-release**
```
alias +cj "+jump;+duck;checkw"
alias -cj "-jump;-duck"
bind <key> +cj
```
**Normal jump with w-release**
```
alias +lj "+jump;checkw"
alias -lj "-jump"
bind <key> +lj
```
## W release bind with mouse wheel
This bind gives you a perfect timing of w-release in every jump, this feature can be used in both CJ and normal jump. The binds below use mwheelup as an example, change it to mwheeldown if you use mwheelup to jump. 

**The w-release function needs the alias of w to activate.** (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**CJ with w-release**
```
alias tick1 "+jump;-jump;+duck;checkw;bind mwheelup tick2"
alias tick2 "-duck"
bind mwheelup +tick1
```
> Add `bind mwwheelup tick1` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Normal jump with w-release**
```
alias tick1 "+jump;-jump;checkw"
bind mwheelup tick1
```
## Null
Null is an alias bind that makes you can't press A and D at the same time. It will provide you a consistent 0 overlap in movement, you can't complete advanced jumpstats technique such as **onekey** without using it. 

(The following binds are made by ss, shoutout to ss for permission of the bind)
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
Low jump also known as the minijump, 48 height jump or 1 tick bind, this bind allows you to consistently get 48 height jumps. For some reasons, the bind will eventually make the jump desubticked, but the doc will still provide both desubtick and subtick format of lowjump binds.

**The w-release function needs the alias of w to activate.** (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

(The following binds are made by gliptal, shoutout to Gliptal for permission of the bind)

**Low jump (no w-release)**
```
alias +mj "+jump;+duck;-jump;-jump;-duck;-duck"
alias -mj ""
bind <key> +mj
```
**Low jump with w-release**
```
alias +mj "+jump;+duck;-jump;-jump;-duck;-duck;checkw"
alias -mj ""
bind <key> +mj
```
## Jump bug bind
Jump bug can give you maintained velocity and same height as CJ when you hit it. You need to jump, crouch at the air and release the crouch with a specific timing when you land, it can be done by both manually and bind. But because of the effect of subtick, manual jb seems to be more inconsistent and difficult in cs2. The doc will provide jb bind the format of key and mouse wheel.

**The some jump bug bind needs specfic change in the alias of w to activate.** (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

**Jump bug bind with key**
```
alias +jb "-duck;+jump"
alias -jb "-jump"
bind <key> "+jb"
```
> To use this bind, you need to manually press crouch at the air in any time, and press the key of +jb when the moment you feel you have landed.

**Jump bug bind with mouse wheel 1**
```
alias tick1 "+duck;bind mwheelup tick2"
alias tick2 "-duck;+jump;-jump"
bind mwheelup "tick1"
```
> Add `bind mwwheelup tick1` in `+w` (check [Alias of W](#alias-of-w) if you don't understand what does it mean)

> To use this bind, you don't need to manually press crouch at the air in any time, just scroll the mouse wheel when the moment you feel you have landed, it will automatically crouch for a tick and release your crouch and try to jump. However, after using it for once, you need to press w to reset it. The bind above uses mwheelup as an example, change it to mwheeldown if you use mwheelup to jump.

**Jump bug bind with mouse wheel 2**
```
alias tick1 "-duck;+jump;-jump"
bind mwheelup "tick1"
```
> To use this bind, you need to manually press crouch at the air in any time, and scroll the mouse wheel when the moment you feel you have landed, it will automatically release your crouch and try to jump. The bind above uses mwheelup as an example, change it to mwheeldown if you use mwheelup to jump.

## Remove immobility and input errors bind
The input rule in cs2 is more strict than csgo. If the input of + in a same command exceeds 1, it will be accumulated and you can't do anything until you input amount of - that greater than its +. The bind is used to resolve the situation stuck in map-running, press the key will input 10x of - for regular movement binds.
```
bind <key> "-jump;-jump;-jump;-jump;-jump;-duck;-duck;-duck;-duck;-duck;-left;-left;-left;-left;-left;-right;-right;-right;-right;-right;-forward;-forward;-forward;-forward;-forward;-back;-back;-back;-back;-back"
```
## Turn bind
This bind can automatically turn your camera left or right with a specfic angular velocity, not really useful in map-running, might be used in some specfic cases.
```
bind <key> "+turnleft"
bind <key> "+turnright"
bind <key> "+turnup"
bind <key> "+turndown"
```

## Spam CP Bind
This bind can allow you to set significant amount of checkpoints in a short time. Normally used in cp'ing in bhop sections or edging. The binds below use mwheelup as an example, change it to mwheeldown if you use mwheelup to jump. 
```
alias tick1 "kz_checkpoint"
bind mwheelup tick1
```