# Stick Figure Wars

A 3D stick-figure shooter that runs in the browser — drawn in a school notebook. Play solo against bots or with friends online through a room code. No install, no account.

**Play:** https://fifsok-star.github.io/stick-figure-wars/

🇵🇱 [Polski opis niżej](#po-polsku)

## Features

- **Third- or first-person view** (switch with `V`), crouching, jumping and diving into cover.
- **Seven modes:** team deathmatch, elimination (round-based), survival against waves, capture the flag, bomb (plant / defuse), a battle royale for up to 128 players with a shrinking zone and loot crates (carry two main weapons), and **Conquest**: capture points A–E by standing in their circle; deaths and the enemy holding more points drain your team's tickets.
- **Classes in Conquest** (gadget on `Z`): Assault — rifle, grenades, vest, drops an ammo box; Medic — heals the team nearby, revives fallen teammates by standing next to them (the fallen can wait up to 25 s for a medic), drops a medic bag; Engineer — shotgun and rocket launcher, repairs vehicles, builds sandbag cover (explosions destroy it); Sniper — sniper rifle, recon marks enemies in front of him for the whole team. Before every spawn a deploy screen lets you pick the class (`1`–`4`) and where to spawn: the base, a point your team holds or next to a squad mate (even straight into their vehicle). Each team is split into squads of 4 — your squad is shown in green, with a squad panel on the left.
- **Vehicles on the Front map** (seats in brackets): tank (2), armoured personnel carrier (5), Humvee with a gun turret (4), helicopter (4), jet (1). `E` gets in and out, `1`–`5` switch seats. Tanks and APCs: `WASD` drive, the mouse aims the gun. Helicopter: `W`/`S` forward and back, `Space`/`C` up and down. Jet: `W`/`S` throttle, the mouse steers. Bots drive ground vehicles and ride as gunners.
- **Thirteen maps:** **Front** (520×360, built for Conquest with vehicles — machine guns and autocannons overheat after ~4 s of continuous fire: a village, a farm, a market square with a church, forests and two airfields), **Town** (240×170, Conquest without vehicles: narrow streets and a square with a fountain; every house and the church can be entered — doors open as you walk up, windows break when shot, two-storey houses have stairs, an upper floor and furniture, the same goes for houses on the Front map; grenades, rockets and tank shells blow holes in walls, smash furniture, sandbags, fences and trees, a house that loses enough walls collapses into a rubble field with broken wall stumps, tanks drive straight through, explosions leave craters with a dirt rim, in Conquest and Battle royale every wall, crate and prop on every map can be destroyed (bullets chip away at them too); other modes keep objects intact, and the knife breaks windows and light objects), three small ones (Notebook, Cardboard, Blackboard), three medium ones modelled in Blender (Gym with climbable bleachers, Desk, Cafeteria), two large Blender maps (School with corridor and classrooms, Schoolyard with buses, trees, containers and a shed you can walk into) and three large mazes built from giant books, rulers, pencils and binders.
- **Economy and shop:** money for kills, headshots, surviving and winning rounds. Eleven guns in the shop (incl. revolver, MP5, burst rifle; the grenade launcher only drops from crates in Battle royale and comes with the Engineer in Conquest), a knife you can hold as a weapon, weapon mods (suppressor, red dot, extended mag, grip), vest and helmet, medkit, frag, flash and smoke grenades.
- **Bots** with three difficulty levels fill empty slots and play the objectives.
- **Online play without a server:** players connect browser-to-browser. The first person in a room becomes the host, starts the match from the lobby and can send an invite link.
- Blood, bullet holes and shells that stay until the end of the round, damage numbers, scoreboard, round results with the best player and their best play, a celebration for the winning team and a crown for the battle royale winner.
- Text chat (all / team), spectator mode, team switching, settings for volume and sensitivity, touch controls for phones.
- FPS counter under the minimap (can be turned off in Settings).
- Interface size slider in Settings (70–160%).
- Sunlight with real-time shadows (can be turned off in Settings; off by default on phones).
- **Languages:** Polish, English, German, Ukrainian, French.

## Controls

| Key | Action |
|---|---|
| `W` `A` `S` `D` | Move |
| Mouse | Aim |
| Left click | Shoot |
| Right click | Aim (every gun): in third person the camera moves over the right shoulder, in first person you look down the sights; sniper scope; stronger zoom with a red dot |
| `Space` | Jump |
| `C` | Crouch |
| `Shift` | Dive to cover |
| `R` | Reload |
| `1` `2` `Q` / wheel | Switch weapon |
| `3` `4` `5` | Choose grenade (frag / flash / smoke) |
| `G` | Throw grenade |
| `Z` | Class gadget (Conquest) |
| `E` | Open a crate / pick up a weapon or item / get in or out of a vehicle (nothing is picked up automatically) |
| `F` / middle mouse button | Knife |
| `X` | Knife in hand (stab with left mouse button) |
| `Ctrl` / left `Alt` | Sneak — slow and silent, no footsteps |
| `H` | Drink a potion (Battle royale) |
| `B` | Shop |
| `Tab` | Scoreboard |
| `Enter` / `Y` | Chat to all / to team |
| `V` | First / third person; when spectating: follow, player's eyes, free camera, overhead |
| `Esc` | Pause, settings, switch team, spectate |

On phones the game shows on-screen buttons: the left side of the screen moves, the right side aims.

## Playing online

1. Everyone opens the game link.
2. Type the same **room code** (letters, digits, `-`) and press **Play** — or the host clicks **Invite** in the lobby and sends the link; the code fills in by itself.
3. The first person in the room is the host: they pick the mode and map and press **Start**. Bots fill the free slots.

Connections are peer-to-peer (WebRTC via [PeerJS](https://peerjs.com/) and its free signalling server). If the host leaves, another player takes over the room. Some networks (certain company networks and mobile carriers) block direct connections — players on them may not be able to join.

## Tech

- One self-contained `index.html`: game logic, maps, textures and sounds are generated in code.
- [three.js](https://threejs.org/) r128 for 3D, PeerJS for networking — both loaded from public CDNs.
- Weapons, weapon mods, grenades, helmet, vest, medkits, deployables, vehicles and map props were modelled in [Blender](https://www.blender.org/) and are embedded as glTF.

## Hosting

The game is served by GitHub Pages from the `main` branch. To host it elsewhere, upload `index.html` to any static hosting.

---

## Po polsku

Strzelanka 3D z patyczakami w przeglądarce, narysowana w zeszycie. Grasz sam z botami albo ze znajomymi przez kod pokoju — bez instalacji i bez zakładania konta.

**Graj:** https://fifsok-star.github.io/stick-figure-wars/

- **Tryby:** drużynowy deathmatch, eliminacja (na rundy), przetrwanie, zdobądź flagę, bomba, battle royale do 128 graczy oraz **Podbój** (punkty A–E, bilety drużyn, klasy: szturmowiec, medyk, inżynier, snajper; oddziały po 4 osoby, odrodzenie w bazie, na punkcie albo przy koledze z oddziału).
- **Pojazdy na mapie Front** (liczba miejsc): czołg (2), transporter (5), humvee z wieżyczką (4), helikopter (4), samolot (1). `E` — wsiadanie i wysiadanie, `1`–`5` — zmiana miejsca.
- **Mapy:** Zeszyt, Karton, Tablica (małe), Segregator, Hala, Aula (labirynty), Sala gimnastyczna, Biurko, Stołówka, Szkoła, Podwórko oraz Front (olbrzymia, z pojazdami) i Miasteczko (podbój bez pojazdów).
- **Gra przez internet:** wszyscy wpisują ten sam kod pokoju albo host wysyła link z przycisku **Zaproś**. Pierwsza osoba jest hostem i startuje mecz z poczekalni, boty zajmują wolne miejsca.
- **Skrzynki i broń:** `E` otwiera skrzynkę i podnosi wybrany przedmiot — nic nie zbiera się samo.
- **Sterowanie:** tabela wyżej; na telefonie przyciski na ekranie.
- **Język** zmienisz w menu w polu „Język”.

Gracze łączą się bezpośrednio przeglądarka–przeglądarka, bez serwera gry. W niektórych sieciach (firmowych, części sieci komórkowych) połączenie może się nie udać.

### Survival
Waves keep coming until the whole team is down. Every 3rd wave brings a **boss** (bigger, much tougher, heavy machine gun, $1000 for the kill). Everyone starts with a Glock and picks a class at the start; the four Conquest classes give their gadgets on `Z`, medics revive fallen defenders (hold `E`), and you pick your class with `1–4` while dead or from the pause menu.

### Flying
- **Helicopter:** mouse turns, `W/S` forward/back, `A/D` sideways, `Space` up, `C` down; with no keys it hovers. Moving off the ground lifts it automatically and it keeps ~5 m above the ground while moving.
- **Jet:** `W/S` set the throttle (it stays where you leave it), mouse or `A/D` steer, `Space`/`C` nose up/down, LMB cannon, RMB rockets. Take off at full throttle and lift the nose at 30 m/s; below that speed the jet sinks. Gentle landings are safe.
- While piloting, a control card with speed, altitude and throttle is shown at the bottom.

### Battle royale loot
Loot crates are hidden: in building corners (sometimes upstairs) and, on maps without houses, in nooks and behind cover rather than out in the open. The minimap only shows crates close to you.
Some boxes, crates, cabinets and other furniture can be searched with `E` — inside are potions, medkits, grenades, armour, mods and sometimes a weapon. A destroyed container drops its loot. **Potions** (up to 3) are drunk with `H`: +40 health over a few seconds.

### Voice chat
Join the Discord voice channel to talk while you play: https://discord.gg/AYHFQ3yr2 (also a button in the menu, lobby and pause menu).
