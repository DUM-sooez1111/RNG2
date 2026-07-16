# Fortune Bastion

An original browser tower-defense prototype inspired by the supplied reference video's core loop: defend a path, collect supplies, and stop escalating enemy waves.

## Run

Open `index.html` in a browser. No installation or local server is required.

## Current gameplay

- Towers live in the inventory, not in the build dock. The inventory scrolls through a 50-tower catalog.
- The catalog has 10 unique tower models across 5 grades: Common, Uncommon, Rare, Epic, and Legendary.
- Every new game starts with three Common starter towers in the inventory.
- The **Draw Tower** button begins at **100 supplies** and adds one random tower to the inventory. Its cost rises by 50 supplies after every defeat, while each new defense starts with enough supplies for at least one draw.
- The draw button now spins a visible tower roulette through the complete tower catalog before revealing the selected tower and prevents duplicate clicks while the roulette is in progress.
- The roulette recovers automatically if its animation is interrupted, and clearly shows the current cost and any missing supplies.
- Select an owned tower, then click a glowing hexagonal build zone to install it.
- Click an installed tower to select it, then use **Upgrade**. Each level increases damage, range, and attack speed. Upgrade costs are 90 supplies per current level.
- Higher grades have higher level caps: Common 3, Uncommon 4, Rare 5, Epic 6, and Legendary 7. The same cap applies to fusion.
- Use **Fuse Match** on a selected tower, then click another installed tower with the same type and level. The two towers merge into one level higher tower for no supply cost.
- Waves continue infinitely and increase in difficulty. Every completed wave rewards exactly 50 supplies.
- Every defeated regular invader rewards 10 supplies; elite invaders reward 25 supplies.
- Six regular enemy types and three elite types now rotate through the waves, with distinct health, speed, size, color, and keep-damage profiles. Their current `DMG` value is displayed above their health bar; higher stages add +1 keep damage.
- Every enemy displays its name above the health bar, making normal, elite, and boss targets easy to identify.
- Every 30th wave (30, 60, 90, and so on) introduces the Ancient Bastion boss with a scaling health pool and a 250-supply reward.
- Use the mouse wheel over the game board to zoom between 70% and 220%; zoom stays centered on the pointer.
- Hold `W`, `A`, `S`, or `D` to move the camera view; camera speed adjusts to the zoom level.
- Use **Reset View** beside the wave button to return the camera to the default position and zoom.
- When the keep falls, choose one persistent base upgrade: Lucky Dice improves high-grade draw odds, Fortified Keep adds 5 starting health, and Battle Doctrine adds 10% tower damage. Each can reach level 10.
- After defeat, placed towers remain in their current build locations, but all placed and stored tower levels reset to level 1 for the new defense.
- The board now includes a shoreline, animated water, trees, and rock formations around the defensive field.
- A monster portal sits near the beginning of every map path. Every enemy emerges directly from it and can only advance toward the keep; it glows, rotates, and emits particles while a wave is active.
- Maps unlock strictly by stage through the defeat upgrade screen: Stage 1 Verdant Coast is available from the start, then **Unlock Stage 2** opens Ember Canyon, followed by **Unlock Stage 3** for Frostwind Pass. Each map keeps its own placed tower layout and tower levels when you switch away and return.
- Use the **NEXT** and **PREV** map controls between waves to move through unlocked stages in either direction.
- Higher stages use longer, more winding paths and add enemy difficulty: each stage raises enemy health by 40%, speed by 10%, and adds two enemies to every wave.
- The HUD displays the current map difficulty: Stage 1 Normal, Stage 2 Hard, and Stage 3 Extreme.
- Use the mouse wheel over the tower inventory to browse its 50 tower cards horizontally.
- Click a placed tower to show its attack range as a colored circle; the circle updates when the tower is upgraded or fused.
- A selected placed tower can be sent back to the inventory with **Store Tower**. Its type and current level are preserved when it is placed again.
- Thorn-type towers (Thorn Garden, Frost Bramble, and Venom Hedge) must be installed directly on the enemy path instead of a glowing build zone.
- Press `Space` or **Start Wave** to begin the next wave.
- Use **Auto Wave** to automatically launch the next wave 1.2 seconds after the previous wave is defeated. It turns off after defeat or a fresh game.
- Use **Save Game** between waves to store progress in the current browser. Saved maps, unlocks, base upgrades, tower layouts for every map, inventory, resources, and camera position are restored when the game is opened again.
