This repository contains config files to be used with the plugins [PugSetup](https://github.com/splewis/csgo-pug-setup)
and [Practice Mode](https://github.com/splewis/csgo-practice-mode). A few commands that permanently alter the server have
been disabled so that these configs can be used by larger organizations (see `addons/sourcemod/configs/pugsetup/permissions.cfg`).

GOTV will be enabled, which takes up one slot on the server, so you need at least 11 slots. Alternatively, you can set `tv_enable 0`
in `server.cfg`, but you won't be able to record demos then.

# Usage
	
Add admins following [these instructions](https://wiki.alliedmods.net/Adding_Admins_(SourceMod)). You need at least the `b` (basic admin) and the `g` (changelevel) flags to use the plugins. Also, `c` (kick) is recommended.

Demos will be recorded automatically in the `csgo/` directory - name format is: `{TIME}_{MAP}` .

Use `.setup` to get started ingame. Also check out the README-pages of both mods for more commands.

Most important commands:

* `.setup` sets up a match or activates Practice Mode
* `.map` changes the map (menu)
* `.kickbots` kicks all bots
* `.spec` makes the client join the spectators
* `.god` makes the client become invulnerable
* `.dryrun` executes a config to dryrun strats and setups

# Installation

1. Install [Metamod](https://metamodsource.net) following [these instructions](https://wiki.alliedmods.net/Installing_Metamod:Source).
1. Install [SourceMod](https://sourcemod.net) following [these instructions](https://wiki.alliedmods.net/Installing_SourceMod).
1. Install [PugSetup](https://github.com/splewis/csgo-pug-setup).
1. Move `pugsetup_damageprint.smx` and `pugsetup_teamnames.smx` from
`/addons/sourcemod/plugins/disabled` to the parent directory.
1. Install [Practice Mode](https://github.com/splewis/csgo-practice-mode).
1. Start the CSGO-server in order to create mod directories and files.
1. Download a release from the [releases](https://github.com/Linus4/csgo_config_plugins/releases) page and extract it in your `csgo/` directory..
1. Rename `server.cfg` to `nameofexecutable.cfg` and fix all FIXMEs in this file.
1. Install [Fix Warmup](https://github.com/Ilusion9/fix-warmup-csgo) (removes 1v1 arenas):
	1. Download `scripting/fix_warmup.sp` in the repository.
	1. Use this file in the [sourcemod web compiler](http://www.sourcemod.net/compiler.php) and compile.
	1. Put `.smx` plugin file from the compiler in `csgo/addons/sourcemod/plugins` on the server.
1. Add admins following [these instructions](https://wiki.alliedmods.net/Adding_Admins_(SourceMod)) for SourceMod.
1. Optionally change where demos will be stored in [this file](https://github.com/Linus4/csgo_config_plugins/blob/master/cfg/sourcemod/pugsetup/pugsetup.cfg) and create the corresponding directory in your `csgo` directory.

# Changes

## New Maps

Add new maps in `csgo_config_plugins/addons/sourcemod/configs/practicemode.cfg`, `csgo_config_plugins/addons/sourcemod/configs/adminmenu_maplist.ini` and `csgo_config_plugins/addons/sourcemod/configs/pugsetup/maps.txt`. Then reload map.
