# RPG Prefab Houses: guide

Everything the mod can do, in detail. For a quick overview, see the [README](README.md).

## The styles

|---|-------|-----------------|-----------|
| 1 | Medieval Stone & Timber Manor | 46 × 42 | Stone ground floor, jettied timber upper floors, gables, vaulted magic room, storage vault |
| 2 | Forest Ranger Lodge | 44 × 42 | Log lodge, towering great hall with fireplace, glazed loft gable, rune cellar, ranger yard |
| 3 | Mountain Adventurer's Keep | 48 × 48 | Gatehouse and curtain wall, terraces, keep and magic tower, halls carved into a rock massif |
| 4 | Rustic Village Homestead | 54 × 46 | Farmhouse with dormers, brick kitchen wing, gambrel barn and hayloft, fields, pen, well |
| 5 | Dark Fantasy Alchemist's Residence | 40 × 36 (68 tall) | Gothic tower house with spire, alchemy lab, vast vaulted magic hall, hidden vault |
| 6 | Coastal Merchant Estate | generated | Stone and timber trader's house, harbour warehouse, merchant's office, lookout, dock |
| 7 | Desert Nomad Oasis Residence | generated | Sandstone courtyard house, arcade and fountain, domed corner towers, caravan yard, oasis |
| 8 | Swamp Witch's Crooked Manor | generated | Mangrove manor on stilts, crooked wing, leaning tower, potion and ritual rooms, boardwalks |
| 9 | Nordic Viking Longhouse | generated | Long timber hall under a sweeping roof, central hearth, feasting area, mead cellar, training yard |
| 10 | Grand Fantasy Wizard's Tower | generated | Great arcane tower, gate hall and ranges, side towers with bridges, observatory, ritual chamber |
| 11 | Ivy-Clad Storybook Manor | generated | Mossy stone and cream plaster, jettied timber floors, cross wings, spired turret, ivy everywhere |
| 12 | Rustic Timber Townhouse | generated | Tall cobblestone and spruce house, row of steep front gables, balcony over the door, kitchen wing |
| 13 | Whimsical Fairy Hut | generated | Pale stone cottage under a mossy teal bell roof with a curled tip, curling tower spires, red door |
| 14 | Cosy Hillside Burrow | generated | A home dug into a grassy mound: only the timber and mud-brick front shows, turf over the roof with chimneys poking through, most rooms in a big timber cellar |


## Playing

* Get the **Prefab House Catalogue**: creative tab *RPG Prefab Houses* (also in *Tools & Utilities*),
  `/prefabhouse give`, or craft it. It is deliberately expensive, a mid-to-late-game goal:

  ```
  diamond     eye of ender  diamond
  gold block  book          gold block
  obsidian    map           obsidian
  ```

  Diamonds, gold blocks and obsidian use Forge's common tags, so other mods' versions also work. Modpacks can
  change the recipe with a datapack or KubeJS (`rpgprefabhouses:prefab_catalogue`). The catalogue is
  reusable; set `consumeCatalogue = true` in the server config to use one up per house.
* Right-click it (or press **K**, rebindable under *Controls › RPG Prefab Houses*) to open the catalogue.
* Pick a style card (the list scrolls), drag to orbit and scroll to zoom the 3D preview, and press
  **Interior** to step through the cutaway levels. Use ↺ / ↻ to choose which way the front door faces.
* The **Houses / Cottages** tabs above the cards switch between each genre's full-size house and its
  cottage version: the same genre as a cosy *Cottage* form design on a natural lot, with roof trim, wall
  details, garden props and the genre's underground style. Switching tabs keeps the selected genre. A
  cottage card has the same Place, Customise and Surprise me buttons as a house card, and Surprise me rolls
  a random cottage. 
