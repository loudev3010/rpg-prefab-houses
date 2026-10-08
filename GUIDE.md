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
3. A ghost shows where the house will go: green means it fits, red means it doesn't, and the screen says why.
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

Save designs you like under **Presets**. They work in every world.

Some options worth knowing:

- **Form:** Classic, Off-centre (door and stairs to one side), or Cottage.
- **Landscape:** Natural sets the house on a grassy mound with a winding path, flowers and trees.
- **Underground style:** turns the basement into a timber cellar, dwarven hall, crypt, grotto or arcane vault.
- **Overgrowth, roof trim, wall details, garden props:** extra character for the outside.

## What every house has

- An enchanting room with a full vanilla setup.
- A storage room, mostly empty so you can fill it with your own storage.
- A deep mine: a lit staircase down to the deepslate, ending in a chamber with chests. The chests hold the
  blocks the mine dug out, nothing more.

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
- `deepMines`, `mineBottomY`, `recovery`: the mine and what its chests hold.

Modpacks can put their own settings in the `defaultconfigs` folder.
