# Changelog

## Krodin v0.3.0-beta.1

The third beta. The first part is a summary of what changed since `v0.2.0-beta.1`, and the complete list follows.

### Highlights

- **Host comp lobbies.** The Host page creates a Krunker custom game with the Competitive preset and gives you the invite link. Hosting and the Servers page need a Krunker account login.
- **Krunker-style comp menu.** Competitive and ranked lobbies now use a copy of Krunker's comp lobby screen: the class bar, the team scores and lists, the timer and Krunker's button row, plus Servers and Mods buttons. One click picks a class, using that class's last secondary (the pistol the first time). The brush button opens the loadout.
- **Melee skins (local only).** The loadout page's Melee section opens a picker of Krunker's melee skins. The skin you pick shows in first person, in its own inspect style and sounds, in the HUD, the killfeed and your shadow. It is cosmetic and only on your screen: nothing is sent to Krunker, and other players see your real skin.
- **Quality presets.** Settings → Video → Quality preset: Potato, Low, Medium or High. Potato is for weak laptops and integrated GPUs.
- **Render distance.** Krunker's Render Distance setting, which also imports and exports with Krunker settings.
- **Fixed leaderboards.** Scores and kills now update in every Krunker mode, including Zombies.

### Joining and hosting

- **Hosting:** creates the lobby on the same connection, solves Krunker's lobby check by itself, and stops with a clear message if Krunker's verification window is signed in to a different account or as a guest.
- **Regions:** joins and hosting now send the lobby's own region (or the one you chose), which fixes joins that were sent to the wrong region and asked for a verification they didn't need.
- **Join errors:** a failed join shows Krunker's reason in plain words, for example "Couldn't join: That lobby is full", instead of the raw server reply.

### Menus and settings

- **Comp lobby screen:**
  - Full classes are greyed out with a lock, and so is your own class.
  - Enemy classes show as "???".
  - "Waiting for players" shows above the button row.
  - Icons use Material Icons, the same icon font Krunker uses.
  - The orange focus ring only shows when you use the keyboard (Tab or arrows), never after a click.
- **Melee picker:** searchable, with a preview for each skin. Animated skins are not included yet.
- **Render scale warning:** setting Render scale above 100% shows a 5-second notice, because it costs a lot of FPS.

### Graphics and performance

- **Vulkan fallback notice:** if Vulkan can't start, Krodin uses OpenGL as before, and now tells you why (no driver, a GPU that only has an older Vulkan, missing features). A driver update may fix it, and Krodin tries Vulkan again on every start.
- **Smoother mouse input:** the cursor is pinned while you play, so moving the mouse no longer causes slow frames. Aiming is unchanged.
- **Smaller download:** Krunker's configs and the bundled maps ship as compact binary packs.

### Diagnostics

- The log records why Vulkan couldn't start, and failed joins log Krunker's full reply.

### Complete list of changes

- Ship Krunker configs and bundled maps as compact binary packs
- Warn when Render scale is above 100%
- Leaderboard: stats for every Krunker mode
- Pin the cursor while playing so event polls stay cheap
- Tell the player when Vulkan can't start (OpenGL fallback notice)
- Leaderboard: Zombies sends points, zombies, downs and damage
- Quality presets (Potato, Low, Medium, High) and Krunker's Render Distance
- Join errors: show Krunker's message, not the HTTP payload
- Krunker-style comp/ranked lobby menu and local melee skins
- Host Krunker custom games (Competitive preset); Servers and Host need a login
- Internal: hold the embedded config pack through a pointer, opt-in Tracy profiler instrumentation, and a log analyser for tester logs

## Krodin v0.2.0-beta.1

The second beta. The first part is a summary of what changed since `v0.1.0-beta.1`, and the complete list follows.

### Highlights

- **Server browser.** A new Servers page lists Krunker's public lobbies, with filters, sorting and a ping for each region. Click a lobby to join it. Only lobbies on maps Krodin can load are listed.
- **Mod explorer.** A new Mods page searches Krunker's public mod packs, shows their thumbnails, and installs them. A pack's textures and sounds apply in game without a restart.
- **NVIDIA Reflex.** Settings → Video → NVIDIA Reflex: Off, On, or On + Boost. It works on NVIDIA GPUs with the Vulkan renderer.
- **Render scale.** This is Krunker's "Resolution" setting. It draws the 3D world at fewer pixels while the HUD and menus stay sharp, which helps low-end PCs and laptops.
- **Throwing knife.** The throwing-knife crosshair, plus a charge bar shared by the knife, the Infiltrator's Charge Rifle and the Crossbow. A thrown knife now leaves your hands, flies, and sticks into walls.
- **Kill sounds.** Krunker's headshot kill sound, and the kill sounds of weapon skins.
- **Chat killfeed.** Krunker's "Use Classic io Scoreboard" setting puts kill lines in the chat box instead of the top-right killfeed. In the Krunker HUD style, the chat now looks like Krunker's own chat box.
- **Spawn fixes.** You face the right way on spawn, and a stray shot on spawn is fixed.

