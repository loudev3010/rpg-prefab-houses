# Changelog

## 1.4.0

**New**
- **Three new genres**, each with its own cottage: the **Gothic Manor** (tall stone ranges, steep roofs, a
  tower, pointed windows and buttresses), the **Dwarven Stone Hall** (a low stone hall dug into a rock face, with a
  carved portal, a forge and a dwarven underground) and the **Eastern Fantasy House** (a hall on a stone podium with
  wide curved roofs, courtyards at the bigger sizes, a lily pond with a bridge and a grotto underground). The rock
  face of the Dwarven hall can be switched off in the Customise screen.
- **Rooms in the basement**: a single-storey house keeps its big rooms in a cellar under the garden, so every genre
  builds at one floor. It is switched on for you when you choose 1 floor, and you can switch it off.
- **Every genre builds at its smallest size with one floor.** When the genre's own rooms do not all fit, the house
  leaves out the ones that do not and names each of them ("No space for the library at this size..."). If even its
  main rooms do not fit, the big rooms move to a cellar under the garden, and as a last resort the rooms get a size
  smaller; each of these says so. Rooms you tick yourself are never left out.
- Faster: houses generate about twice as fast, and placing a house costs the server much less each tick (each
  layer of a house now costs only its own blocks).

**Changes**
- **Windows keep solid wall between them and every door**, and every window sits in solid wall all round. An
  extension's new doorway walls up any window pane right beside it.

**Fixes**
- Designs that could not be built now build: the Massive single-storey fairy hut, narrow mountain keeps, shallow
  hillside burrows with big rooms, and desert oases without towers.
- Fixed rare crashes and flaws: overlapping longhouse annexes, floating flowers and lanterns, swamp water over a
  basement room, and steps or window sills you could climb onto but not off.

Because of the window change, **saved designs and design codes may build slightly different houses** than in
1.3: windows next to doors move along the wall or are left out. Saved presets show their "may look different" note.
Servers and clients must both run 1.4.0.

## 1.3.2

**New**
- New server setting `exemptOperators` (in the placement section). It's on by default, so nothing changes:
  operators, and the owner of a single-player world with cheats on, place houses for free like creative players.
  Modpacks that want everyone to play by the survival rules can turn it off: operators then pay the placement price
  and need the catalogue (and the hammer for extensions). Creative players always build for free.

## 1.3.1

**Fixes**
- The 3D preview now shows overlay and connected textures correctly in packs with texture mods (such as Continuity
  and Fusion). Before, parts of some blocks showed as black and white patches in the preview.

## 1.3.0

**New**
- **Size** in the Customise screen: Small, Medium, Large, Huge or Massive. Sizes are relative to the style, from
  the smallest footprint its rooms fit in up to 64 blocks on the long side, in the style's own proportions. Picking
  one sets the width and depth, and the sliders below still fine-tune it. Catalogue cards show each house's size.
- **1 to 5 floors for every style.** Where a style doesn't usually go that high or that low, it adapts: the fairy
  hut keeps to three floors and its towers get taller, the longhouse keeps its two-storey hall and raises its end
  bays, a tall hillside burrow sits inside a bigger hill, and the tower styles keep their towers above the house
  when it has fewer floors.
- The tiny cottage is now the **Small cottage**: choose Cottage, then Small. Surprise me rolls Small cottages and
  unusual floor counts now and then.

**Fixes**
- The Desert Oasis with corner towers never built at some sizes (34-38 and 42-44 blocks). It now builds at every
  size.

Saved designs and design codes build exactly the same houses as before.

## 1.2.1

**New**
- **Prices per house** for servers that set `placementCost`: the base price is now for a medium house and is
  multiplied by the house's size (`costBySize`: tiny 0.5x up to huge 2x), its genre (`costByGenre`, e.g.
  `wizard_tower=1.5`), a basement (`basementCostMultiplier`, 1.25x) and a deep mine (`mineCostMultiplier`, 1.25x).
  All of it is in the server config.
- The placement panel shows what a house will cost before you place it.

Houses are still free unless a server sets `placementCost`.

**Fixes**
- Every generated house is now checked for building flaws before you see it: holes in walls or roofs, single
  missing blocks, floating blocks, stairs you cannot walk and places you can get into but not back out of. A
  design with a flaw quietly tries its next variation instead.
- Tower stairs in some desert houses had the floor above in the way, so you could walk up but not back down.
- Little gaps beside cellar stairs that you could drop into and not climb out of are now filled.
- The mine shaft under houses on stilts is now walled in.
- Mountain Keep gatehouse turrets no longer have a hole in the middle of their tops.
- Hillside Burrow grass tufts now actually appear (they used a block name from a newer Minecraft version).

Designs saved with an older version may look slightly different when rebuilt.

## 1.2.0

**New**
- **Undo:** changed your mind? Click [Undo] in chat (or /prefabhouse undo) within 30 minutes and the house is
  taken away and the land put back exactly as it was, with anything you paid given back. Works while nothing of
  the house is broken and none of its chests used.
- **No more lag spikes:** houses are now built a little at a time, so even the biggest house and its deep mine
  no longer freeze a server for a second.
- **Optional price** for servers: `placementCost` in the server config, e.g. 16 emeralds per house (free by
  default).
- **Pressure plates: Inside only.** Doors still open by themselves for you, but mobs outside cannot open them.
- **Translations:** Chinese, Russian, Spanish, Brazilian Portuguese and German.

**Fixes**
- Every Tiny cottage now builds: rooms that do not fit are left out with a message naming them, instead of the
  design failing.
- Nothing blocks the way out of a door any more (window sills, flower boxes or a low eave above some doors).

Designs saved with an older version may look slightly different when rebuilt.

## 1.1.1

**New**
- Doors option in Customise: genre default, single or double doors throughout.
- Pressure plates option: a plate either side of every door, so doors open as you walk up and close behind you.
  On for new designs and for the signature houses (mobs can open these doors too, so switch it off if that matters).

**Fixes**
- Every staircase now ends level with the floor above. Before, the top step stopped a block short, so you had
  to jump off it.
- No more lanterns hanging over staircases where you bump your head climbing up (this could trap you in a
  basement).
- Basements no longer show dirt and grass in their ceilings: they have a proper ceiling of their own.
- The deep mine's staircase is lined all the way up, so no dirt shows in its walls or ceiling.

Designs saved with an older version may look slightly different when rebuilt.

## 1.1.0

- 14 genres, each with a full-size house and a cottage version (Houses / Cottages tabs in the catalogue).
- New genre: the Cosy Hillside Burrow, a home dug into a grassy mound.
- New Tiny cottage form: a little hut over a big cellar.
- Customise: form, landscape, overgrowth, roof trim, wall details, garden props and five underground hall styles.
- Lot blending: the lot meets the surrounding terrain smoothly.
- The catalogue loads about twice as fast and uses far less memory.
- Works with every Forge 1.20.1 build from 47.1.0.
