# osu!dan

osu!dan is a set of **courses** for osu!mania: long marathon maps that test your consistency, stamina and reading. Clear a course and it shows on your record; clear the next one to move up. somtum.fun's courses and rules come from [Dan ~ REFORM ~](https://www.danreform.com/) (DanReform). DanReform is a community project, not an official osu! website, so follow its own rules for its courses too.

See every course, its maps and who has cleared it on the [osu!dan page](/community/dan). Courses appear there as staff add them.

## Rules {id=rules}

A play counts as a **clear** only when all of these are true:

- **osu!mania**, in **osu!(stable)**: today's osu! through the Somtum Patcher, or one of our patched old clients from mid-2013 on. Dan maps can't be played for scores in TumThai (osu!lazer) yet: see [below](#lazer).
- **No pausing.** BanchoBot spectates you while you play a course map (you'll see "BanchoBot is spectating"), so it can tell if you pause.
- **Accuracy:** 96% or more, or 95% for intro courses. The accuracy is the one the game shows you, to two decimals.
- **Only allowed mods:** Mirror, Hidden, Fade In, Flashlight, Hard Rock, Double Time and Nightcore, unless a course says otherwise.
- **You pass the map.** A failed play isn't a clear.

A course with several maps is cleared once each of its maps has a clear. If you clear a course again, it keeps the date of your first clear and your best accuracy.

## What happens to a play that doesn't count {id=not-a-clear}

In osu!(stable), it's still a **normal score**: it stays on the leaderboard and in your stats, it just isn't a dan clear. BanchoBot tells you why, for example:

| BanchoBot says | What to do |
| :-- | :-- |
| *you paused, so this … attempt won't count as a clear* | Retry the map (a retry starts a new attempt) and don't pause. |
| *… isn't allowed here, so this play won't count* | Take that mod off. Only the allowed mods above count. |
| *it needs 96% accuracy* | Play again for higher accuracy. |
| *it wasn't played in osu!mania* | Play the course in osu!mania, not converted to another mode. |
| *BanchoBot couldn't watch the play* | You started the map before BanchoBot could start watching, or lost connection. Play it again. |
| *this osu! version can't be watched for pauses* | Builds from before May 2013 can't be watched. Use the Somtum Patcher or a newer patched client from the [download page](/home/download). |

## Chat commands {id=commands}

Type these in any chat, or in a private message to BanchoBot:

| Command | What it shows |
| :-- | :-- |
| `!dan` | Your highest clear for each key count, and the next course to try |
| `!dan <player>` | Someone else's |
| `!dan list` | Every course |
| `!dan rules` | The rules, in short |

## osu!lazer and TumThai {id=lazer}

osu!dan is only for osu!(stable) for now: BanchoBot can't watch osu!lazer plays for pauses yet. When you start a dan map in TumThai (our osu!lazer), the game tells you:

> **Score will not be submitted**
> This beatmap is part of osu!dan, which is only for osu!(stable) for now. Stay tuned!

You can still play the map, but the score isn't saved: it doesn't go on the leaderboard or in your stats. In multiplayer and playlists the map can't be started at all. Play dan courses in osu!(stable). Stay tuned for osu!lazer support.

## Beatmaps {id=beatmaps}

Dan maps on somtum.fun are **Loved**: they have leaderboards but give no pp. Each course on the [osu!dan page](/community/dan) links its maps, so you can download them there, or get them from [DanReform](https://www.danreform.com/).

We're starting with 4K. Other key counts (7K first) and other course packs come later. If you know a course pack or a ruleset we should support, tell us on our [Discord](https://discord.gg/U6Ztb3mRyz).
