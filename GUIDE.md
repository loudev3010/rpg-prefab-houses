# Guide

How to use RPG Prefab Houses. For a quick overview, see the [README](README.md).

## Styles

| Style | What it is |
|---|---|
| Medieval Stone & Timber Manor | Stone ground floor, timber upper floors, a vaulted magic room |
| Forest Ranger Lodge | Log lodge with a tall great hall and a fireplace |
| Mountain Adventurer's Keep | Gatehouse, walls and a keep built into a rock |
| Rustic Village Homestead | Farmhouse with a barn, fields and a well |
| Dark Fantasy Alchemist's Residence | Gothic tower house with an alchemy lab |
| Coastal Merchant Estate | Trader's house with a warehouse and a dock |
| Desert Nomad Oasis Residence | Sandstone courtyard house with domed towers |
| Swamp Witch's Crooked Manor | Mangrove manor on stilts with a leaning tower |
| Nordic Viking Longhouse | Long timber hall with a central hearth |
| Grand Fantasy Wizard's Tower | Arcane tower with side towers and an observatory |
| Ivy-Clad Storybook Manor | Mossy stone and plaster, covered in ivy |
| Rustic Timber Townhouse | Tall house with a row of steep front gables |
| Whimsical Fairy Hut | Stone cottage under a curled teal roof |
| Cosy Hillside Burrow | A home dug into a grassy hill |
| Elegant Gothic Manor | Tall stone ranges with steep roofs, a tower and buttresses |
| Dwarven Stone Hall | Low stone hall dug into a rock face, with a carved portal and a forge |
| Eastern Fantasy House | Hall on a stone base with wide curved roofs and a lily pond |
| Greek Villa | White villa on a stone podium with terracotta roofs, a portico, roof terraces and a court |
| Great Canopy Treehouse | Hollow trunks with stairs inside, cabins on boughs and bridges between the trees |
| Alpine Mountain Chalet | Broad gable front with deep eaves and a balcony on every upper floor |

The first five also have a hand-built signature house.

## Placing a house

1. Get the **Prefab House Catalogue** from the creative tab, with `/prefabhouse give`, or craft it:

   ```
   diamond     eye of ender  diamond
   gold block  book          gold block
   obsidian    map           obsidian
   ```

   It isn't used up when you place a house (servers can change that).
2. Right-click it, or press **K**. Pick a style, then press **Place**, **Customise** or **Surprise me**.
3. A ghost shows where the house will go: green means it fits, red means it doesn't, and the screen says why. If a nearby spot fits better, the ghost moves or turns the house there and says so.
   **R** rotates, **Shift + scroll** moves it up or down, left-click builds, right-click cancels.

The **Cottages** tab shows a smaller, cosier version of every style.

## Customising

Customise lets you change the size (Small to Massive), floors (1 to 5), rooms, basement, grounds, materials,
roof, doors and more. The preview updates as you go and can show the outside, a cutaway of each floor, a room
plan, or the mine.

If a house is too small for its style's rooms, it leaves out the ones that don't fit and names them; if even its
main rooms don't fit, its big rooms go in a cellar under the garden, and as a last resort the rooms get a size
smaller. A single-storey house keeps its big rooms in the basement (the **Rooms in the basement** option). Rooms
you add yourself are never left out: if they don't fit, the right panel tells you why, for example "remove 2
rooms". **Surprise me** only picks designs that build as asked.

Every size choice uses the same five sizes, **Small, Medium, Large, Huge and Massive**: the house, its room size,
basement, mine, grounds and Builder's Hammer extensions. Hover a size setting to see what the size you chose
measures. When one choice changes another (a Massive basement needs Large grounds), the screen tells you.

Save designs you like under **Presets**. They work in every world.

Some options worth knowing:

- **Form:** Classic, Offset (door and stairs to one side), Cottage, or Tiny.
- **Colour:** recolours the carpets, beds, banners and wool inside the house.
- **Landscape:** Natural sets the house on a grassy mound with a winding path, flowers and trees.
- **Terrain:** Terrain Adapted lays the house into the land around it; Flat Platform puts it on a level lot with
  the land blended to meet it.
- **Path Size:** Expanded (a wide main path, every path carried on to a nearby road) or Compact (the main path as
  wide as the front door, and only it carried a short way out).
- **Rooms:** every room has its own switch, and All On / All Off switches them all.
- **Underground:** On / Off. Off builds the house wholly above ground: no basement, no rooms in it, no mine. Always
  on for cottages, the Swamp Manor, the Hillside Burrow and the Treehouse.
