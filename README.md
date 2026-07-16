# Fortune Bastion

An original browser tower-defense prototype inspired by the supplied reference video's core loop: defend a path, collect supplies, and stop escalating enemy waves.

## Run

Open `index.html` in a browser. No installation or local server is required.

## Current gameplay

- Towers live in the inventory, not in the build dock. The inventory scrolls through a 100-tower catalog.
- Use the **ALL**, **ELECTRIC**, **CANNON**, **THORNS**, and **FUSABLE** category tabs above the inventory to filter the catalog and find a tower quickly. A second filter row lets you select any tower grade, and it combines with the first row. **FUSABLE** gathers a tower whenever you have one or more copies in inventory and at least two total copies across inventory and the current field, even at different levels; it shows field count and every current level. Fusion itself still requires matching levels. A roulette result automatically opens its matching category and grade.
- The catalog has 10 unique tower models across 12 grades (120 tower types): Common, Uncommon, Rare, Epic, Legendary, Mythic, Ancient, Celestial, Divine, Transcendent, Eternal, and Apex.
- Every new game starts with three Common starter towers in the inventory.
- The **Draw Tower** button begins at **100 supplies** and adds one random tower to the inventory. Its cost rises by 50 supplies after every defeat. Supplies are retained on defeat; if the retained amount is below the new draw cost, it is raised to that cost for one guaranteed draw.
- **Roulette Mastery** is a permanent base upgrade chosen after defeat. Levels 1–9 can draw only Common through Rare; Epic and Legendary enter at level 10; Mythic and Ancient enter at level 20; Celestial through Transcendent enter at level 40; Eternal enters at level 50; and Apex enters at level 60. Map-gated grades still require their stage to be unlocked.
- **Expand Build Slots** is a permanent base upgrade chosen after defeat. Every map starts with all of its original build zones visible (9 / 11 / 12 / 13 / 14 from Stages 1–5). Each upgrade adds an extra build zone, up to 13 / 17 / 19 / 21 / 23 total zones respectively, with no locked-zone placeholders.
- The draw button now spins a visible tower roulette through the complete tower catalog before revealing the selected tower and prevents duplicate clicks while the roulette is in progress.
- The roulette recovers automatically if its animation is interrupted, and clearly shows the current cost and any missing supplies.
- Select an owned tower, then click a glowing hexagonal build zone to install it.
- Click an installed tower to select it, then use **Upgrade**. Each level increases damage, range, and attack speed. Upgrade costs are 90 supplies per current level.
- Use **All Upgrade** to raise every installed tower that is not at its level cap by one level at once. The button displays the tower count and total cost, and only activates when enough supplies are available.
- Higher grades have higher level caps, from Common level 3 to Apex level 14. The same cap applies to fusion.
- Use **Fuse Match** on a selected tower, then click another installed tower with the same type and level. The two towers merge into one level higher tower for no supply cost. Fusing two maximum-level towers promotes the result to level 1 of the next rarity; Apex is the final rarity.
- While fusion is armed, use **Cancel Fusion** in the upgrade panel to return to normal play without consuming either tower or any supplies.
- Waves continue infinitely and increase in difficulty. A cleared wave rewards 50 supplies on wave 1, then the clear reward increases by 10 supplies every wave (wave 2: 60, wave 3: 70, and so on).
- Every defeated regular invader rewards 10 supplies on wave 1 and gains 5 more supplies per wave; elite and boss rewards scale by the same +5-per-wave amount.
- Twelve regular enemy types and six elite types now rotate through the waves, with distinct health, speed, size, color, and keep-damage profiles. Their current `DMG` value is displayed above their health bar; higher stages add +1 keep damage.
- Every enemy displays its name above the health bar, making normal, elite, and boss targets easy to identify.
- Use **INDEX** on the board to browse every tower and enemy, including their core damage, range, speed, and keep-damage stats.
- Use **STATS** to view persistent overall statistics: total, normal, elite, and boss kills; supplies earned; roulette draws; cleared and highest waves; and defeats. These totals save automatically in the browser.
- Each of the ten tower models now has a distinct board silhouette, including separate leaf, ice-bramble, and venom-vine visuals for thorn towers.
- Higher-grade towers now have escalating physical visuals as well as board effects: an aura at Uncommon, crystals at Rare, a crown at Epic, wings at Legendary, then increasingly elaborate arcs, runes, stars, halos, and a transcendent starburst through the highest grades. Higher grades also make the tower model itself slightly larger.
- Every tower model has a unique combat ability that becomes stronger with rarity: chains, shock, prism splits, storm arcs, splash attacks, burning shots, roots, freeze, and poison. The current ability is shown in the upgrade panel and index.
- Every 30th wave (30, 60, 90, and so on) introduces the Ancient Bastion boss with a scaling health pool and a 500-supply reward. Every boss defeat permanently raises Permanent Keep Health by 1 level (+5 starting health) with no level cap, and immediately restores 5 keep health. It also has a 50% chance to increase permanent Roulette Mastery by one level (up to level 40).
- Use the mouse wheel over the game board to zoom between 70% and 220%; zoom stays centered on the pointer.
- Hold `W`, `A`, `S`, or `D` to move the camera view; camera speed adjusts to the zoom level.
- Use **Reset View** beside the wave button to return the camera to the default position and zoom.
- When the keep falls, choose one persistent base upgrade: Lucky Dice improves high-grade draw odds, Permanent Keep Health adds 5 starting health per level with no level cap, and Battle Doctrine adds 10% tower damage. The health card shows its current permanent bonus and next level value.
- After defeat, placed towers remain in their current build locations, but all placed and stored tower levels reset to level 1 for the new defense.
- The board now includes a shoreline, animated water, trees, and rock formations around the defensive field.
- A monster portal sits near the beginning of every map path. Every enemy emerges directly from it and can only advance toward the keep; it glows, rotates, and emits particles while a wave is active.
- Maps unlock strictly by stage through the defeat upgrade screen: Stage 1 Verdant Coast is available from the start, **Unlock Stage 2** opens Ember Canyon plus Mythic and Ancient grades, **Unlock Stage 3** opens Frostwind Pass plus Celestial through Transcendent grades, **Unlock Stage 4** opens Thundercrown Ridge plus Eternal, and **Unlock Stage 5** opens Obsidian Eclipse plus Apex. Each map keeps its own placed tower layout and tower levels when you switch away and return. Permanent upgrades and map unlocks are also saved independently, so changing maps never removes them.
- Use the **NEXT** and **PREV** map controls between waves to move through unlocked stages in either direction.
- Higher stages use longer, more winding paths and add enemy difficulty: each stage raises enemy health by 40%, speed by 10%, and adds two enemies to every wave.
- The HUD displays the current map difficulty: Stage 1 Normal, Stage 2 Hard, Stage 3 Extreme, Stage 4 Nightmare, and Stage 5 Apocalypse.
- Use the mouse wheel over the tower inventory to browse its 100 tower cards horizontally.
- Click a placed tower to show its attack range as a colored circle; the circle updates when the tower is upgraded or fused.
- A selected placed tower can be sent back to the inventory with **Store Tower**. Its type and current level are preserved when it is placed again.
- Thorn-type towers (Thorn Garden, Frost Bramble, and Venom Hedge) must be installed directly on the enemy path instead of a glowing build zone.
- Press `Space` or **Start Wave** to begin the next wave.
- Use **Auto Wave** to automatically launch the next wave 1.2 seconds after the previous wave is defeated. It turns off after defeat or a fresh game.
- Use **Save Game** at any time to store progress in the current browser. During a wave it also saves active monsters, their health and positions, pending portal spawns, and the wave state so the defense continues when reopened.
