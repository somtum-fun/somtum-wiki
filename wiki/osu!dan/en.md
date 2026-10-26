# osu!dan

osu!dan is a set of **courses** for osu!mania: long marathon maps that test your consistency, stamina and reading. Clear a course and it shows on your record; clear the next one to move up. somtum.fun's courses and rules come from [Dan ~ REFORM ~](https://www.danreform.com/) (DanReform). DanReform is a community project, not an official osu! website, so follow its own rules for its courses too.

See every course, its maps and who has cleared it on the [osu!dan page](/community/dan). Courses appear there as staff add them.

## Rules {id=rules}

A play counts as a **clear** only when all of these are true:

- **osu!mania**, in **osu!(stable)** (today's osu! through the Somtum Patcher, or one of our patched old clients from mid-2013 on) or in **TumThai** (our osu!lazer) with the Classic mod: see [below](#lazer).
- **No pausing.** LimeBot spectates you while you play a course map (you'll see "LimeBot is spectating"), so it can tell if you pause.
- **Accuracy:** 96% or more, or 95% for intro courses. The accuracy is the one the game shows you, to two decimals.
- **Only allowed mods:** Mirror, Hidden, Fade In, Flashlight, Hard Rock, Double Time and Nightcore, unless a course says otherwise.
- **You pass the map.** A failed play isn't a clear.

A course with several maps is cleared once each of its maps has a clear. If you clear a course again, it keeps the date of your first clear and your best accuracy.

## What happens to a play that doesn't count {id=not-a-clear}

In osu!(stable), it's still a **normal score**: it stays on the leaderboard and in your stats, it just isn't a dan clear. (In TumThai, a play that breaks the rules isn't kept: see [osu!lazer and TumThai](#lazer).) LimeBot tells you why, for example:

| LimeBot says | What to do |
| :-- | :-- |
| *you paused, so this … attempt won't count as a clear* | Retry the map (a retry starts a new attempt) and don't pause. |
| *… isn't allowed here, so this play won't count* | Take that mod off. Only the allowed mods above count. |
| *it needs 96% accuracy* | Play again for higher accuracy. |
| *it wasn't played in osu!mania* | Play the course in osu!mania, not converted to another mode. |
| *LimeBot couldn't watch the play* | You started the map before LimeBot could start watching, or lost connection. Play it again. |
| *this osu! version can't be watched for pauses* | Builds from before May 2013 can't be watched. Use the Somtum Patcher or a newer patched client from the [download page](/home/download). |

## Chat commands {id=commands}

Type these in any chat, or in a private message to LimeBot:

| Command | What it shows |
| :-- | :-- |
| `!dan` | Your highest clear for each key count, and the next course to try |
| `!dan <player>` | Someone else's |
| `!dan list` | Every course |
| `!dan rules` | The rules, in short |

## osu!lazer and TumThai {id=lazer}

You can play dan courses in TumThai (our osu!lazer), with the same rules:

- **Turn on the Classic mod (CL).** Without it, TumThai shows "Score will not be submitted" and says why. An older TumThai is asked to update.
- **Don't pause.** The first pause tells you the play can't count, and a paused play isn't submitted.
- **The rest of the [rules](#rules) apply too:** osu!mania only, only the allowed mods (a lazer-only mod, or one with its own settings, isn't allowed), and the course's accuracy, counted as osu!(stable) counts it.

A TumThai play that keeps the rules goes on the map's leaderboard and in your stats like any other score, and **counts as a clear**, within a couple of minutes of finishing (once the server has processed it). One that breaks them isn't kept at all.

Instead of LimeBot, our spectator server watches TumThai plays: it's how the server knows you didn't pause. A play it didn't see (for example, if your connection to it dropped) isn't a clear, so play the map again. Dan maps can't be played in multiplayer or playlists.

## Beatmaps {id=beatmaps}

Dan maps on somtum.fun are **Loved**: they have leaderboards but give no pp. Each course on the [osu!dan page](/community/dan) links its maps, so you can download them there, or get them from [DanReform](https://www.danreform.com/).

We're starting with 4K. Other key counts (7K first) and other course packs come later. If you know a course pack or a ruleset we should support, tell us on our [Discord](https://discord.gg/U6Ztb3mRyz).