* Press **Place** for the signature house (or the style's default design), **Customise** (key **C**) to
  design your own, or **Surprise me** for a random house in that genre that builds.
* In placement mode a ghost follows your aim: green means valid, red means invalid, and the HUD says why.
  Press **R** to rotate, **Shift + scroll** to raise or lower, **left-click** to build, **right-click** to cancel.

### Customise

The left panel holds every setting:

| Setting | Range |
|---------|-------|
| Style | any of the fourteen |
| Form | Classic / Off-centre / Cottage (see *Exterior character*) |
| Size | Small / Medium / Large / Huge / Massive (see *Size and floors*) |
| Width, depth | fine-tune the size: 16-64 (each style has its own minimum; a Small cottage 17-20, larger cottages from 20 × 18) |
| Floors | 1-5, for every style |
| Room size | Compact / Spacious / Huge |
| Basement | None / Small / Medium / Large / Very Large (a cottage: Large or Very Large) |
| Underground style | Plain basement / Genre / Timber Undercroft / Dwarven Hall / Crypt / Lush Grotto / Arcane Vault |
| Mine | Standard / Large / Very Large |
| Grounds | None / Small / Medium / Large / Huge |
| Porch, balcony, tower | where the style allows them |
| Exterior features | the style's features, e.g. dock, oasis, graveyard, training yard |
| Rooms | core rooms plus the style's optional rooms. Entrance hall, storage, magic and mine are always included and never shrunk to a token size. |
| Landscape, overgrowth | Tidy / Natural; Genre default / None / Overgrown |
| Roof trim, wall details, garden props | on / off |
| Doors, pressure plates | Genre default / Single / Double; Off / Both sides / Inside only |
| Materials | wood, stone, roof and colour accent (with optional tinted windows); *Style default* keeps the style's own |

The preview updates by itself shortly after every change. Generation runs in the background, so the game
never stalls. The preview has four views: **Exterior**, **Interior** (cutaway by level), **Rooms** (a
labelled floor plan per storey; hover a room for its size) and **Mine** (the whole staircase and chamber).

The right panel shows the generator's verdict. When a design cannot be built it says why, for example
*"Not enough space for every room: increase the size or remove 2 room(s)"*. It also shows warnings, the
footprint, the lot size and a list of rooms by floor.

* **Generate** (G) builds now. **Regenerate** (R) keeps the settings but picks a new seed. **Surprise me**
  searches in the background for a random design in the current genre that actually builds. You can also
  type a seed.
* **Presets**: save, load, rename and delete designs. They are stored in
  `config/rpgprefabhouses-presets.json` as design codes, so they work in every world. Each preset remembers
  the generator version it was saved with. If a later version of the mod builds that design differently, the
  preset is marked with `*`, and loading it tells you to check the preview before placing.
* **Place** is only enabled for a design that has been generated successfully. The preview is built from
  the same blueprint that will be placed.

#### Size and floors

**Size** is relative to the genre. Each tier is a point between the genre's smallest workable footprint (Small:
the smallest where its core rooms build at its usual floors) and 64 blocks on its long side (Massive), in the genre's own proportions, so a Small fairy hut and a Small manor are
each clearly smaller than their own larger versions. Choosing a tier moves the width and depth sliders to that
tier's footprint; the sliders then fine-tune it, and the Size row shows the nearest tier. A cottage scales the
same way from the Small cottage. The catalogue cards show each design's tier.

**Floors** are 1-5 for every genre, whatever the size. Within a genre's usual range the house is built as it
always was; beyond it the extra floors go where the genre puts them:

* the fairy hut keeps to three floors under its bell roof and its towers rise with the rest (on a lot too
  narrow for towers, the hut takes every floor);
* the longhouse keeps its two-storey hall, and the end bays rise around it as lofts;
* a hillside burrow above two floors sits in a big hill that slopes down to the edge of the lot (it always
  has Huge grounds for that);
* the tower genres (wizard, alchemist, keep, swamp, storybook, townhouse) keep their towers taller than the
  house when it has fewer floors than usual, and its rooms may also go down into the basement;
* the others, all naturally tall house types, simply gain storeys, with rooms, stairs, balconies and roofs
  redistributed by the planner.

A footprint too small for the chosen rooms and floors says so ("remove 2 room(s)"), as before.

