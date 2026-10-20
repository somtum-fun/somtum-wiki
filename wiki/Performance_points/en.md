# Performance points

**Performance points (pp)** measure how impressive a play is. Every pass on a ranked or approved map gets pp (qualified and loved maps don't, see [the FAQ](/wiki/FAQ#score-not-submitted)), and your best plays add up to your total pp and your rank. osu!'s wiki explains [what pp is](https://osu.ppy.sh/wiki/Performance_points); this page says which calculator works out the pp for each mode on somtum.fun.

## Which calculator each mode uses {id=calculators}

Normal play uses **osu!'s official calculator**, the same one osu.ppy.sh uses. Relax and Autopilot have their own rankings, and their pp comes from **[akatsuki-pp-rs](https://github.com/osuAkatsuki/akatsuki-pp-rs)**: Akatsuki's calculators, made for those mods.

| Mode | Variant | Calculator | In short |
| :-- | :-- | :-- | :-- |
| osu! | Normal | osu!'s official calculator | Aim, speed, accuracy and flashlight, as on osu! |
| osu!taiko | Normal | osu!'s official calculator | As on osu! |
| osu!catch | Normal | osu!'s official calculator | As on osu! |
| osu!mania | Normal | osu!'s official calculator | As on osu! |
| osu! | Relax | akatsuki-pp-rs, Akatsuki's Relax formula (`osu_2019`) | Built for Relax: you don't tap, so it's about aim and accuracy. It has its own star rating. |
| osu!taiko | Relax | akatsuki-pp-rs | Akatsuki's version of the normal osu!taiko calculator |
| osu!catch | Relax | akatsuki-pp-rs | Akatsuki's version of the normal osu!catch calculator |
| osu! | Autopilot | akatsuki-pp-rs, with Autopilot changes | The cursor moves by itself, so aim gives no pp: it's about tapping (speed) and accuracy |

osu!mania has no Relax, and only osu! has Autopilot.

Because Relax and Autopilot pp is worked out in other ways, it isn't comparable with normal pp. That's why they have their own leaderboards and rankings (see [Relax and Autopilot](/wiki/FAQ#relax-and-autopilot)), and why they don't count for the [map of the day](/wiki/Map_of_the_day).

## TumThai and osu!(stable) {id=clients}

Plays from both clients count towards the same rankings, and both use the calculators above:

- **osu!(stable)** plays get their pp from the game server as they're submitted.
- **TumThai (osu!lazer)** plays get theirs from osu!'s own score processor, as on osu.ppy.sh, so a TumThai play gets the pp it would get on osu!. Relax and Autopilot plays from TumThai go to the same Relax and Autopilot calculators as osu!(stable)'s.
- A TumThai play only gets pp when all of its mods are **ranked**: osu!'s usual mods with their normal settings. Staff can rank more mods; those count whatever their settings. TumThai may still call such a mod unranked while you play; the server decides once the play is submitted.

## How your total is worked out {id=total}

Your plays are sorted by pp, best first. Your best play counts in full, your second best 95%, your third 90.25%, and so on (each 95% of the one before). A small bonus is then added for how many maps you've played, as on osu!. Only your best play on each map counts. Relax and Autopilot totals are worked out the same way, from their own plays.

## When the pp changes {id=pp-updates}

osu! and Akatsuki change their calculators now and then. When they do, staff update somtum.fun's and recalculate every play: a **pp rework**. While one runs, a banner on every page says which modes it affects and how far along it is. The rankings for those modes pause, and new plays in them get their pp once it's done. Then everything switches to the new pp at once. Big pp updates are announced in the [news](/home/news).
