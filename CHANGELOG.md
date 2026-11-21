# Changelog

## Krodin v0.2.0-beta.1

The second beta. Since `v0.1.0-beta.1` there are 19 merged pull requests. The first part is a summary, and the complete list follows.

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

- **Spawn direction:** on spawn and respawn you face the direction the server gives, instead of a random one (#137).
- **Stray shot on spawn:** held mouse buttons are reset on spawn the way Krunker's `resetKeys` does it. You no longer fire a stray bullet when you spawn (#136).
- **Overlapping players:** players are hidden while your camera is inside them, as in Krunker (#135).
- **Throwing knife** (#140):
  - Krunker's throwing crosshair while a throwable knife is held and fully aimed.
  - One charge bar for the knife throw, the Charge Rifle and the Crossbow.
  - The thrown knife leaves your hands, flies with Krunker's speed, gravity and spin, and sticks into walls.
- **Kill sounds:** `headshot_0` plays on your headshot kills, in live lobbies, Local Practice and Krodin servers. Weapon skins with their own kill sound play it in live lobbies. As in Krunker, a plain kill without such a skin is silent (#143).
- **FFA HUD:** team scores and round wins are hidden in free-for-all modes, in both HUD styles (#127).
- **Chat killfeed:** Settings → HUD → Killfeed → "Use Classic io Scoreboard" (#144).
  - Kill lines go to the chat box, and the top-right killfeed is hidden. Each line shows the killer, the weapon picture, wallbang and headshot badges, and the victim.
  - Lines follow the chat's timer, height, opacity, background opacity and text outline settings. The setting imports and exports with Krunker's `oldScoreboard` key.
  - In the Krunker HUD style, the whole chat uses Krunker's chat box. That means one dark box at the bottom left, Krunker's font, and Krunker's input row with a Team / All label.

### Menus and settings

- **Servers page** (#119): Krunker's public lobbies with filters, sorting, a ping for each region, and joining through the invite path.
  - Lobbies on custom maps, or on maps Krodin has no data for, are hidden (#126).
- **Mods page** (#120): search, thumbnails, download and install. A pack's textures and sounds apply in game without a restart.
- **Key binds:**
  - New **Primary weapon** (T) and **Toggle weapon visibility** (unbound) binds, matching Krunker's (#118).
  - Each key bind has a **Reset** button that restores that one bind to its default (#133).
  - Importing Krunker settings warns you when Fire or Aim ends up unbound (#129). Krunker's export leaves out binds still at their defaults, so an import can clear them.
- **Render scale** (Krunker's "Resolution"), for both OpenGL and Vulkan (#128).
- **Motion blur** with a strength slider. This is Krodin's own setting and is off by default (#122).

### Graphics and performance

- **NVIDIA Reflex** (Vulkan): Off (default), On, or On + Boost (#134).
- **Intel UHD and minimised-window hangs fixed:** OpenGL never waits forever on GPU frame fences or timer queries. Rendering pauses while the window is minimised, which also fixes the GPU resets some players hit (#123).
- **Fonts:** the font fallback searches more fonts and handles emoji sequences. Characters that still can't be drawn are logged, so they can be fixed (#121).

### Diagnostics

- The log records the build version and commit at startup and on every join, so a log always says which build wrote it (#117).

### Not in this release yet

These are in testing and will follow in a later update:
- In-game game hosting
- Cursor pinning for smoother mouse event polling
- Tracy profiler support
- Compact config and map files
- Linux packaging fixes, including the "CPU ISA level lower than required" error on some Intel CPUs

### Complete list of pull requests

- #117 Log the build version and commit at startup and on every join
- #118 Add Primary weapon and Toggle weapon visibility binds
- #119 Add an in-game server browser for Krunker's public lobbies
- #120 Mod explorer: search, install and apply Krunker mod packs
- #121 Log missing glyphs, widen the font fallback, handle emoji sequences
- #122 Motion blur with a strength slider (Krodin's own, default off)
- #123 Never block forever on GL frame fences and timer queries (Intel UHD 620 hang)
- #126 Server browser: list only lobbies on maps Krodin can load
- #127 Hide team scores and round wins in FFA HUDs
- #128 Render scale (Krunker's Resolution setting)
- #129 Warn when a settings import leaves Fire or Aim unbound
- #133 Add a Reset button to each key bind
- #134 Add NVIDIA Reflex low-latency mode (Vulkan)
- #135 Hide players the camera is inside (Krunker back-face culling parity)
- #136 Fix stray shot on spawn: reset held mouse buttons like Krunker's resetKeys
- #137 Face the server's spawn direction on (re)spawn
- #140 Throwing-knife crosshair and weapon charge bar (knife, Charge Rifle, Crossbow)
- #143 Play Krunker's headshot kill sound on local kills
- #144 Add Krunker's chat killfeed (Use Classic io Scoreboard)

## Krodin v0.1.0-beta.1

The first beta. Download it from the Releases page.
