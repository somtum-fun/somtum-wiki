# Why somtum.fun?

somtum.fun is a free, fan-run osu! server. Here's what you get by playing here, and what runs it.

## At a glance {id=at-a-glance}

- **A custom-built bancho core:** our own osu! server backend, developed by [blueskychan_](/users/2) and [Lilian](/users/410). It isn't bancho.py or g0v0 (see [below](#our-own-server)).
- **One account everywhere:** the same account, profile and friends in TumThai (osu!lazer), osu!(stable) and the old 2008-2015 clients.
- **osu!lazer sees osu!(stable) scores**, like on osu!: one leaderboard per map, whichever client you play on.
- **Old clients welcome:** 75 osu! builds from 2008 to 2015, rebuilt to connect here.
- **Built-in pp calculator:** every beatmap page on the website has one: pick mods, misses, combo and accuracy and see what a pass would be worth, in every mode (converted maps too). Every play's pp is worked out on the server, Relax and Autopilot included, and osu!(stable) gets a live pp counter through the Somtum Patcher.
- **Earn custom medals** the community asked for, on top of osu!'s own.
- **Custom rulesets:** play Sentakki, Tau, Rush!, Soyokaze and more in TumThai, with their own leaderboards and rankings.
- **More to play:** Relax and Autopilot boards, [osu!dan](/wiki/osu!dan) courses, the [Daily challenge](/wiki/Daily_challenge) and [Map of the day](/wiki/Map_of_the_day).
- **Watch any play as a video:** render a replay on its score page or from our Discord bot, in your own skin.
- **Frequent updates:** we fix and add things all the time; see the [changelog](/home/changelog).
- **Free**, always.

## One account for every osu! {id=one-account}

- **TumThai**, our version of osu!lazer, for Windows, Linux, macOS and Android. It updates itself. **TumThai!Next** is its faster, experimental stream, on our own framework, for players who want the newest performance options first.
- **osu!(stable)**, today's client, through the **Somtum Patcher** or the **Somtum Launcher**.
- **osu! from 2008 to 2015**: play the client you started with.

Your profile, friends, scores and rankings are the same in all of them and on this website. See [How do I connect?](/wiki/FAQ#how-do-i-connect)

## More ways to play {id=more-ways-to-play}

- **Relax and Autopilot** with their own leaderboards, rankings and pp, in TumThai and osu!(stable). See [Relax and Autopilot](/wiki/FAQ#relax-and-autopilot) and [Performance points](/wiki/Performance_points).
- **Custom rulesets** from [rulesets.info](https://rulesets.info), installed right in TumThai (**Settings → General → Custom rulesets**): Sentakki, Tau, Rush!, Hishigata, Soyokaze, FPSosu, osu!fps, Swing, Sandbox, bosu! and Touhosu. Each has its own leaderboards, rankings and profile pages, ranked by score.
- **Replay videos:** render any osu! play as a video, with [o!rdr](https://ordr.issou.best), from its score page or with our Discord bot's `/render`, in the skin you pick.
- **[osu!dan](/wiki/osu!dan)**: osu!mania dan courses with real rules (no pausing, accuracy, mods), and clears on your profile.
- **[Daily challenge](/wiki/Daily_challenge)** and **[Map of the day](/wiki/Map_of_the_day)**.
- **Custom medals**: ask for one on the medals page, and our Medal Team adds the good ones for everyone to earn.
- **Our own beatmaps and ranking**: mappers can upload sets here, and our nominators rank and love maps on [BN Management](https://bn.somtum.fun) (see [Beatmap ranking procedure](/wiki/Beatmap_ranking_procedure)).
- **[Tournaments](/wiki/Tournaments)**, with the tournament client.

## Fair play {id=fair-play}

Scores from osu!(stable) and the old clients only count with our anti-cheat running, and replays are checked after you play. The old clients are our own patched builds of each version (the old "hook" isn't used any more). Cheaters are restricted, and you can [appeal](/legal/en/Restrictions) if you think we got it wrong. TumThai and the Somtum Patcher are the only ways in whose scores count, so everyone plays on the same terms.

## Our own server, not bancho.py or g0v0 {id=our-own-server}

somtum.fun doesn't run on [bancho.py](https://github.com/osuAkatsuki/bancho.py) or [g0v0](https://github.com/GooGuTeam/g0v0-server), the server software many other private servers use. It runs on our own, self-developed osu! server backend.

- **The game server is [TomYum](https://github.com/somtum-fun/TomYum-OSS)**, our custom-built bancho core in C# (.NET), developed by [blueskychan_](/users/2) and [Lilian](/users/410). One server speaks to osu!lazer, today's osu!(stable) and the old 2008-2015 clients alike, and works out pp itself. It's open source; its documentation is at [docs.somtum.fun](https://docs.somtum.fun).
- **The website is our fork of [osu-web](https://github.com/ppy/osu-web)**, the same software as osu.ppy.sh. That's why profiles, beatmap pages, rankings, the forum and the API v2 look and work like osu!'s.
- **For lazer**, we run ppy's own open-source spectator and score-processing servers next to TomYum, so multiplayer, spectating and replays work as they do on osu!.
- **bancho.py:** somtum.fun ran on it until 12 October 2026. When we moved to TomYum, your account, scores and custom medals came along. Tools made for bancho.py servers still work through our [bancho.py API](/wiki/API#bancho-py-api).
- **g0v0** is a separate osu!lazer server project. We don't use any of it; TumThai talks to our own servers. Its client can still connect (see [Connecting with another lazer client](/wiki/FAQ#other-lazer-clients)), but its scores aren't submitted.

Something not working? See [Reporting a bug](/wiki/Help_centre/Reporting_a_bug). Ready? Head to the [download page](/home/download), or start with the [FAQ](/wiki/FAQ).
