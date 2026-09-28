# WowVision Surroundings

Map data for the surroundings of [WowVision](https://github.com/wow-vision/WowVision) on
WoW: Forever. With it, WowVision describes where you walk: the land, roads and streets, city
squares, rooms of buildings, drop edges, entrances and what you bump into. Without it the
surroundings stay silent. What is said and how to use it: WowVision's documentation,
"Surroundings (WoW: Forever)".

Covered so far: Elwynn Forest with Stormwind, Dun Morogh with Ironforge, Tirisfal Glades with
Undercity. Place and building names are in English, German and French.

## Installing

1. Install WowVision first. This addon depends on it and does nothing on its own.
2. Download `WowVision_Surroundings.zip` from the latest release on the releases page and
   extract it into the WoW: Forever client's addons folder, so the files sit at
   `World of Warcraft\_classic_beta_\Interface\AddOns\WowVision_Surroundings`.
3. Log in. WowVision picks the data up by itself; `/wv surr` says whether it is loaded.

Or clone this repository into that addons folder under the name `WowVision_Surroundings`.

## Layout

- `WowVision_Surroundings.toc` declares the addon and its dependency on WowVision.
- `main.lua` collects the zones for WowVision.
- `zones/` holds one generated file per zone. WowVision unpacks a zone only while the player is
  in it. The format is described in WowVision's developer documentation, "Surroundings
  (WoW: Forever)".

The zone files are generated. Edit them through the generator, not by hand.

## Sources

The data is generated offline from the WoW: Forever client's own map files (terrain, buildings
and their rooms and doorways, water, objects), its database tables (AreaTable, WMOAreaTable,
with Classic Era's for the originals of rebuilt places) and the community listfile for model
names. Shop sign names and their German and French forms come from the cMaNGOS classic-db and
AzerothCore databases.
