# FAQ

Answers to the questions we hear most. Can't find yours? See the [Help centre](/wiki/Help_centre).

## What is somtum.fun? {id=what-is-somtum-fun}

somtum.fun is a fan-run private server for the rhythm game osu!. It has its own accounts, rankings, beatmaps and community. It is not affiliated with ppy Pty Ltd, and your osu! account and scores on osu.ppy.sh aren't shared with it. It runs on its own server software, not bancho.py or g0v0: see [Why somtum.fun?](/wiki/Why_somtum.fun)

## How do I connect? {id=how-do-i-connect}

All downloads are on the [download page](/home/download). The easiest way is the **Somtum Launcher**: it installs and updates everything below and starts the game for you.

- **TumThai** is our version of osu!lazer, for Windows, Linux, macOS and Android. Install it (or unzip the portable version) and sign in. It updates itself.
- **osu!(stable):** start your osu!(stable) with the **Somtum Patcher** (or from the Somtum Launcher).
- **Old clients (2008 to 2015):** download one of our rebuilt legacy clients, unzip it anywhere and run `osu!.exe`. Keep `pkms.dll` (our anti-cheat) next to `osu!.exe`: without it your scores aren't submitted. They need Windows and .NET Framework 3.5 (a few 2015 builds need .NET Framework 4). Can't find the build you want? Ask for it in our [Discord server](https://discord.gg/U6Ztb3mRyz) or on the [forum](/community/forums/4).

**Only these submit scores.** From October 2026, our anti-cheat checks every client that plays here, and only the Somtum Launcher, the Somtum Patcher, TumThai and our rebuilt legacy clients pass. You can still connect other ways, and log in, chat, play and join multiplayer, but **your scores won't be submitted**, because the anti-cheat can't verify those clients:

1. **`-devserver`:** osu!(stable) started with `-devserver somtum.fun` (without the Somtum Patcher) still connects to somtum.fun, but its scores aren't submitted.
2. **Your own modded clients:** a client you patched or built yourself (the way Titanic's clients connect to Titanic, for example) can connect to somtum.fun too, but its scores aren't submitted either. The same goes for other lazer clients pointed at somtum.fun (such as g0v0's, or osu!lazer with LazerAuthlibInjection). Their settings are in [Connecting with another lazer client](#other-lazer-clients).

**Old clients (2008 to 2015) are different:** only our rebuilt legacy clients can log in. An unmodified old build (with the hook or not), or one you modded or rebuilt yourself, gets ["This old osu! build can't play on somtum.fun as it is"](#error-old-build) and can't connect.

This keeps the rankings fair for everyone. If your setup can't run one of ours, tell us in [Discord](https://discord.gg/U6Ztb3mRyz).

## TumThai: bringing your osu!lazer beatmaps and replays {id=tumthai-import}

TumThai can use the beatmaps, skins and replays you already have in osu!lazer. In TumThai, open **Settings → Maintenance → Change folder location** and choose your osu!lazer folder:

- Windows: `%AppData%\osu`
- Linux: `~/.local/share/osu`
- macOS: `~/Library/Application Support/osu`

TumThai then reads that folder instead of its own, so close osu!lazer first. To move back, choose another folder the same way.

## Connecting with another lazer client {id=other-lazer-clients}

Using g0v0's client, another lazer-based client, or osu!lazer with LazerAuthlibInjection? Fill in these settings:

| Setting | Value |
|---|---|
| API URL | `https://osu.somtum.fun` |
| Website URL | `https://osu.somtum.fun` |
| Client ID | `5` |
| Client Secret | `FGc9GAtyHzeQDshWP5Ah7dega8hJACAJpQtw6OXk` |
| Spectator URL | `https://spectator.somtum.fun/spectator` |
| Multiplayer URL | `https://spectator.somtum.fun/multiplayer` |
| Metadata URL | `https://spectator.somtum.fun/metadata` |
| Beatmap Submission Service URL | `https://osu.somtum.fun/beatmap-submission` |
| Non-g0v0 server | **On** (checked) |

You can log in, chat, spectate and play multiplayer, but **score submission never works** on these clients. For your scores to count, play on [TumThai](#how-do-i-connect).

## My antivirus or Windows warns about your downloads {id=antivirus}

Our downloads aren't code-signed: signing them would cost us upwards of 300€ a year, which is too much for a free community server. So Windows may show "Windows protected your PC" (click **More info**, then **Run anyway**), and antiviruses may block or remove the Somtum Launcher, the Somtum Patcher, `pkms.dll`, TumThai or our old clients by mistake. Add an exception for their folders: see [My antivirus or Windows blocks a download](/wiki/Help_centre/Common_problems#antivirus) for the steps. Only do this for files from our [download page](/home/download).

## How do I make an account? {id=registration}

Make it in the game: open TumThai or osu!(stable) on somtum.fun and register there, not on the website. Then sign in to this website with the same name and password.

New here and not set up yet? You can also make your account from osu!(stable) started with `-devserver somtum.fun`, or from another lazer client pointed at somtum.fun. Keep in mind that **you can't submit any scores** until you play on our official builds: TumThai, or osu!(stable) through the Somtum Launcher (or the Somtum Patcher), or one of our legacy clients. See [How do I connect?](#how-do-i-connect)

You can have **one account**. Sign-ups through a VPN, proxy, Tor or a hosting network are blocked, and each network can make one account a day. If that stops you from signing up honestly, email [accounts@somtum.fun](mailto:accounts@somtum.fun).

## Is it free? {id=is-it-free}

Yes. Supporter tags are optional and help pay for the server.

## Relax and Autopilot {id=relax-and-autopilot}

Relax and Autopilot have their own leaderboards, rankings and pp, separate from normal play, in both TumThai and osu!(stable). Choose them on the rankings page and on beatmap leaderboards. Their pp is worked out with other calculators: see [Performance points](/wiki/Performance_points).

## How do I link my Discord account? {id=discord-link}

Link it once, either way: in your [account settings](/home/account/edit#connections) under **Connections**, or with `/link` on our Discord bot (it gives you a code to send to LimeBot). Both make the same link, so **if you linked Discord on the website, you don't need `/link` too**. See [Linking Discord](/wiki/Map_of_the_day#linking-discord).

## What are the daily challenge and the map of the day? {id=daily}

The [daily challenge](/wiki/Daily_challenge) is a new map every day in a room in TumThai, ranked by score. The [map of the day](/wiki/Map_of_the_day) is our Discord bot's daily map: the best pass by pp wins a Discord role for a week. [How they differ](/wiki/Daily_challenge#map-of-the-day).

## Which beatmaps can I play? {id=beatmaps}

Every osu! beatmap, with the same ranked status as on osu!, plus maps submitted here by our mappers. Download maps in the game (osu!direct) or from the [beatmap listing](/beatmapsets).

## Why didn't my score submit? {id=score-not-submitted}

Every play on a beatmap the server knows is submitted and saved, with its replay, whatever the map's status. The status only decides what the play gives you, as on osu!:

| Map status | Leaderboard | pp |
| :-- | :-- | :-- |
| Ranked, Approved | Yes | Yes |
| Qualified | Yes | No. Qualified maps are ranked after 1 day (see the [ranking queue](/wiki/Beatmap_ranking_procedure/Ranking_queue)). |
| Loved | Yes | No |
| Pending, WIP, Graveyard | No | No |

So a play on an unranked map that gave you nothing *was* submitted; it just doesn't count for rankings.

A score is really not submitted only when:

- **Your TumThai is out of date.** Update it from the [download page](/home/download) (an installed TumThai updates itself).
- **Your Somtum Patcher or legacy client is out of date or damaged.** Get it again from the [download page](/home/download) or the Somtum Launcher. The game usually tells you why; see [Error messages](#errors).
- **The beatmap isn't on the server**, for example a map you made yourself and never submitted.
- **You connected another way** than the Somtum Launcher, the Somtum Patcher, TumThai or our legacy clients (for example `-devserver`, your own modded client, g0v0 or LazerAuthlibInjection). See [How do I connect?](#how-do-i-connect)

If your account is restricted, your scores are still saved, but they're hidden from everyone else: only you can see them (see [Restrictions & appeals](/legal/en/Restrictions)).

## I was restricted. What now? {id=restricted}

Read [Restrictions & appeals](/legal/en/Restrictions). If you think it's a mistake, email [support@somtum.fun](mailto:support@somtum.fun).

## Playing with the Somtum Patcher {id=somtum-patcher}

The Somtum Patcher launches osu!(stable) on somtum.fun and keeps the session fair. While it is running:

- **Don't run memory readers or cheat tools** (Cheat Engine, osu! trainers, pattern scanners, timing-rate hacks, auto-clickers, replay editors and the like). The Patcher watches osu!'s memory and process handles for them, and if it sees one your score will be refused and your account can be restricted.
- **Don't attach a debugger to osu!.exe.** The Patcher treats debuggers as tamper. If you're just curious, close the debugger before launching.
- **Overlays like Discord, MSI Afterburner or RivaTuner are fine.** The Patcher only flags programs that read or write osu!'s own memory.
- **Streaming and recording software are fine** (OBS, ShadowPlay, NVIDIA/AMD overlay). They don't touch the game.
- **Tablet drivers are fine** (OpenTabletDriver in any output mode, Wacom, Huion, XP-Pen, Windows Ink).
- **ReShade and other shader injectors aren't allowed**, and neither is anything else you add to the osu! folder. ReShade works by putting its own `opengl32.dll`, `d3d9.dll` or `dxgi.dll` next to `osu!.exe`, the same way some cheats load. With one of those files there, your scores aren't submitted. Delete it and start osu! again. Any other DLL that isn't part of osu! counts as cheating.

If you weren't using any of those and your score was still refused, email [support@somtum.fun](mailto:support@somtum.fun) from your account's email with your username and roughly when you played, and we'll look into it.

## What is osu!dan? {id=osu-dan}

Courses of long osu!mania maps, from DanReform: pass one with 96% accuracy and no pausing, and it's on your record. See [osu!dan](/wiki/osu!dan) for the rules, and the [osu!dan page](/community/dan) for the courses.

## How do I get a title or a group badge? {id=titles-and-groups}

Staff give them. See [User titles](/wiki/People/User_title) and [User groups](/wiki/People/User_groups).

## Can I change my username? {id=username}

Yes, on the website: [Username change](/store/products/username-change) (in the store). Everyone gets 5 free changes every 30 days, and [Somtum Supporters](/home/support) can change it as often as they like. Some names can't be used (staff keep a list of blocked names).

If it doesn't work for you, email [accounts@somtum.fun](mailto:accounts@somtum.fun) from your account's email address.

## Where do I report a bug or a player? {id=reporting}

Report players with the report button in the game or on their profile. Report bugs on our [Discord](https://discord.gg/U6Ztb3mRyz). For anything serious, see [Reporting abuse](/wiki/Reporting_bad_behaviour/Abuse).

## Error messages {id=errors}

What the messages you might see in the game mean, and what to do about them.

### "Authentication failed" or "Incorrect password" {id=error-login}

Check your username and password; they're the same as on this website. Forgot your password? [Reset it here](/home/password-reset). Signing up happens in the game, not on the website (see [How do I make an account?](#registration)).

### "This is a new device, so it needs confirming first" {id=error-new-device}

You're logging in from a computer or network we haven't seen on your account. Sign in to this website, open [the verification page](/p/verify) and confirm the device there, then log in to the game again.

### "This version of osu! can't confirm a new device" {id=error-new-device-old-client}

Older builds can't show the confirmation screen. Confirm the device on [the verification page](/p/verify) first, then log in again. If that doesn't help, use TumThai or the Somtum Patcher from the [download page](/home/download).

### "This old osu! build can't play on somtum.fun as it is" {id=error-old-build}

Only our rebuilt legacy clients can log in with a 2008-2015 build: an unmodified build (with the hook or not), or one you modded yourself, can't. Download the same build, already patched, from the [download page](/home/download). If it isn't there, ask for it in our [Discord server](https://discord.gg/U6Ztb3mRyz) or on the [forum](/community/forums/4).

### "Something on your computer isn't allowed while playing here (a debugger or a cheat tool)" {id=error-cheat-tool}

A program that reads or changes osu!'s memory is running (see [Playing with the Somtum Patcher](#somtum-patcher)). Close it, then log in again.

### "Score submission is disabled: your Somtum Patcher isn't running" or "didn't respond in time" {id=error-patcher-not-running}

osu!(stable) was started without the Somtum Patcher, or the Patcher was closed or stopped while you played. Close osu! and start it again from the Somtum Patcher or the Somtum Launcher.

### "Score submission is disabled: your Somtum Patcher failed the integrity check" {id=error-patcher-integrity}

The Patcher's files were changed or damaged (an antivirus sometimes does this). Download it again from the [download page](/home/download) and reinstall it. If your antivirus removes it, add an exception for the Patcher's folder.

### "Your anti-cheat is out of date — score submission is disabled" {id=error-anticheat-outdated}

You can play, but your Somtum Patcher or legacy client has an anti-cheat version we no longer accept. Get the newest Somtum Patcher from the [download page](/home/download) (or let the Somtum Launcher update), or download your legacy build again, then start osu! again.

### Legacy clients: "Score submission is disabled: the anti-cheat isn't running", "didn't respond in time", "failed the integrity check" or "is out of date" {id=error-legacy-anticheat}

Our legacy clients load our anti-cheat, `pkms.dll`, from their own folder, and scores need it. Make sure `pkms.dll` is still next to `osu!.exe` (an antivirus sometimes removes it: add an exception for the folder), then start `osu!.exe` again. If that doesn't help, or the message says it's out of date, download your build again from the [download page](/home/download) and unzip it to a new folder.

### "Score submission is disabled: a file next to osu!.exe replaces part of Windows" {id=error-proxy-dll}

There's a file such as `opengl32.dll`, `d3d9.dll`, `dxgi.dll`, `dinput8.dll` or `version.dll` in your osu! folder. These come from ReShade or similar tools, which aren't allowed (see [Playing with the Somtum Patcher](#somtum-patcher)). Delete the file from your osu! folder, then start osu! again. You're not in trouble for this.

### Legacy clients: "Score submission is disabled: this osu! folder doesn't match our download" {id=error-legacy-files}

A file of your legacy client isn't the one we published: it was changed, replaced, or comes from another version. Download your build again from the [download page](/home/download) and unzip it to a new, empty folder.

### "Your Somtum Patcher is out of date" {id=error-patcher-outdated}

Download the newest Somtum Patcher from the [download page](/home/download). Old versions stop being able to submit scores some time after a new one is out.

### osu! closes with "[pkms] integrity violation in 'net': server rejected flag: revoked_version" {id=error-pkms-revoked}

Your Somtum Patcher is a version we no longer accept (usually because a newer one fixes a problem). The game stops so nothing is played on it. Download the newest Somtum Patcher from the [download page](/home/download), or let the Somtum Launcher update itself, then start osu! again. You're not in trouble.

### osu! closes with "[pkms] integrity violation in 'net': pkms: launched outside injector" {id=error-pkms-outside}

The anti-cheat was loaded without the Somtum Patcher starting osu!. This happens when osu! restarts itself (after an osu! update, or from its own options) while the Patcher is attached. Close osu! and start it again from the Somtum Patcher or the Somtum Launcher.

### osu! closes with "[pkms] integrity violation in 'net': network worker terminated unexpectedly" {id=error-pkms-network}

The part of the anti-cheat that talks to our server was stopped. Most often an antivirus or firewall stopped it. Allow the Somtum Patcher's folder in your antivirus, close any tools that touch osu!, and start osu! again from the Patcher.

### osu! closes with "[pkms] violation handler patched", "unreadable" or "stalled; failing closed" {id=error-pkms-handler}

Something changed or froze the anti-cheat inside osu!. Close any program that reads or writes osu!'s memory (see [Playing with the Somtum Patcher](#somtum-patcher)) and start osu! again from the Patcher. If you weren't running anything like that, email [support@somtum.fun](mailto:support@somtum.fun) with your username, roughly when it happened and your antivirus's name.

### Other "[pkms] integrity violation in '…'" messages {id=error-pkms-other}

The anti-cheat found something changing osu! while it ran, and closed the game. Close the program it found and start osu! again from the Patcher. If it keeps happening and you don't know why, email [support@somtum.fun](mailto:support@somtum.fun) with a screenshot of the message.

### "osu! did not finish starting within 10 seconds and has been closed" {id=error-patcher-start}

osu! got stuck while starting (often while it updates, or while an antivirus scans it). Start `osu!.exe` once by itself, let it reach the main menu, close it, then use the Somtum Patcher again. If it keeps happening, delete osu!'s update and launcher cache files from your osu! folder.

### "Still verifying your client — hold on" {id=error-patcher-verifying}

Not an error: the Patcher is still checking in with our server. It can take up to 45 seconds, mostly on Linux with Wine. Wait for "Client verified".

### "Your computer has traces of hq!osu's multi-account tool (relife)" {id=error-relife}

osu! found relife in your Windows registry. Turn relife off (or reinstall it and turn it off) so it doesn't trip again. This is a warning, not a restriction.

### "Please contact staff directly to create an account" {id=error-contact-staff}

A new account was made on the same computer as a restricted account. If that's a shared or family computer and you aren't the restricted player, email [accounts@somtum.fun](mailto:accounts@somtum.fun) with both usernames.

### "This account is locked. Please contact staff." {id=error-locked}

Staff locked the account. Email [support@somtum.fun](mailto:support@somtum.fun) from the account's email address.

### "This account has been deleted" {id=error-deleted}

The account was deleted on request or by staff. Email [accounts@somtum.fun](mailto:accounts@somtum.fun) if you think that's a mistake.

### "Bot accounts can't log in to the game" {id=error-bot}

That's a [bot account](/wiki/Bot_account): it can only chat over IRC. Log in to the game with your own account.

### "This account has too many tournament client windows open" {id=error-tournament-windows}

Close some of the tournament client's windows and try again (see [Tournament client](/wiki/Tournaments/Tournament_client)).

### osu!dan: "this attempt won't count as a clear" {id=error-dan}

Your score is saved as normal, it just isn't a dan clear. See [osu!dan](/wiki/osu!dan#not-a-clear) for each reason.

### osu!dan: "This beatmap is part of osu!dan, which can't be played in multiplayer or playlists" {id=error-dan-lazer}

TumThai (osu!lazer) shows this under "Score will not be submitted" when a multiplayer room or playlist has a map from an [osu!dan](/wiki/osu!dan#lazer) course. Dan maps are only for solo play, so the play isn't saved. Play the map on its own (with the Classic mod) instead.
