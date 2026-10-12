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

## Can I change my username? {id=username}

Email [accounts@somtum.fun](mailto:accounts@somtum.fun) from your account's email address.

## Where do I report a bug or a player? {id=reporting}

Report players with the report button in the game or on their profile. Report bugs on our [Discord](https://discord.gg/U6Ztb3mRyz). For anything serious, see [Reporting abuse](/wiki/Reporting_bad_behaviour/Abuse).
