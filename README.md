Here are some primitive scripts that I use to play Edgeworld semi-automatically. These scripts are meant to work under Linux. No Windows version will be made in any foreseensble future.

It is highly unlikely that these scripts will work for anyone just out-of-the-box without any customizations. Everything here depends on:
* Base layout (position of certain building),
* Browser type and configuration (window size, font sizes, presence of toolbars, ...),
* Window setting (sizes of decorations and fonts on title bar),
* Screen resolution (in my case it's 1920x1080).

Included tools:
* [Unpack](../master/Unpack): Open the shop, point at "Use" button of a troop bundle and call `Unpack number_of_items_to_unpack number_of_scrolldowns`.
* [PlayZoot](../master/PlayZoot): Open Zoot Ticket and call `PlayZoot [number_of_tickets_to_use]`. Default for `number_of_tickets_to_use` is 100.
* [Craft](../master/Craft): To craft Tier 1 Rare Part Boxes from Rare Parts call `Craft [number_of_boxes_to_craft]`. Default for `number_of_boxes_to_craft` is 10.
* [SimpleSim](../master/SimpleSim): Perform a simple sequence of simulations. Open desired simulation and call `SimpleSim [number_of_cycles] [type_of_cycle]`. Default `number_of_cycles` is 1000, default `type_of_cycle` is `S_15`. Types of cycles are:
 * `S_1` for one simulation without boosters,
 * `S_2` for one simulation with Defense Sim XP x2,
 * `S_15` for one simulation with Defense Sim XP x15,
 * `S_30` for one simulation with Defense Sim XP x30,
 * `L_2` for sequence of simulations with Defense Sim XP x2,
 * `L_15` for sequence of simulations with one Defense Sim XP x15,
 * `L_30` for sequence of simulations with one Defense Sim XP x30.
