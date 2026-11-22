# Changelog

## Krodin v0.4.0-beta.1

The fourth beta. The first part is a summary of what changed since `v0.3.0-beta.1`, and the complete list follows.

### Highlights

- **Windows installer.** `Krodin-Setup-0.4.0-beta.1.exe` installs Krodin for your user only, with no admin rights needed, and adds a Start menu shortcut. The zip is still available if you prefer it. The installer isn't code-signed yet, so Windows SmartScreen will warn you the first time.
- **Your data lives outside the game folder.** Settings, logs, the cache and mods now live in `%LOCALAPPDATA%\Krodin`, so updating or reinstalling no longer touches them. On first start, Krodin copies your old settings and mods from beside the exe. To keep the old layout, put an empty `portable.txt` file next to `Krodin.exe`. Settings → Gameplay → Diagnostics has an "Open logs folder" button.
- **Krunker HUD by default.** New installs start with the Krunker HUD style.
- **K/D counter.** Krunker's "Show K/D Counter" setting, off by default, which imports and exports with your Krunker settings. FPS and ping now look like Krunker's and sit beside the timer, and all Krunker-style HUD text uses the Krunker font.
- **Krunker customization.** Score popups, damage numbers, nametag styles, the throwing-knife crosshair, the progress bar and UI scale, all as in Krunker's settings.
- **Show sights.** A setting and a Toggle sights bind (unbound by default) that hide weapon sights, for custom models that break with them.
- **Asset pack.** Game files ship as one `assets.kpak` with compressed world textures. Adds Texture quality and Mip bias settings, and mod packs still work.

### Gameplay

- **Hardpoint rounds:**
  - Public Hardpoint is one round.
  - Comp and ranked Hardpoint use the lobby's rounds, 3 by default, played as best-of with No Draws.
  - A tied round gets 60 extra seconds.
  - The round counter only shows when there's more than one round.
- **Ramps:** shots pass through ramps as they do in Krunker. Bullet holes no longer float in the air above a slope, and tracers leave the barrel when you stand on one.
- **Bullet holes:** they now appear on every map object a shot hits, as in Krunker.
- **Slide timer:** it counts in double-precision milliseconds, like Krunker.
- **Net rate:** the 720 and 1000 Hz options are gone, so 520 Hz is the top. A saved rate above 520 loads as 520.

### Settings

- **Krunker settings import and export:** these now cover the per-weapon viewmodel and more keybinds, and importing then exporting keeps every setting unchanged.
- **Audio:** Krunker's HRTF and distance falloff only, with Krunker's volume sliders and sound volumes. The old spatial audio, falloff and loudness options are gone.
- **Cursor:** the Play click that enters or re-enters the game now captures the cursor straight away.

### Complete list of changes

- Keep user data outside the install folder; Windows installer
- Default the HUD style to Krunker
- Capture the cursor on the Play click that (re)enters the game
- Bullet holes on every hit map object, as in Krunker
- Krunker settings parity: per-weapon viewmodel, more keys, lossless round trip
- Slide timer in double-precision milliseconds, like Krunker
- Match Krunker's audio: HRTF and Krunker falloff only, Krunker's sliders and sound volumes
- Asset pack (assets.kpak) with compressed world textures, Texture quality and Mip bias
- Krunker customization: score popups, damage numbers, nametags, throwing crosshair, progress bar, UI scale
- Remove the 720 and 1000 Hz Net rate options; 520 Hz is the top
- Show sights setting and Toggle sights bind
- K/D counter, Krunker-style FPS and ping, and the Krunker font across the Krunker HUD
- Hardpoint: one round in public lobbies, the lobby's rounds in comp and ranked
- Shots pass through ramps, as in Krunker
- Internal: test builds compile with 4 threads

## Krodin v0.3.0-beta.1

The third beta. The first part is a summary of what changed since `v0.2.0-beta.1`, and the complete list follows.

### Highlights

- **Host comp lobbies.** The Host page creates a Krunker custom game with the Competitive preset and gives you the invite link. Hosting and the Servers page need a Krunker account login.
- **Krunker-style comp menu.** Competitive and ranked lobbies now use a copy of Krunker's comp lobby screen: the class bar, the team scores and lists, the timer and Krunker's button row, plus Servers and Mods buttons. One click picks a class, using that class's last secondary (the pistol the first time). The brush button opens the loadout.
- **Melee skins (local only).** The loadout page's Melee section opens a picker of Krunker's melee skins. The skin you pick shows in first person, in its own inspect style and sounds, in the HUD, the killfeed and your shadow. It is cosmetic and only on your screen: nothing is sent to Krunker, and other players see your real skin.
- **Quality presets.** Settings → Video → Quality preset: Potato, Low, Medium or High. Potato is for weak laptops and integrated GPUs.
- **Render distance.** Krunker's Render Distance setting, which also imports and exports with Krunker settings.
- **Fixed leaderboards.** Scores and kills now update in every Krunker mode, including Zombies.
- **New name and icon.** The game is now `Krodin.exe`, with the Krodin logo as its icon, and the download no longer has "Testing" in its name. If you pinned `krodin_client.exe` to the taskbar, or picked a GPU for it in Windows or the NVIDIA Control Panel, do that again for `Krodin.exe`. Thanks to @ylive-wav (`@_ylive` on Discord) for the logo.

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
- Name the Windows client Krodin.exe and give it the Krodin logo icon
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