### Gameplay and Krunker parity

- **Spawn direction:** on spawn and respawn you face the direction the server gives, instead of a random one.
- **Stray shot on spawn:** held mouse buttons are reset on spawn the way Krunker's `resetKeys` does it. You no longer fire a stray bullet when you spawn.
- **Overlapping players:** players are hidden while your camera is inside them, as in Krunker.
- **Throwing knife**:
  - Krunker's throwing crosshair while a throwable knife is held and fully aimed.
  - One charge bar for the knife throw, the Charge Rifle and the Crossbow.
  - The thrown knife leaves your hands, flies with Krunker's speed, gravity and spin, and sticks into walls.
- **Kill sounds:** `headshot_0` plays on your headshot kills, in live lobbies, Local Practice and Krodin servers. Weapon skins with their own kill sound play it in live lobbies. As in Krunker, a plain kill without such a skin is silent.
- **FFA HUD:** team scores and round wins are hidden in free-for-all modes, in both HUD styles.
- **Chat killfeed:** Settings → HUD → Killfeed → "Use Classic io Scoreboard".
  - Kill lines go to the chat box, and the top-right killfeed is hidden. Each line shows the killer, the weapon picture, wallbang and headshot badges, and the victim.
  - Lines follow the chat's timer, height, opacity, background opacity and text outline settings. The setting imports and exports with Krunker's `oldScoreboard` key.
  - In the Krunker HUD style, the whole chat uses Krunker's chat box. That means one dark box at the bottom left, Krunker's font, and Krunker's input row with a Team / All label.

### Menus and settings

- **Servers page**: Krunker's public lobbies with filters, sorting, a ping for each region, and joining through the invite path.
  - Lobbies on custom maps, or on maps Krodin has no data for, are hidden.
- **Mods page**: search, thumbnails, download and install. A pack's textures and sounds apply in game without a restart.
- **Key binds:**
  - New **Primary weapon** (T) and **Toggle weapon visibility** (unbound) binds, matching Krunker's.
  - Each key bind has a **Reset** button that restores that one bind to its default.
  - Importing Krunker settings warns you when Fire or Aim ends up unbound. Krunker's export leaves out binds still at their defaults, so an import can clear them.
- **Render scale** (Krunker's "Resolution"), for both OpenGL and Vulkan.
- **Motion blur** with a strength slider. This is Krodin's own setting and is off by default.

### Graphics and performance

- **NVIDIA Reflex** (Vulkan): Off (default), On, or On + Boost.
- **Intel UHD and minimised-window hangs fixed:** OpenGL never waits forever on GPU frame fences or timer queries. Rendering pauses while the window is minimised, which also fixes the GPU resets some players hit.
- **Fonts:** the font fallback searches more fonts and handles emoji sequences. Characters that still can't be drawn are logged, so they can be fixed.

### Diagnostics

- The log records the build version and commit at startup and on every join, so a log always says which build wrote it.

### Complete list of changes

- Log the build version and commit at startup and on every join
- Add Primary weapon and Toggle weapon visibility binds
- Add an in-game server browser for Krunker's public lobbies
- Mod explorer: search, install and apply Krunker mod packs
- Log missing glyphs, widen the font fallback, handle emoji sequences
- Motion blur with a strength slider (Krodin's own, default off)
- Never block forever on GL frame fences and timer queries (Intel UHD 620 hang)
- Server browser: list only lobbies on maps Krodin can load
- Hide team scores and round wins in FFA HUDs
- Render scale (Krunker's Resolution setting)
- Warn when a settings import leaves Fire or Aim unbound
- Add a Reset button to each key bind
- Add NVIDIA Reflex low-latency mode (Vulkan)
- Hide players the camera is inside (Krunker back-face culling parity)
- Fix stray shot on spawn: reset held mouse buttons like Krunker's resetKeys
- Face the server's spawn direction on (re)spawn
- Throwing-knife crosshair and weapon charge bar (knife, Charge Rifle, Crossbow)
- Play Krunker's headshot kill sound on local kills
- Add Krunker's chat killfeed (Use Classic io Scoreboard)

## Krodin v0.1.0-beta.1

The first beta. Download it from the Releases page.
