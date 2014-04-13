Here are some primitive scripts that I use to play Edgeworld semi-automatically. These bash scripts are meant to work under Linux and require [xdotool](http://www.semicomplete.com/projects/xdotool/xdotool.xhtml). No Windows version will be made in any foreseeable future.

It is highly unlikely that these scripts will work for anyone just out-of-the-box without any customizations. Everything here depends on:
* Base layout (positions of certain buildings in HQ and A-1),
* Browser type and configuration (window size, font sizes, presence of toolbars, ...),
* Window setting (sizes of decorations, fonts on title bar, ...),
* Screen resolution (in my case it's 1920x1080).

Included tools:
* [Unpack](./Unpack): Open the shop, point at "Use" button of a troop bundle and call `Unpack number_of_items_to_unpack number_of_scrolldowns`.
* [Unpack_NoLevelUp](./Unpack_NoLevelUp): Like `Unpack` but changed for unpacking Core bundles and Nano Cannisters.
* [PlayZoot](./PlayZoot): Open Zoot Ticket and call `PlayZoot [number_of_tickets_to_use]`. Default for `number_of_tickets_to_use` is 100.
* [Craft](./Craft): To craft Tier 1 Rare Part Boxes from Rare Parts call `Craft [number_of_boxes_to_craft]`. Default for `number_of_boxes_to_craft` is 10.
* [SimpleSim](./SimpleSim): Perform a simple sequence of simulations. Open desired simulation and call `SimpleSim [number_of_cycles] [type_of_cycle]`. Default `number_of_cycles` is 1000, default `type_of_cycle` is `S_15`. Types of cycles are:
 * `S_1` for one simulation without boosters,
 * `S_2` for one simulation with Defense Sim XP x2,
 * `S_15` for one simulation with Defense Sim XP x15,
 * `S_30` for one simulation with Defense Sim XP x30,
 * `L_2` for sequence of simulations with Defense Sim XP x2,
 * `L_15` for sequence of simulations with one Defense Sim XP x15,
 * `L_30` for sequence of simulations with one Defense Sim XP x30.
* [Autoplayer](./Autoplayer): This is the main script used to farm XP from defense simulations from A-1. It performs many tasks: Calls non-trivial sequence of [SimpleSim](./SimpleSim), tries to upgrade certain parts, collects resources, tries to upgrade map bases. Call `Autoplayer [number_of_cycles]`. Default `number_of_cycles` is 100.
* [Mouse2Cmd](./Mouse2Cmd): Just prints a command thet moves cursor to the current position and does an LMB click.
* [DecryptBoxes](./DecryptBoxes): Open an Encrypted Box, then call `DecryptBoxes number_of_remaining_boxes_to_decrypt`. May occasionally skip one turn due to irregulatities of the game.

To Do:
* Move layout-dependent coordinates to a kind of config file, so multiple scripts can use them (e.g. Engineering Lab position in [Craft](./Craft) and [Autoplayer](./Autoplayer)).
* Put some often-changing choices such as position of upgraded part or simulation scenario into a kind of config file.
* Convert parts of these scripts into true xdotool scripts and shorten sleeps where possible.
