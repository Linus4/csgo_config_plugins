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

1. Install [Metamod](metamodsource.net) following [these instructions](https://wiki.alliedmods.net/Installing_Metamod:Source).
1. Install [SourceMod](sourcemod.net) following [these instructions](https://wiki.alliedmods.net/Installing_SourceMod).
1. Install [PugSetup](https://github.com/splewis/csgo-pug-setup).
1. Move `pugsetup_damageprint.smx`, `pugsetup_teamlocker.smx` and `pugsetup_teamnames.smx` from
`/addons/sourcemod/plugins/disabled` to the parent directory.
1. Install [Practice Mode](https://github.com/splewis/csgo-practice-mode).
1. Start the CSGO-server.
1. Download a release from the [releases](https://github.com/Linus4/csgo_config_plugins/releases) page and extract it in your `csgo/` directory.
1. Fill in the fields marked with `FIXME` in `server.cfg`.
1. Restart CSGO-server.
