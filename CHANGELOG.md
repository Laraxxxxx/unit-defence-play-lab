# City Siege v0.3.1 — Formation facing and scavenging

[Play City Siege](https://laraxxxxx.github.io/unit-defence-play-lab/city.html)

## Turn your formation before moving

1. Select the units you want to move.
2. Press and hold the **right mouse button at the destination**.
3. Drag towards the direction the group should face. An arrow marks the front, and ghost units show their destinations.
4. Release to issue the move. **Escape cancels** without moving or clearing your selection.

The destination stays where you first pressed. Block formation places infantry, flamers and gunners ahead of support units and snipers. Line formation rotates the whole line so everyone stands abreast. Slots shift to open ground around buildings and at map edges; shifted preview slots are amber. Units correct small nudges as they settle into position.

A normal right-click still moves; right-clicking an enemy still focuses fire. Facing orders also work while paused and with individual units. Units can still turn to engage enemies after reaching the formation. The chosen facing is retained for later moves and saved checkpoints.

## Scavenging checks the collector, not the neighbourhood

The old 180-radius danger check around the crate has been removed. One stationary survivor now collects a crate for seven uninterrupted seconds. Only direct danger to that survivor interrupts collection:

- An enemy is targeting the collector within its actual attack range and has a clear shot.
- A poison projectile or boss warning will hit the collector's current position.
- The collector has taken damage within the last two seconds, including poison damage.

The collector shooting enemies does **not** interrupt scavenging. Enemies fighting another survivor do **not** interrupt it unless an incoming area attack also threatens the collector. If several survivors are at a crate, a safe one can collect even while another is attacked. A new collector starts their own seven-second attempt.

Collection remains combat-only and unlocks after the first infected arrive. It can continue in quiet gaps between the announced attack groups. Leaving, moving, changing collectors, or finishing an assault clears partial progress. Each crate still pays once. The crate and selected collector show progress or the reason collection is stopped.

## Compatibility and checks

Existing saves continue to work; no squad, supplies, upgrades or rank reset is needed. Older checkpoints without formation facing use the default north-facing arrangement.

62 City Siege simulation checks pass, including direct versus unrelated threats, collection during wave gaps, interrupted final collection frames, collector changes, four-direction formation rotation, paused orders, obstacle placement and saved facing. Browser checks cover the held-button preview, release, cancellation and normal movement.


---

# City Siege v0.3 — The specialist update

[Play the updated game](https://laraxxxxx.github.io/unit-defence-play-lab/city.html)

## Squads and progression

- **Useful rewards.** Specialization cards name their exact recipient, such as Sniper S11. A trained survivor cannot receive the same specialization again. Full squads are not offered extra recruits; recovery appears only when someone or the shelter is hurt. Repeatable field drills and district roadblock reinforcement provide real improvements and disappear when their bonuses are capped.
- **Controlled veteran growth.** The first rank needs 7 XP, then each rank requires 3 more XP than the previous one. Each rank adds 4% of base damage and 8 maximum health, stopping at +40% damage and +80 health. Rank badges can continue increasing beyond that. This replaces runaway compounded damage.
- **Medics:** a 6-damage pistol fires independently of healing. Restore 40 health to other survivors to earn 1 XP. Single treatment, healing aura, and emergency treatment cannot heal or cleanse the caster. A second medic can treat the first. Overhealing earns no XP.
- **Engineers:** recruit for 45 supplies at the top of Supplies & training. Move within 115 of a standing damaged roadblock to repair 7 HP/s in combat, using 1 supply per 5 seconds of work. Earn 1 XP per 50 HP actually repaired. Fast weld doubles repair speed; Repair drone extends reach to 195. Emergency patch restores up to 150 HP. Destroyed barriers still require rebuilding between assaults.
- **Making room:** select a survivor, open Supplies & training, and send them to shelter duty. This requires confirmation, permanently removes that survivor from the active squad, and gives no refund. It lets a full squad replace a sniper with a second medic or engineer.

## Weapons and tactical positions

- **Snipers:** base damage 66 → 60; shot interval 2.1 → 2.3 seconds, about 17% lower sustained damage before rank bonuses. Must still aim for 0.6 seconds and deal only 25% damage under close pressure.
- **Piercing shot [Q]:** right-click an enemy to choose a direction, then use the ability. The first enemy in that line takes 150% weapon damage; each subsequent hit retains 70% of the previous hit. Armour applies unless Hard target is trained. Buildings and solid wrecks stop the shot. Cooldown: 24 seconds. Friendlies are not hit.
- **Grenadiers:** damage 38 → 46 and shot interval 2.1 → 2 seconds. Incendiary rounds replaces the old Fragmentation specialization: radius 78, plus a radius-64 fire zone lasting 5 seconds at 10 DPS. Overlapping ground fires use the strongest effect rather than stacking. Fire kills credit the attacker. Breach shells remains the alternative for stripping armour.
- **High ground:** two gold lookout platforms per district grant +12% weapon range while occupied. They are reachable ground features; normal visibility and movement rules still apply.
- **Spotter network:** a sniper upgrade costing 40 supplies grants other visible allies within 140 an 8% weapon-range aura. Healing range is unchanged.
- **Protective formation:** an infantry upgrade costing 35 supplies reduces damage to other visible allies within 140 by 12%. These aura upgrades are separate from the survivor’s specialization. Matching auras never stack. High ground plus a spotter gives +20% range.

## Streets and enemies

- **Combat-only scavenging:** crates cannot be collected in preparation or before infected arrive. Collection needs 7 continuous seconds with a survivor nearby and no visible infected within 180. Leaving or becoming contested resets progress. Crates pay their normal value plus the 15-supply combat bonus, once per district visit.
- **Wider pursuit:** ordinary infected notice exposed survivors within 240; poison carriers detect them within 280. Scavengers can be chased before enemies reach a barricade. Melee attacks still require physical contact. Intact barriers screen their far side from melee pursuit.
- **Rare Blight carriers:** one poison thrower every fourth assault; two from endless assault 16. The forecast announces arrival at 35 seconds (and 55 for the second). They throw poison up to 230 away, including over a roadblock if they have a clear shot. Purple impact circles give 1 second to dodge. A hit adds 14 seconds of poison; toxin treatment cures it.
- **Splitters:** introduced on assault 6. Killing one releases two smaller infected at its death location. Each has 42 base health versus the parent’s 180, lower damage, and greater speed. Children cannot divide. The assault continues until they are defeated; forecasts disclose the extra offspring.
- **Endless pressure:** after assault 9 every road becomes active, waves contain more Breakers, and health and damage scale more strongly. Enemy arrivals become denser. From assault 18, boss assaults contain two Wreckers.

## Existing saves and validation

Existing campaign and endless checkpoints remain usable. Squads, earned ranks, specializations, supplies and cleared assaults are preserved. Veteran statistics adopt the new balance, the old Fragmentation upgrade becomes Incendiary rounds, and old reward screens regenerate valid choices. No old rewards or resources are taken back. In-progress battles still reload from their preparation checkpoint.

50 automated City Siege checks cover these changes, plus 15 checks for the four original prototypes. A scripted squad-management run completed the nine-assault campaign; the same simple strategy lost on endless assault 10. These are functional checks and balance probes, not a claim of perfect balance or a substitute for player feedback.
