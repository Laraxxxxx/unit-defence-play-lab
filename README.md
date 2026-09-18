# Unit Defence: four playable experiments

Open the published GitHub Pages link in Edge, Chrome, or Firefox, or download and open **index.html** locally. This edition contains all scripts inside that one file. No installation, player account, external libraries, or game assets are required. These are original 2D prototypes intended to compare mechanics. Publishing instructions are in PUBLISH.md.

## The four versions

| Prototype | What to try |
|---|---|
| Last Light — zombies | Protect a depot across six waves. Try a frontline flamer and gunner, with the sniper and medic behind them. |
| Dead Road — zombies | Escort the truck. It moves with an ally within 150 units, but stops with enemies within 100. Clear enemies and reach the checkpoint to finish each encounter. |
| Rift Wardens — aliens | Move the expedition to the glowing rift and occupy it for eight uncontested seconds. Clear the attackers as well. The target changes each encounter. Your squad is the survival objective; the rally point is not a defendable base. |
| The Living Front — alien player faction | Defend the heart from machines. Nearby allies regenerate; kills earn biomass. Spend eight biomass to grow a skirmisher, up to 18 living units. Melee skirmishers need movement or focus-attack orders to close on ranged enemies. |

Each version has six encounters, with bosses on encounters three and six. The shared combat engine makes it easier to compare objectives and mechanics without investing in four separate art pipelines. Brood roles share some underlying weapon mechanics with the expedition, with different names, melee/range/health values, regeneration, and growth.

## Controls

- Left-click a unit, use its roster button, or drag a box to select.
- Hold Shift to add units to a battlefield selection.
- Right-click the ground to move. Right-click an enemy to focus it.
- Press A, then click the ground, to advance and stop for enemies in range.
- Press H to stop and hold. Units attack automatically in range.
- Space pauses or resumes. Movement orders can be issued while paused.
- Ctrl+A selects the whole squad. Keys 1–6 select all units of a role.
- The Move order and Attack-move buttons are alternatives to keyboard shortcuts.
- After clearing an encounter, choose one reward. Reposition freely before starting the next one.
- The game pauses when its window loses focus. Use Resume when returning.

## Roles and upgrades to compare

- Infantry: steady medium-range fire; can shoot while moving at reduced damage.
- Medic: heals one nearby ally. Healing aura changes this to a smaller pulse for all nearby allies. Toxin cleansing then removes poison on healing pulses.
- Flamethrower: short cone against crowds; can gain lingering damage.
- Grenadier: delayed splash damage; can gain a larger explosion radius. Reduced damage at very short range. No friendly fire in this prototype.
- Sniper: long range and heavy hits, but cannot shoot while moving. An enemy within 105 world units reduces its shot damage to 25%.
- Gunner: sustained fire slows enemies. Moving reduces damage, while a later upgrade improves stationary fire.

Kills can increase unit rank, maximum health, and damage. Living units keep ranks between encounters. Rewards offer support development, a combat upgrade, another unit, or emergency healing and repair. Ordinary recruits inherit unlocked squad upgrades.

## Terrain and enemies

Buildings block movement and direct fire. Units find routes around them. Cover reduces incoming ranged damage; high ground increases weapon range; water slows movement. Boss ground strikes have visible warnings so units can move away.

Zombies include slow hordes, runners, brutes, poisonous spitters, and callers that summon additional runners. The alien expedition meets fast shardlings, hunters that prefer nearby specialists, armoured shell bearers, and toxic ranged enemies. The brood faces machines alongside other hostile threats. Enemy health and damage rise through the run, and spawn positions vary.

## Deliberate limits

These are gameplay tests, not finished games. Art is labelled geometric placeholders. There is no sound, multiplayer, inventory, full campaign, or saved mid-run state. Best cleared encounter per mode is stored locally if the browser allows it. Balance has had initial simulation checks, but still needs human playtesting. Formations, pathfinding, and collision avoidance are simple. Position choices matter; the prototypes do not yet contain a large variety of maps or upgrade trees.

The source is included so the chosen version can be extended. No Celtic Kings, Aliens, or Predator source code, artwork, music, unit models, or dialogue was reused.
