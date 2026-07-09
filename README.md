# Mulligan Coach

A real-time **mulligan helper for MTG Arena Limited** (Draft & Sealed). 
It watches your Arena log, reads your opening hand and
deck, and shows a Keep-vs-Mulligan verdict — with win-rate estimates —
right next to the mulligan prompt.

> **Read-only. Nothing about your games ever leaves your PC.** Mulligan
> Coach only *reads* your local Arena log file. It never touches the game
> client, never reads game memory, and never uploads anything.

*(This repo hosts the downloads + auto-update data. The app itself is a
small Windows overlay.)*

---

## Download & install

1. Go to the [**latest release**](https://github.com/vonbeschwitz/mulligan_coach_data/releases/tag/exe-latest)
   and download **`MulliganCoachSetup.exe`**.
2. Run it. It installs **per-user — no admin prompt** — and adds a
   Start-menu entry you can uninstall any time. (Updating later is the
   same: download the new installer and run it; it upgrades in place.)

### "Windows protected your PC" (SmartScreen)

The installer is **not code-signed yet**, so Windows SmartScreen shows a
blue warning on first run. This is expected for a new indie app. To
proceed:

> Click **More info** → **Run anyway**.

If your antivirus flags it, that's an unsigned-binary false positive; a
**VirusTotal scan** is linked on the
[download page](https://github.com/vonbeschwitz/mulligan_coach_data/releases/tag/exe-latest)
so you can check for yourself.

## First run — one Arena setting

Mulligan Coach needs Arena's detailed logging:

> In MTG Arena: **Options → Account → enable "Detailed Logs (Plugin
> Support)"**, then restart Arena.

The app's setup wizard checks this for you and walks you through it if
it's off. Once enabled, open a Limited match — the overlay appears at the
mulligan screen (Alt+E to minimize/maximize). It hides itself whenever Arena isn't running and lives in
your system tray (right-click for settings, feedback, and quit).

## Which formats?

Built and trained for **Premier and Traditional Draft**. Sealed works too, but 
the model is trained on draft data, so treat its numbers there as approximate. 

## Updates

- **Card data & model** auto-update in the background (pull-only from this
  repo).
- **The app itself** notifies you when a new build is available and links
  the download. It never silently replaces itself.

## Feedback & bugs

Use **"Send feedback…"** in the app (tray or ⚙ menu), or open an issue
here — bug-report and feature-request templates are provided.

---

## FAQ

**Is this allowed?**
It only reads the local log file Arena already writes — the same approach
other community tools (17Lands, Untapped.gg) use, and the line Wizards
tolerates. It does not read game memory, modify the client, or automate
anything.

**What leaves my computer?**
Nothing about your games. The app *downloads* card data/model updates from
this public repo; it never *uploads* your logs, hands, or results.

**Why does Windows / my antivirus warn me?**
The binary isn't code-signed yet. Unsigned apps trigger SmartScreen + occasional anti-virus false
positives. See the install steps above and the per-release VirusTotal
link.

**Does it tell me which card to put on the bottom?**
Not yet — only keep vs. mulligan.

---

## Credits & attribution

- Card statistics derived from **[17Lands](https://www.17lands.com)**
  public data (CC BY 4.0). *17Lands does not endorse this tool.*
- Card data from **[Scryfall](https://scryfall.com)**.
- Arena card identifiers from **[MTGJSON](https://mtgjson.com)**.

## Legal

Mulligan Coach is unofficial Fan Content permitted under the Fan Content
Policy. Not approved/endorsed by Wizards. Portions of the materials used
are property of Wizards of the Coast. ©Wizards of the Coast LLC.

Free to use. Contact: bastian.vonbeschwitz@gmail.com — for any takedown or data-use concern,
email and it will be addressed promptly.