- **Underground style:** turns the basement into a timber cellar, dwarven hall, crypt, grotto or arcane vault.
- **Overgrowth, roof trim, wall details, garden props:** extra character for the outside.
- **Mods > Tom's Simple Storage vault** (since 1.7.0; needs Tom's Simple Storage installed): fills the Storage Room
  with 20 connected chests, an Inventory Connector, a Storage Terminal and a Crafting Terminal. In survival they are
  part of the price. Undo is refused while the vault holds items.
- **Mods > Iron's Spells 'n Spellbooks** and **Mods > Forbidden & Arcanus: Hephaestus Forge** (since 1.8.0; each needs
  its mod installed, either or both): the Magic Room gains Iron's Spells' Inscription Table, Scroll Forge and Arcane
  Anvil, and/or a working Hephaestus Forge on its full darkstone floor. The Magic Room grows only as much as they need
  (at least 11 x 13, 11 x 17 or 11 x 19 with both). In survival their blocks are part of the price (the forge as a
  Smithing Table and Mundabitur Dust). Undo is refused while a station or the forge holds anything.
- **Placing them yourself** (since 1.9.0): in the **Rooms** view, click the vault, the forge or a station, move it with
  the arrow keys between the places where it fits (green dots), Shift-click a station to move all three, **R** to turn,
  **Delete** or **Reset to automatic** to put it back. The places are saved in the design. A place that no longer fits
  after a size or genre change turns red and the house can't be placed until you move or reset it.

## What every house has

- An enchanting room with a full vanilla setup (switch the Magic Room off in the rooms if you don't want it).
- A storage room, mostly empty so you can fill it with your own storage (it can be switched off, except in the
  Village Homestead and Coastal Estate, which are built around it).
- A deep mine: a lit staircase down to the deepslate, ending in a chamber with chests. The chests hold the
  blocks the mine dug out, nothing more. Switch the Mine off in the rooms for a house without one.

## Placement rules

- Houses won't overwrite chests, other containers or things you've built.
- Land claims (such as FTB Chunks) and spawn protection are respected.
- The ground around the house is smoothed into a gentle slope, so there are no dirt walls at the edge.
- Houses build a little at a time, so the server doesn't freeze.

## Undo

`/prefabhouse undo`, or the [Undo] link in chat, removes your last house and puts the land back. It works for
30 minutes, as long as nothing in the house has been broken and no chest in it used. Anything you paid is
given back.

## Builder's Hammer

Craft one to add wings and towers to a house you placed:

```
iron block  diamond  iron block
iron block  stick    iron block
            stick
```

Right-click your house, choose a room and a size, then press **Choose spot**. **R** cycles through the
places it fits, and left-click builds. A house can have up to 8 extensions.

**Mods** (since 1.9.0): puts the storage vault, the Hephaestus Forge or the Iron's Spells stations into a house you
already built, or moves them. The Hammer only builds on empty space (the forge's darkstone only on the room's own floor),
never over your blocks, and never makes a room bigger. Install costs what a new house would; moving is free and keeps
everything inside (chests, the Crafting Terminal's grid, the Scroll Forge, the forge's essences). A move is refused while
someone has one of its chests, terminals or stations open nearby, or while another inventory touches the vault. After
adding or moving one, the house can't be undone.

## Commands

```
/prefabhouse list
/prefabhouse undo
/prefabhouse give [targets]
/prefabhouse spawn <house> [facing] [force]
/prefabhouse generate <style> [seed] [width depth] [floors] [facing] [force]
/prefabhouse design <code> [facing] [force]
```

Everything except `list` and `undo` needs operator rights.

## Server settings

The settings are in `serverconfig/rpgprefabhouses-server.toml` inside the world folder. Each one is explained
in the file. The main ones:

- `requireCatalogue`, `consumeCatalogue`: whether placing a house needs the catalogue, and uses it up.
- `placementCost`: what survival players pay for a house, e.g. `["minecraft:emerald=16"]`. Empty means free.
  Bigger houses, basements and mines cost more; `costBySize` and `costByGenre` adjust this.
- `undoMinutes`: how long undo works (0 turns it off).
- `blendTerrain`: smooth the land around the house.
- `fitTerrain`: lay Varied houses into the land (level ground round the house, the garden following the slope, a path
  from the front door, only the trees in the way taken down). Off puts them on a level lot as before.
- `deepMines`, `mineBottomY`, `recovery`: the mine and what its chests hold.

Modpacks can put their own settings in the `defaultconfigs` folder.
