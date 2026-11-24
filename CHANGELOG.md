# Changelog

## Krodin v0.5.2-beta.1

A patch on top of `v0.5.1-beta.1`, with new in-game UI from Krunker and a few fixes.

### In game

- **Player List.** Press Alt, Krunker's default key, to open Krunker's Player List. You can rebind it under Settings > Key binds > Interface.
  - It shows everyone in the lobby with their ping, clan tag, a star for the host and a search box.
  - From the list you can start a vote kick, under Krunker's rules.
- **Vote kick and forfeit.** Krunker's vote kick box, with the Vote kick [Yes] / [No] keys (1 and 2 by default). Type /ff in chat for the forfeit vote.
- **Objective markers.** In Hardpoint, the active objective is marked on screen, with "Next" shown near the end of each rotation, as in Krunker. Krunker's Objective Opacity and ADS Objective Opacity settings (Settings > HUD) control them.
- **Game messages.** Krunker's centre banners appear for:
  - the mode name when warmup ends;
  - Overtime and +60 Seconds;
  - Switching Sides;
  - who is in the lead.

  The server's status line ("waiting for players" and similar) shows too.
- **Reload prompt.** "[R] Reload" appears when your magazine is empty, using your reload key.
- **Connection warning.** A small warning under the FPS and ping display shows when your ping is high (150 ms and up), when packets stop arriving, or when the connection is lost. This is Krodin's own design. Krunker only colours the ping number.
- **Chat command replies.** Replies to chat commands such as /c now show in chat.

### Settings

- **Settings profiles.** Keep more than one set of game settings and switch between them from the top of Settings. Display and graphics settings are not part of profiles.
- **Flick clamp removed.** The Mouse flick and Flick clamp settings are gone. Values imported from Krunker are still kept, so exporting writes them back unchanged.

### Fixes

- **Local Practice after a lobby.** Leaving a lobby and starting Local Practice no longer keeps you on the lobby's map; every map can be picked again.

If you said yes to automatic updates, Krodin offers this update the next time you start it.

### Complete list of changes

- Player List window and its bind (Alt)
- Vote kick and forfeit votes, with the Vote kick [Yes] / [No] binds
- Objective markers in Hardpoint, with Objective Opacity and ADS Objective Opacity
- Krunker's game messages, the reload prompt and a connection warning
- Show chat command replies in chat
- Settings profiles
- Remove the Mouse flick and Flick clamp settings
- Restore every Local Practice map after leaving a lobby

## Krodin v0.5.1-beta.1

A very small patch on top of `v0.5.0-beta.1`.

### Fixes

- **No more console window.** Krodin no longer opens a black console window next to the game. Logs are still written to the logs folder (Settings > Gameplay > Open logs folder).

If you are on 0.5.0 and said yes to automatic updates, Krodin offers this update the next time you start it.

### Complete list of changes

- Build Krodin.exe without a console window

## Krodin v0.5.0-beta.1

A feature release on top of `v0.4.2-beta.1`. The first part covers what is new in 0.5.0, then a recap of what 0.4.1 and 0.4.2 added since 0.4.0, then the complete list.

### Updates

- **Krodin can now update itself.** On first open it asks whether to check for updates automatically. If you say yes, it offers each new release when you start the game, patches included, and installs it for you. You can change this any time in Settings > Gameplay, which also has a "Check for updates" button.
- Every download is checked against its published SHA-256 before it is installed.

### Matches

- **Map voting.** At the end of a match you can vote for the next map from a set of map cards, as in Krunker. The counts update live, and you can change your vote.
- **Narrator countdown and match-found sound.** The "5, 4, 3, 2, 1" narrator and the ranked match-found sound now play. They were missing from earlier downloads, together with the melee skin equip sound.
- **Sawed Off** holds 2 shells, not 3.

### Death screen

- **Rebuilt to match Krunker's**: the same layout, the killer's skins and player card, the art, the background blur and the shadows.

### Settings

- **Changes apply instantly.** There is no Save button any more, just Close.
- **Editing a value keeps its text.** Clicking a field that says 0.5 no longer makes you retype it.
- **Sliders move in Krunker's steps** (for example FOV by 5, volume by 0.01). A value you type keeps its full precision.
- **Image hitmarkers.** Settings > Hitmarker > Hitmarker image takes a link or a local file, and works like Krunker's custom hitmarker.
- **Show Movement Speed.** Krunker's speed display (current and max) with its position, scale, opacity and colour settings, under Settings > HUD.

### Maps

- **Breakable objects** can be destroyed and come back, as in Krunker (Site, Kanji, Lagoon).
- Every hosted model the maps use is now drawn.

### Sound

- **Long Nuke and siren sounds from mods** now fade out after a few seconds instead of playing to the end.

### Since 0.4.0 (from 0.4.1 and 0.4.2)