Design codes start with their version: codes made before the size tiers (`1-...`) keep their genre's old
floor range, so they build exactly the house they always did.

### Placement and the deep mine

Placement is validated on the client for feedback, and again on the server before anything changes. The
checks cover height limits, loaded chunks, terrain rise and drop, water and lava, containers and other block
entities, player-built blocks (tag `rpgprefabhouses:protected_builds`) and generated surface structures.
Natural terrain inside the footprint is cleared, and gaps under the house get a dirt/stone foundation.

Land claims and spawn protection are respected. For every chunk the house or its mine touches, the server
fires the standard Forge block-place event for the player; FTB Chunks and similar claim mods use it to
protect their land. If any chunk is protected, the placement is refused. Each player can only have one
generated design being prepared on the server at a time.

**Lot blending.** After placement, a ring of land around the lot (6 blocks by default) is reshaped into a gentle
slope, so the lot meets the terrain instead of ending in a dirt wall or a ledge. Land higher than the lot is cut
back, land lower than it is built up, and the result is smoothed and walkable (at most one block per step).
The blending:

* never needs to know biomes, so modded terrain works: each column keeps its own surface block (vanilla or
  modded grass, sand, snow) over the block that was under it, and loose plants or snow go back on top;
* only reshapes natural ground (tag `rpgprefabhouses:blend_ground`, extendable by datapacks) and the plants on
  it;
* leaves a column alone if anything else is on or in it: builds, logs, liquids, block entities;
* leaves cliffs and ravines (more than 5 blocks off by default) as they are;
* skips claimed chunks the player could not build in.

The placement ghost shows the planned slope as small squares at the new ground height (green raised, amber
lowered), and the HUD counts them. Builder's Hammer extensions do not blend. Server config: `blendTerrain`,
`blendWidth`, `blendMaxStep`.

The mine is planned for the actual placement height and dug down to `mineBottomY` (default y = -32). Every
cell it opens is sealed with a stone/deepslate shell, so caves, aquifers and lava stay out. If the shaft
would cut through containers, player builds or an underground structure, the first click only warns you;
clicking the same spot again confirms the placement. Unbreakable blocks are never touched.

The recovery chests hold **only what the excavation actually removed**. Each block is counted once, at the
moment it is removed, and container contents the shaft cut through are moved into the chests. Nothing else
is ever added. Recovery modes:

* `DROPS`: what hand-mining with an iron pickaxe would give;
* `BLOCKS`: the blocks themselves;
* `NONE`: nothing.

### Builder's Hammer: extending a house

Craft a Builder's Hammer:

```
iron block  diamond  iron block
iron block  stick    iron block
            stick
```

Right-click a house you built from the catalogue to add a **wing** (one room, or two storeys for tall rooms
like a library) or a **tower** (2-4 floors with the room at the top). Choose the room, the size and, for a
tower, the floors. The extension uses the house's style and materials. **Choose spot** returns you to the
world: the server picks where it fits against the house and shows it as a ghost. Press **R** for the next
spot, **left-click** to build and **right-click** to go back to the screen.

A spot is a plain ground-floor wall with a room behind it and open ground outside. The back and sides of the
house come first, then the flattest ground. Only a doorway is cut through the house wall. The extension
never overlaps the house, its porches or another extension. Spots with containers or player builds in the
way are skipped, and the house's own eaves and garden blocks stay as they were. Land claims are respected as
for placement. A house takes up to 8 extensions. Only its owner (or an operator) can extend it.

Houses are remembered when they are placed, so houses built with an older version of the mod cannot be
extended.

## Commands (permission level 2 except `list` and `undo`)

```
/prefabhouse list
/prefabhouse undo
/prefabhouse give [targets]
/prefabhouse spawn <house> [north|south|east|west] [force]
/prefabhouse generate <style> [seed] [width depth] [floors] [facing] [force]
/prefabhouse design <code> [facing] [force]
/prefabhouse verify
```

`generate` builds a generated house in front of you and prints its design code. `design` builds any design
code, for example one copied from a preset file.

