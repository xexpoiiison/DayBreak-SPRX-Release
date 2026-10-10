# DayBreak V1.1.1 – BO3 Zombies SPRX (PS4 / PS5)

**Game:** Black Ops III – CUSA02290 (V1.33)
**Needs:** GoldHEN (PS4) or NexHEN (PS5)

## Fixed in V1.1.1
- **PS5 / NexHEN autoload:** DayBreak didn't show up when set to `?autoload=true` in NexHEN (no load box, no menu), but worked when loaded from the Plugin Loader at the main menu. NexHEN autoload injects the moment the game starts, before BO3 is ready, and DayBreak gave up. It now waits for the main menu and hooks in then, the same as the Plugin Loader. It also keeps retrying its startup and controller hook instead of giving up, and shows the load box within 20 seconds on the main menu even if the X on "Press X to start" was missed.
- **Clearer messages:** if another plugin already hooked BO3 or took over the controller, DayBreak now says so instead of "game version doesn't match".
- PS4 with GoldHEN loads the same as before.

## Install (PS4 – GoldHEN)
1. Download `DayBreak.sprx`
2. With FTP, copy it to:
   `/data/GoldHEN/plugins/DayBreak.sprx`
3. Open `/data/GoldHEN/plugins.ini` (create it if it isn't there) and add:
   ```ini
   [CUSA02290]
   /data/GoldHEN/plugins/DayBreak.sprx
   ```
4. Restart BO3.

## Install (PS5 – NexHEN)
1. Download `DayBreak.sprx`
2. With FTP, copy it to:
   `/data/nexHEN/plugins/DayBreak.sprx`
3. In NexHEN's `plugins.ini`, add:
   ```ini
   [CUSA02290]
   /data/nexHEN/plugins/DayBreak.sprx?autoload=true
   ```
   Or leave off `?autoload=true` and enable it through NexHEN's Plugin Loader.
4. Start BO3.

## Use
- After "Press X to start" it asks **"Would you like to load DayBreak ZM SPRX?"** Pick **Yes**.
- **L1 + R1** opens the menu (Pre Game Menu on the main menu, Full Menu in a match).
- **D-pad** moves, **X** selects, **O** goes back, **Left / Right** changes values.
- **Verified players:** hold **L1** and tap **R1** (or **L1 + Triangle**) to open their menu.

## Coming in V1.2
- **Stats for all modes** (Multiplayer, Campaign and Zombies), done right in the SPRX, no GSC injection: level, prestige, unlocks, liquid divinium, clan tag and more.

## Problems
- Nothing shows up: check the path and `plugins.ini`, and make sure your game is CUSA02290 on the latest patch.
- Running other BO3 plugins? Try DayBreak by itself first, and only list it once in `plugins.ini`.
- Questions: Discord / X **@xexpoiiison**

Created By: XeX Poiiison
