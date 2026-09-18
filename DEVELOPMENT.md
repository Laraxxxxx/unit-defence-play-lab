# Last Light: City Siege — development notes

## Direction

Build a tactical squad survival game whose battlefield tells a story. The player should understand where danger comes from, why their defence failed, and what a different squad arrangement could achieve. Keep direct control of every unit. Make the squad the main weapon; fortifications buy time.

The first four experiments established controls and roles. Their main weakness was spatial: enemies arriving around the perimeter gave the player little opportunity to form a useful plan. Merely adding more enemies and upgrades would amplify that problem.

## What the research suggests

These are design interpretations, not claims that our game recreates the source games. Research used the readable document text; Scribd's separate AI-generated questions were not treated as the manual.

| Reference | Observed design | Our interpretation |
|---|---|---|
| [AVP Extinction bestiary](https://avp.fandom.com/wiki/Aliens_versus_Predator:_Extinction_Bestiary) | Support specialists supply healing, repairs, detection and reinforcements. Snipers trade close-range safety and firing speed for reach and penetration. Upgrades can counter status effects or change attacks. Alien support can extend regeneration territory. | Units should solve different problems. Protect a medic to sustain the line; shield a stationary marksman from flankers. The alien game should use living territory as a resource and positional constraint. |
| [Celtic Kings manual hosted on Scribd](https://www.scribd.com/document/851765780/Celtic-Kings-Rage-of-War) | Formations, stand-ground orders, experience, consecutive-hit bonuses, charge attacks, defensive first-hit protection, healing and equipment create distinct combat roles. | Movement should have a cost: a gunner builds pressure while firing at one target, but loses that advantage when repositioning. Add a formation order and deliberate defensive abilities. Avoid reproducing its exact values or roster. |
| [They Are Billions — developer's Steam description](https://store.steampowered.com/app/644930/They_Are_Billions/) | Tactical pause permits orders; terrain, fortifications, survival maps and a campaign shape play. Noise can attract infected. | Give unlimited planning time and clearly announced road threats. Later, noise should be a visible trade-off with a forecast, not an invisible punishment for firing. |
| [Infection Free Zone — publisher's Steam description](https://store.steampowered.com/app/1465460/Infection_Free_Zone/) | Existing city buildings become useful locations. Scavenging, vehicles and settlement defence connect geography to resources. | Hospitals, workshops and blocked intersections should matter mechanically. Move survivors to supply sites and decide whether to expose specialists during an attack. Use a fictional authored city first. |
| [Kingdom Rush — Ironhide](https://www.ironhidegames.com/Games/kingdom-rush) | Tower specializations, varied environments, enemy abilities, reinforcements and commanded troops broaden defence choices. | Start with understandable lanes and counters, then combine them. Area damage handles crowds; armour penetration handles heavy targets; slows create time for both. |
| [The Last Spell — developer/publisher Steam description](https://store.steampowered.com/app/1105670/The_Last_Spell/) | A small squad defends a city, rebuilds between attacks, manages scarce recovery, and adapts to distinct maps and elites. | Give each battle consequences and a calm recovery phase. A short campaign should carry survivors and upgrades forward. Endless mode should ask whether the same build survives changing pressure. |

## Playable iteration in this delivery

**Last Light: City Siege** is the deeper zombie prototype. Its first campaign has three districts with three assaults each. Endless uses the same tactical systems with continuing escalation and a new district after every three assaults. This is an authored campaign framework, not a finished story campaign.

- Enemies enter through named roads. A forecast shows active routes, enemy composition and the three arrival groups before the player starts.
- Buildings obstruct shots and movement. Wrecks provide nearby cover; damaged vehicle barricades hold a road until destroyed. Friendly troops can pass through the barricade's access gap.
- Every assault waits for the player. Pause supports issuing movement orders. A line formation and attack-move reduce control friction.
- Six initial specialists plus a recruitable engineer. Each has a manual ability, a weakness and two mutually exclusive specializations. Medic group healing can be extended with toxin treatment.
- Supplies buy repairs, recruits and unit specializations. Reward choices also offer abilities and supplies. Supply sites reward a unit that reaches and holds the location; contested sites stop progress.
- Survivors, their skills and supplies carry between districts. Preparation and reward checkpoints can be resumed in the same browser. A battle resumes from its start checkpoint rather than its exact interrupted instant.
- Boss ground attacks have a visible warning and time to move. Special enemies appear gradually.

## Unit identity and counterplay

| Unit | Job and limitation | Choices |
|---|---|---|
| Infantry | Durable mobile screen; moderate damage | Brace to reduce incoming damage, or improve moving fire. Rally briefly protects nearby allies. |
| Medic | Sustain the squad; cannot attack | Group healing or stronger individual triage. Later toxin training cures poison. Emergency treatment gives a short burst of nearby healing. |
| Flamer | Clear a narrow choke; short range | Lingering burns or a longer cone. Firebreak buys space but has a cooldown. |
| Grenadier | Break clustered enemies; weak when rushed | Wider blasts or armour-breaking shells. Concussion temporarily stalls a crowd. |
| Sniper | Remove armoured and support enemies; poor when crowded | Armour piercing or a finishing shot specialization. Must stop to aim. |
| Gunner | Slow the front of a swarm; slow relocation | Sustained focus builds damage, or area suppression. Emergency suppression helps a retreat. |
| Engineer | Keep a nearby barricade functioning; low firepower | Faster repairs or a broader repair radius. A manual patch restores a nearby damaged barricade. |

Specializations change behaviour rather than adding an endless ladder of percentages. Their prices compete with replacing a casualty or restoring a failing roadblock. New recruits start without individual specializations, so survivors have value.

## Alien direction

The two alien prototypes remain available as comparisons. Their next major revision should diverge from the human game instead of simply renaming the human weapons.

**Rift Wardens: expedition defence.** A compact human team stabilizes sites while retreating through hostile terrain. Add a surveyor that exposes ambushers, a shield carrier that protects a directional arc, and a medic choosing between trauma care and toxin protection. Enemy pressure is traced to visible fissures. Destroying or sealing one changes the route network. An exposed ranged attacker, a flanker and an armoured breaker should demand different responses.

**The Living Front: territory and evolution.** A colony spreads a living network between nodes. Creatures regenerate on connected ground; leaving it enables raids at the cost of sustain. A mobile support creature extends this network temporarily. Biomass choices compete: repair a node, spawn bodies, or evolve one veteran. Proposed original roles: Rootwarden (anchors defence), Glassspine (fragile piercing shot), Veilrunner (flanker), Chorus (support), and Seedbearer (network expansion). Use new silhouettes, fiction and effects.

**A possible third faction:** salvage automatons that recover wreckage, share battery power and overheat. Their economy should concern energy and repair logistics rather than human healing or alien biomass. This remains a proposal, not an implemented faction.

## Campaign beyond this prototype

1. The junction teaches a single useful firing line and rescue of resources.
2. The hospital splits the squad, introduces toxins, and tests support positioning.
3. The terminal pressures two crossings and adds a final evacuation defence.
4. Future missions can add a moving ambulance, power restoration, limited ammunition during a blackout, civilian escort, and controlled fallback between barricades.

Prefer objectives that change decisions over longer health bars. Use optional objectives and authored map variants before attempting unrestricted procedural cities. Between missions, offer a choice of route with clearly disclosed consequences: clinic supplies, workshop repairs or a faster but more dangerous crossing.

## Endless and future cooperation

Endless already escalates counts and enemy durability, varies announced routes, and carries the squad forward. Further variety should come from mutators with counterplay: heavy rain reduces visibility, an evacuation column occupies one road, or a supply crash invites a risky excursion. Show the modifier in advance. Do not quietly spawn enemies behind the player's squad.

Multiplayer is a later engineering project. Recommended first format: two-player cooperative defence with shared objectives and supplies, individually owned squads, pings, and unanimous tactical pause. It needs an authoritative simulation service, command validation, reconnection, lobby identity and latency testing. GitHub Pages can host the client but not that server. The current game is single-player; its simulation is separated from rendering and uses a seeded random generator, but it is not a tested network simulation.

## What to measure next

- Can a new player explain the next threat from the briefing alone?
- Does a moved firing line outperform leaving the entire squad on its initial positions?
- Do two different specialization paths survive the same district?
- Do players spend supplies on at least three distinct uses?
- Is a failed defence understandable: lost barricade, exposed support, ignored flanker, or missed boss warning?
- Are retries different without relying on blind random punishment?

Aim for useful decisions every 15–30 seconds during combat, with no countdown forcing the player out of preparation. Treat those as playtest targets, not measured claims. More content comes after repeated external playtests establish that the core is enjoyable.

## Original work

The implementation uses our own code, maps, unit descriptions and procedural drawings. Research informs general design principles. No franchise artwork, characters, dialogue, audio or extracted game files are included in the published game. The references are research sources, not affiliations or endorsements.

## Validation for v0.2

23 automated simulation checks passed, covering road connectivity, barriers, pause, damage counters, healing and cleansing, specialist costs, engineer repair, scavenging, save roundtrips, campaign transitions and completion rules. A scripted squad-management run completed all nine campaign assaults; a separate endless run completed twelve. These are functional checks and preliminary balance probes, not a substitute for human playtesting.

Browser testing covered the opening assault through its reward screen, buying medic group healing, selecting toxin treatment, reloading and continuing with both upgrades retained, and movement orders while paused. No browser errors were reported during those checks.

Known limits: authored maps, modest swarm sizes, basic collision avoidance, no audio, no full story campaign, no online co-op. The alien scenarios are still the early experiments; the alien revisions above are design proposals. New city systems are separate from those prototypes so further iteration remains manageable.
