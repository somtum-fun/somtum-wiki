# Custom speed pp glitch (November 2026)

From 14 to 20 November 2026, lazer plays with **Double Time or Nightcore set to a custom speed** were given far too much pp in Relax. It was a server bug, not cheating, and it's fixed now. Nobody needs to do anything.

## What happened {id=what-happened}

In osu!lazer, DT and NC have a speed setting. The usual speed is 1.5×, but you can pick anything from 1.01× to 2×, and HT and DC can be set from 0.5× to 0.99×.

Our pp calculator for Relax and Autopilot only got told *which* mods were on, not how fast they were set. It saw "DT" and assumed the usual 1.5×. So a play at **DT 1.01×**, which is almost normal speed, was paid as if it was 50% faster.

For example, Ito Kanako - Sky of Twilight (Sped Up Ver.) with HR, DT at 1.01× and Relax at 98.75% was given **3,147 pp**. It's worth **875 pp**.

Only Relax was affected in practice: 707 plays from 4 players. Autopilot used the same calculator, but nobody played it at a custom speed. Normal (non-Relax) pp uses osu!'s own calculator, which always handled the speed correctly. osu!(stable) can't change DT's speed, so stable plays were never affected.

## How it was fixed {id=fix}

- **20 November, first fix:** DT and NC set below 1.5× were paid as if DT was off, so the glitch couldn't give extra pp any more. Every Relax score was worked out again.
- **20 November, full fix:** the server now sends the real speed to the calculator, so every play is paid at the speed it was played. DT at 1.01× is paid as 1.01×, and DT at 2× is paid as 2× (before, anything above 1.5× was paid as 1.5×). Every Relax score was worked out again.

Players who used the glitch were not punished. It was our bug, and they didn't break any [rules](/wiki/Rules). They got the [PP Breaker](/wiki/People/Users_with_unique_titles#pp-breaker) title instead.

## Old score posts {id=old-posts}

Score posts sent to Discord before the fix still show the old pp, such as "3,147.39pp" for the play above. Posts can't be changed after they're sent. The pp on the website and in game is the correct one.

## See also {id=see-also}

- [Performance points](/wiki/Performance_points)
- [Relax and Autopilot](/wiki/Relax_and_Autopilot)
- [Users with unique titles](/wiki/People/Users_with_unique_titles)
