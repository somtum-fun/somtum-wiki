# FAQ

Answers to the questions we hear most. Can't find yours? See the [Help centre](/wiki/Help_centre).

## What is somtum.fun? {id=what-is-somtum-fun}

somtum.fun is a fan-run private server for the rhythm game osu!. It has its own accounts, rankings, beatmaps and community. It is not affiliated with ppy Pty Ltd, and your osu! account and scores on osu.ppy.sh aren't shared with it.

## How do I connect? {id=how-do-i-connect}

All downloads are on the [download page](/home/download).

- **TumThai** is our version of osu!lazer, for Windows and Linux. Install it (or unzip the portable version) and sign in. It updates itself.
- **osu!(stable):** run the **Somtum Patcher** to play your osu!(stable) on somtum.fun.
- **Old clients (2008 to 2015):** download one of the rebuilt legacy clients, unzip it anywhere and run `osu!.exe`. They need Windows and .NET Framework 3.5 (a few 2015 builds need .NET Framework 4). If you'd rather play an unmodified build, use the hook from the same page. The hook ([somtum-fun/hook](https://github.com/somtum-fun/hook)) also lets old builds play today's beatmaps: it fixes, as each map loads, the parts of a modern `.osu` file an old build can't read.

## How do I make an account? {id=registration}

Make it in the game: open TumThai or osu!(stable) on somtum.fun and register there, not on the website. Then sign in to this website with the same name and password.

You can have **one account**. Sign-ups through a VPN, proxy, Tor or a hosting network are blocked, and each network can make one account a day. If that stops you from signing up honestly, email [accounts@somtum.fun](mailto:accounts@somtum.fun).

## Is it free? {id=is-it-free}

Yes. Supporter tags are optional and help pay for the server.

## Relax and Autopilot {id=relax-and-autopilot}

Relax and Autopilot have their own leaderboards, rankings and pp, separate from normal play, in both TumThai and osu!(stable). Choose them on the rankings page and on beatmap leaderboards.

## Which beatmaps can I play? {id=beatmaps}

Every osu! beatmap, with the same ranked status as on osu!, plus maps submitted here by our mappers. Download maps in the game (osu!direct) or from the [beatmap listing](/beatmapsets).

## Why didn't my score submit? {id=score-not-submitted}

- You played with a mod that isn't ranked here. Those plays don't give pp and stay off the leaderboards.
- Your TumThai is out of date. Update it from the [download page](/home/download) (an installed TumThai updates itself).
- The beatmap isn't ranked, approved or loved.
- Your account is restricted (see [Restrictions & appeals](/legal/en/Restrictions)).

## I was restricted. What now? {id=restricted}

Read [Restrictions & appeals](/legal/en/Restrictions). If you think it's a mistake, email [support@somtum.fun](mailto:support@somtum.fun).

## Playing with the Somtum Patcher {id=somtum-patcher}

The Somtum Patcher launches osu!(stable) on somtum.fun and keeps the session fair. While it is running:

- **Don't run memory readers or cheat tools** (Cheat Engine, osu! trainers, pattern scanners, timing-rate hacks, auto-clickers, replay editors and the like). The Patcher watches osu!'s memory and process handles for them, and if it sees one your score will be refused and your account can be restricted.
- **Don't attach a debugger to osu!.exe.** The Patcher treats debuggers as tamper. If you're just curious, close the debugger before launching.
- **Overlays like Discord, MSI Afterburner or RivaTuner are fine.** The Patcher only flags programs that read or write osu!'s own memory.
- **Streaming and recording software are fine** (OBS, ShadowPlay, NVIDIA/AMD overlay). They don't touch the game.

If you weren't using any of those and your score was still refused, email [support@somtum.fun](mailto:support@somtum.fun) from your account's email with your username and roughly when you played, and we'll look into it.

## What is osu!dan? {id=osu-dan}

Courses of long osu!mania maps, from DanReform: pass one with 96% accuracy and no pausing, and it's on your record. See [osu!dan](/wiki/osu!dan) for the rules, and the [osu!dan page](/community/dan) for the courses.

## How do I get a title or a group badge? {id=titles-and-groups}

Staff give them. See [User titles](/wiki/People/User_title) and [User groups](/wiki/People/User_groups).

## Can I change my username? {id=username}

Email [accounts@somtum.fun](mailto:accounts@somtum.fun) from your account's email address.

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

That build needs our fixes. Download the same build, already patched, from the [download page](/home/download), or run it through the hook.

### "Something on your computer isn't allowed while playing here (a debugger or a cheat tool)" {id=error-cheat-tool}

A program that reads or changes osu!'s memory is running (see [Playing with the Somtum Patcher](#somtum-patcher)). Close it, then log in again.

### "Score submission is disabled: your Somtum Patcher isn't running" or "didn't respond in time" {id=error-patcher-not-running}

osu!(stable) was started without the Somtum Patcher, or the Patcher was closed or stopped while you played. Close osu! and start it again from the Somtum Patcher or the Somtum Launcher.

### "Score submission is disabled: your Somtum Patcher failed the integrity check" {id=error-patcher-integrity}

The Patcher's files were changed or damaged (an antivirus sometimes does this). Download it again from the [download page](/home/download) and reinstall it. If your antivirus removes it, add an exception for the Patcher's folder.

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