`undo` takes away the last house you placed and puts the land back exactly as it was (the chat message after
placing has a clickable [Undo] too). It works for `undoMinutes` (30 by default) and only while nothing of the
house has been broken and no chest in it used, so nothing can be duplicated; your own chests must be taken out
first, and a house extended with the Builder's Hammer can no longer be undone. Whatever was paid for the house
is given back.

Houses are built a little at a time, a few milliseconds of every server tick, so even the biggest house and its
mine never make the server stutter; another house cannot be placed over one still being built.

## Configuration

`serverconfig/rpgprefabhouses-server.toml`:

* **placement**: `requireCatalogue`, `consumeCatalogue`, `placementCost` (what survival players pay for a medium
  house, e.g. `["minecraft:emerald=16", "minecraft:gold_ingot=4"]`; empty = free), multiplied (rounded up) by
  `costBySize` (`tiny=0.5`, `small=0.75`, `medium=1`, `large=1.5`, `huge=2`; the size is the floor area of the
  rooms above ground: under 400, 650, 1500, 2200 blocks, or more), `costByGenre` (e.g. `["wizard_tower=1.5"]`;
  unlisted = 1), `basementCostMultiplier` (1.25, rooms below ground) and `mineCostMultiplier` (1.25, a deep mine).
  The price shows in the placement panel. `undoMinutes` (0 turns undo off),
  `maxPlacementDistance`, `protectedBlockTolerance`, `blockStructureOverlap`.
* **generator**: `allowCustomHouses`, `maxOptionalRooms`.
* **mines**: `deepMines`, `mineBottomY`, `recovery` (`DROPS` / `BLOCKS` / `NONE`).


## How the houses are designed

### Exterior design rules

Every generated house follows the same design rules, tuned by each genre:

* **Shape and depth.** Timber genres jetty their upper floors one block out over brackets. Steep cross gables
  rise through the eaves (a row of them on long fronts). There are dormers on long roof slopes, flared eaves,
  brackets under the eaves and a small window high in each gable end.
* **Cohesion with the rooms.** Windows follow the room behind them:
  * large windows for halls, living rooms, libraries and dining rooms;
  * slits for storage rooms;
  * none for a hidden room.

  Living rooms and libraries can get a bay window with a window seat. Upper-floor rooms such as bedrooms and
  studies can open onto a balcony that runs the length of the wall and wraps around the corners. Chimneys
  stand over the fireplaces and kitchens, preferably on the sides and back of the house.
* **Life.** Ivy and vines on the walls, moss and leaf patches on the roofs, flower boxes under the windows,
  planting beds along the walls, lanterns under the eaves and pots, barrels and lanterns by the doors. Fairy-tale
  genres add coloured roof rings and curled spire tips.

Each genre sets how much of each it uses (from the grounded keep and desert house to the overgrown storybook
manor and fairy hut). Your material choices apply to all of it.

### Exterior character (options)

On top of each genre's own look, every generated house can take these options. They are additions: their
defaults build exactly the houses the genres always built, and saved designs and presets are unchanged.

* **Form.**
  * *Classic*: the genre's own layout.
  * *Off-centre*: the same layout, but the stair bay, front door and porch move to one end, and mirrored pairs
    (two wings, two flanking towers) become one.
  * *Cottage*: a compact, tall cottage composed around one dominant feature pushed to one side, with a lower
    lean-to set back on the other side. The feature is one of: a tall tower at the end of the range, a tower in
    front of it, a cross wing whose gable faces the front, or a narrow front gable beside the door. Whatever fits
    the lot is chosen.

  A cottage keeps its big rooms underground: the magic room, storage and mine go into the basement rows, so a
  cottage always has a large basement. Switching a design to Cottage brings the size down to cottage
  proportions and keeps two optional rooms (you can tick others again).

  A *Small* cottage is the smallest home: a single little range 17-20 blocks wide and deep (the swamp's
  stilts make it 20 deep) over a cellar that spreads out under the garden and holds nearly every room. It
  always has Huge grounds (the cellar needs the room) and Compact or Spacious rooms. Optional rooms that do not
  fit are left out with a warning naming them, so every Small cottage builds.
