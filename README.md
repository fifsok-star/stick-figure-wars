# Stick Figure Wars

A 3D stick-figure shooter that runs in the browser — drawn in a school notebook. Play solo against bots or with friends online through a room code. No install, no account.

**Play:** https://fifsok-star.github.io/stick-figure-wars/

🇵🇱 [Polski opis niżej](#po-polsku)

## Features

- **Third- or first-person view** (switch with `V`), crouching, jumping and diving into cover.
- **Six modes:** team deathmatch, elimination (round-based), survival against waves, capture the flag, bomb (plant / defuse), and a battle royale for up to 128 players with a shrinking zone and loot crates (carry two main weapons).
- **Eleven maps:** three small ones (Notebook, Cardboard, Blackboard), three medium ones modelled in Blender (Gym with climbable bleachers, Desk, Cafeteria), two large Blender maps (School with corridor and classrooms, Schoolyard with buses, trees, containers and a shed you can walk into) and three large mazes built from giant books, rulers, pencils and binders.
- **Economy and shop:** money for kills, headshots, surviving and winning rounds. Twelve guns (incl. revolver, MP5, burst rifle, grenade launcher), a knife, weapon mods (suppressor, red dot, extended mag, grip), vest and helmet, medkit, frag, flash and smoke grenades.
- **Bots** with three difficulty levels fill empty slots and play the objectives.
- **Online play without a server:** players connect browser-to-browser. The first person in a room becomes the host, starts the match from the lobby and can send an invite link.
- Blood, bullet holes and shells that stay until the end of the round, damage numbers, scoreboard, round results with the best player and their best play, a celebration for the winning team and a crown for the battle royale winner.
- Text chat (all / team), spectator mode, team switching, settings for volume and sensitivity, touch controls for phones.
- FPS counter under the minimap (can be turned off in Settings).
- **Languages:** Polish, English, German, Ukrainian, French.

## Controls

| Key | Action |
|---|---|
| `W` `A` `S` `D` | Move |
| Mouse | Aim |
| Left click | Shoot |
| Right click | Aim down sights (every gun; sniper scope, stronger zoom with a red dot) |
| `Space` | Jump |
| `C` | Crouch |
| `Shift` | Dive to cover |
| `R` | Reload |
| `1` `2` `Q` / wheel | Switch weapon |
| `3` `4` `5` | Choose grenade (frag / flash / smoke) |
| `G` | Throw grenade |
| `E` | Open a crate / pick up a weapon or item (nothing is picked up automatically) |
| `F` / middle mouse button | Knife |
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
- Weapon, grenade, helmet, vest and small-map props were modelled in [Blender](https://www.blender.org/) and are embedded as glTF.

## Hosting

The game is served by GitHub Pages from the `main` branch. To host it elsewhere, upload `index.html` to any static hosting.

---

## Po polsku

Strzelanka 3D z patyczakami w przeglądarce, narysowana w zeszycie. Grasz sam z botami albo ze znajomymi przez kod pokoju — bez instalacji i bez zakładania konta.

**Graj:** https://fifsok-star.github.io/stick-figure-wars/

- **Tryby:** drużynowy deathmatch, eliminacja (na rundy), przetrwanie, zdobądź flagę, bomba, battle royale do 50 graczy.
- **Mapy:** Zeszyt, Karton, Tablica (małe) oraz Segregator, Hala, Aula (duże labirynty z wysokich murów).
- **Gra przez internet:** wszyscy wpisują ten sam kod pokoju albo host wysyła link z przycisku **Zaproś**. Pierwsza osoba jest hostem i startuje mecz z poczekalni, boty zajmują wolne miejsca.
- **Skrzynki i broń:** `E` otwiera skrzynkę i podnosi wybrany przedmiot — nic nie zbiera się samo.
- **Sterowanie:** tabela wyżej; na telefonie przyciski na ekranie.
- **Język** zmienisz w menu w polu „Język”.

Gracze łączą się bezpośrednio przeglądarka–przeglądarka, bez serwera gry. W niektórych sieciach (firmowych, części sieci komórkowych) połączenie może się nie udać.
