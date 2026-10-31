# Reporting a bug

Found something broken, or did the game crash? Tell us: most fixes start with a player's report. This page says what to send so we can find the problem quickly.

Before you report, check [Common problems](/wiki/Help_centre/Common_problems) and the [FAQ](/wiki/FAQ): your problem may already have a fix.

## Where to report {id=where}

- **Our [Discord server](https://discord.gg/U6Ztb3mRyz):** the quickest way, and staff can ask you questions.
- **Email [support@somtum.fun](mailto:support@somtum.fun)** from your account's email address, if you'd rather not use Discord. Attach the logs to the email.

For a cheater or a rude player, use the report button instead (see [Help centre](/wiki/Help_centre#reporting-a-player)). For a security problem (a way to cheat the server, or to see someone else's data), see [Reporting a security problem](/wiki/Help_centre/Reporting_a_security_problem) and don't post it in public.

## What to tell us {id=what}

1. **What happened**, and what you expected to happen instead.
2. **How to make it happen again**, step by step, if you can.
3. **When it happened** (the date and time, and your time zone): we look for it in the server's logs.
4. **Which client and version**: TumThai or TumThai!Next (shown at the bottom of Settings), osu!(stable) with the Somtum Patcher (the Patcher's version, and osu!'s under **Options → General → Updates**), or which old client (for example b20130606.1).
5. **Your system**: Windows (which version), Linux (which distribution, and if you use Wine), macOS or Android.
6. **Your username**, and the link to the beatmap or score if it's about one.
7. **Logs**, for a crash or a client problem (see [below](#logs)). A screenshot or a short video helps too.

## Getting the logs {id=logs}

### With the Somtum Launcher (the easiest way) {id=logs-launcher}

1. In the Somtum Launcher, open **Settings → Advanced options** and turn on **Record logs**.
2. Start the game from the launcher and make the problem happen again.
3. Back in the launcher, press **Export logs** in **Settings → Advanced options**. On Linux, run `somtum export-logs`.
4. A zip appears on your Desktop: send it with your report.

The zip holds the launcher's log, what the games logged, TumThai's own logs, osu!'s Logs folder, the old clients' crash logs and Windows' own error reports for these programs. It never holds your password, your login, or your game settings. Recording logs can cost a little performance: turn **Record logs** off again once you've sent them.

### TumThai {id=logs-tumthai}

TumThai always keeps logs. In TumThai, open **Settings → General** and press **Export logs**: a zip of them is saved for you to send. **Open TumThai folder** in the same place shows them too, in the `logs` folder.

### osu!(stable) with the Somtum Patcher {id=logs-stable}

The Somtum Patcher writes `patcher.log` in the `Logs` folder inside your osu! folder. Send that file, or use the launcher's [Export logs](#logs-launcher), which includes it.

### Old clients (2008 to 2015) {id=logs-legacy}

When an old client crashes, it writes a crash log in its own folder. With **Record logs** on in the Somtum Launcher, it also writes a log of the whole session, from the moment it starts. The launcher's [Export logs](#logs-launcher) collects both.

## What happens next {id=next}

Staff read every report. We may ask you a question or two, or for a test build. Fixes come in updates: TumThai and the Somtum Launcher update themselves, and every change is listed on the [changelog](/home/changelog). Thank you for helping make somtum.fun better!