* **Landscape.**
  * *Tidy*: lawns and straight paths.
  * *Natural*: the house sits in a gentle mound of turf with a ragged edge, level with the ground floor. Around
    it:
    * patches of coarse dirt, moss and podzol;
    * a winding path of trodden earth, gravel and cobbles, with a stone slab where it climbs the mound;
    * drifts of wild flowers, tall grass and ferns;
    * leafy bushes, mossy boulders and a fallen log;
    * trees with lumpy, uneven canopies.
* **Overgrowth.** *Genre default*, *None* (clean walls and roofs), or *Overgrown* (much more ivy, roof moss,
  planting, flower boxes and weathered stone).
* **Roof trim.** The outline of every pitched roof (eaves, gable verges and the foot of each spire) is laid in
  the stone of the house's base, or a contrasting one, so roof and plinth frame the walls together.
* **Wall details.** Each window gets a hood and a sill. Outer corners stand on stone piers (timber houses: a
  post on the front or back face). A rough stone base course runs along the foot of the walls; on stone walls
  it breaks up irregularly.
* **Garden props.** Barrels, crates, firewood stacks, hay, pumpkins, benches, cauldrons, decorated pots and
  little toadstools against the walls, inner corners first. The set of props follows the genre. They stay out
  of doorways and below the windows.
* **Doors.** *Genre default* keeps each doorway as the layout plans it; *Single* or *Double* makes every door
  that width wherever the doorway has room.
* **Pressure plates.** A plate in the door's wood on the floor by every door, so doors open as you walk up and
  close behind you: *Both sides* (new designs; mobs can open the outside doors too), *Inside only* (no plate
  anywhere a mob outside can reach) or *Off*. Design codes made before this option keep their doors without
  plates.

**Surprise me** mixes these in too. Builder's Hammer extensions take on the house's overgrowth, roof trim and
wall details.

### Underground themes

Any house with a basement can give it a theme (**Underground › Style**). A plain basement stays exactly as it
was. A themed one is dug two blocks deeper (three with Huge rooms) and rebuilt in its own style once the
rooms are furnished:

* its own ceiling, crossed every four blocks by ribs resting on corbels;
* pillars engaged in the walls under the ribs;
* lamps hanging from the ribs on chains;
* walls, floors and the stair down in the theme's materials.

| Theme | Character |
|-------|-----------|
| Timber Undercroft | Stone walls, plank floors and ceilings, dark oak beams, barrels and kegs along the walls |
| Dwarven Hall | Deepslate and polished blackstone, gold-flecked floors, a forge with a blast furnace, anvil and lava cauldron |
| Crypt | Cobbled deepslate and mossy stone, checkered floors, soul lanterns, candles, skulls, cobwebs and chains |
| Lush Grotto | Mossy stone, moss floors, glow berries and spore blossoms from the ceiling, azaleas, a pool under a light well |
| Arcane Vault | Deepslate, purpur ribs and pillars, amethyst and end rods, purple carpets, a skylight over the largest room |

*Genre* picks the theme that suits the house: Dwarven for the keep, longhouse and desert house; Crypt for the
alchemist and swamp houses; Grotto for the fairy hut, storybook manor and coastal estate; Arcane for the
wizard's tower; Timber for the rest. A cottage uses its genre's theme by default. Set pieces only use free
floor, never doorways, door approaches, stairs or the enchanting room's sight lines, and the lighting check
tops up anything still dark.

Every house, signature or generated, has:

* an **enchanting/magic room** with a full-power vanilla setup and plenty of free floor;
* a **storage room** with a modest starter set, mostly empty for modded storage;
* a **deep mine**: a lit, supported staircase shaft (spiral or switchback, depending on the style) that is
  dug when the house is placed, all the way down into the deepslate layer, ending in a large chamber with
  **recovery chests**.