- **No login needed to join.** Invite links and the Servers page join you as a guest when you aren't logged in. Hosting still needs a Krunker account.
- **Killstreaks.** Streak slot binds (1, 2 and 3 by default) call in earned streaks, including the Nuke with Krunker's siren, blast and flash.
- **End screen.** Chat works there, each player shows their last class icon, Escape switches between the results and the menu, and Krunker's current Victory and "ENDED" titles are used.
- **Clan tags** on nametags, the leaderboard, the scoreboard and the end tables, in Krunker's format.
- **Maps.** Lumber's trees, Piazza's arches, Eterno Simulator's hosted textures, Kanji's launch pads and light cones, and sky domes everywhere.
- **Mod sounds** that were silent now play, including MP3Gain-tagged files and AAC or Ogg files renamed to `.mp3`.
- **Fixes.** The missing K/D and end-screen icons are back, your account name updates right after joining, and the FPS counter counts above 4096.

### Complete list of changes

- Auto-update: ask on first open, then offer and install every newer release
- Vote for the next map at the end of a match
- Death screen parity with Krunker: layout, skins, player cards, art, blur and shadows
- Settings apply instantly; fields keep their text; sliders follow Krunker's steps
- Image hitmarkers
- Show Movement Speed with its settings
- Include the narrator countdown, ranked match-found and melee equip sounds in the download
- Cap long Nuke and siren sounds from mods
- Map objects: breakable triggers, every hosted model, destroy and respawn
- Sawed Off ammo is 2
- Log memory use every 30 seconds and after each map load

## Krodin v0.4.2-beta.1

A patch release on top of `v0.4.1-beta.1`. The first part is a summary, and the complete list follows.

### Maps

- **Lumber:** the missing pine trees are back, the stray "ghost" models are gone, and the invisible box that blocked one tree spot is now the tree's real trunk hitbox. The sky dome is drawn.
- **Eterno Simulator and Piazza:** surfaces that use Krunker's hosted textures now show them. Piazza's arches are drawn as open arches instead of solid disks, and objects that are invisible in Krunker are hidden.
- **Kanji:** launch pads and light cones are drawn.
- **Lush** and the other maps benefit from the same fixes: glowing surfaces, see-through materials, cylinders and sky domes.

The map files were already current. Krodin had been ignoring or misreading several of Krunker's map object properties. The download is a few MB larger because it now includes the hosted models and textures these maps use.

### Mods

- **Hit sounds that were silent now play.** Sound files edited with MP3Gain carry an extra tag that Krodin's decoder choked on (the idrc mod's hit sound).
- **Mod sounds in other formats now play.** Many mods rename AAC or Ogg Vorbis files to `.mp3`. Krodin now checks what each file really is, like the browser does. AAC uses the decoder built into Windows. A sound Krodin still cannot play is named in the log.

### HUD and end screen

- **Clan tags.** Players' clans show after their names on nametags, the top-right leaderboard, the Tab scoreboard and the end-of-match tables, in Krunker's format. Krunker's special clans are gold. In ranked, clans stay hidden until warmup ends, as in Krunker.
- **Escape on the end screen** now switches between the results and the menu as many times as you like.
- **New end titles.** Krunker's current Victory art, and its "ENDED" title for modes with no winner.
- **FPS counter.** It no longer stops at 4096 in small windows.

### Complete list of changes

- Use Krunker's current Victory art and add its Ended title
- Escape toggles between the end screen and the menu
- Map parity: hosted art, visibility, arches, sky domes, launch pads (Lumber, Piazza, Eterno Simulator, Lush, Kanji)
- Play mod sounds that end with an APE tag
- Play mod sounds that are Ogg Vorbis or AAC renamed to .mp3
- Show clan tags on nametags, leaderboard, scoreboard and end tables
- Count FPS above 4096

## Krodin v0.4.1-beta.1

A hotfix and feature update for `v0.4.0-beta.1`. The first part is a summary, and the complete list follows.

### Fixes

- **Missing HUD icons.** The K/D counter icons and the end screen's victory, defeat and draw titles were missing from the 0.4.0 installer and zip. They're back.
- **Account name after joining.** After switching lobbies you could stay `Guest_<number>` until your first death. Krunker often confirms your login just after you spawn and then renames you, and Krodin now applies that rename straight away.

### New

- **No login needed to join.** If you aren't logged in, joining any lobby from an invite link or the Servers page joins you as a guest. The "Play as guest" button is gone and the Servers page is open to everyone. Hosting a game still needs a Krunker account. A saved login that has expired is renewed instead of falling back to a guest.
- **Killstreaks.** Streak slot 1, 2 and 3 binds (keys 1, 2 and 3 by default) call in your earned streaks, as in Krunker. They're in Settings → Controls and import and export with your Krunker settings. Earned streaks show beside the ammo box, and the Nuke plays Krunker's siren, blast and white flash. For now slot 3 is always the Nuke and the boxes show the streak's name instead of its image. Krunker only gives Nukes to logged-in accounts.
- **End screen chat.** You can open chat and keep talking on the end screen.
- **Class icons on the end screen.** Each player's circle on the end-screen leaderboard shows the class they last played.

### Complete list of changes

- Include the K/D counter and end-screen title icons in packaged builds
- Chat on the end screen
- End-screen leaderboard: each player's last-played class icon
- Join as a guest when not logged in; remove the Play as guest button
- Killstreak call-ins: Streak slot binds, the streak holder and the Nuke
- Rename players from Krunker's name update instead of waiting for a respawn

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
