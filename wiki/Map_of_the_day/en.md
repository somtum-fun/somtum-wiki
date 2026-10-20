# Map of the day

The **map of the day** is a small daily contest run by our Discord bot. Every day the bot posts a random ranked map in our [Discord server](https://discord.gg/U6Ztb3mRyz), and whoever sets the best pass on it that day wins the **Map of the Day** role for a week.

It isn't the same as the [daily challenge](/wiki/Daily_challenge): that one is a playlist room inside TumThai (osu!lazer), ranked by score. See [how they differ](/wiki/Daily_challenge#map-of-the-day).

## How it works {id=how-it-works}

1. Soon after midnight UTC, the bot posts the day's map in the map of the day channel on Discord. It's a random **ranked** difficulty, 3 to 6.5 stars and 1 to 7 minutes long.
2. Play it like any other map, in **TumThai** or **osu!(stable)**. You don't play it in a special room, and you don't have to be on Discord to take part.
3. At midnight UTC the day ends. The best pass set that day wins: **the most pp**, then the highest score if two plays have the same pp.
4. The next day the bot announces the winner together with the new map.

## What counts {id=what-counts}

- **A pass** on that difficulty, set between midnight and midnight UTC on the day it was posted.
- **In the map's own mode.** An osu! map played as osu!taiko or osu!catch (a convert) doesn't count.
- **Any mods**, since the winner is picked by pp: Hard Rock, Double Time and the like can help.
- **Not Relax or Autopilot.** Their pp is worked out differently (see [Performance points](/wiki/Performance_points)), so those plays are left out.
- Restricted accounts can't win.

## The Map of the Day role {id=role}

The winner gets the **Map of the Day** role in our Discord server for **7 days**; the bot takes it back after that. Win again while you have it and the 7 days start over from the new win.

The bot can only give you the role if your Discord account is **linked** to your somtum.fun account. If you win without a link, you're still announced as the winner, just without the role. See [Linking Discord](#linking-discord).

## Linking Discord {id=linking-discord}

There are two ways, and both make the same link, so you only need one:

- **On the website:** open your [account settings](/home/account/edit#connections), find **Connections** and link Discord.
- **On Discord:** use `/link` with our bot. It replies with a code: send `!link <code>` to **LimeBot** in a private message (in the game or on the website) within a few minutes.

::: alert-note
**Already linked Discord on the website?** Then you're done: you don't need `/link` on Discord as well. If you use `/link` anyway, the bot tells you who you're already linked to.
:::

To unlink, use **Connections** on the website or `/unlink` on Discord.
