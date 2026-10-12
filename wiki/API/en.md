# API

somtum.fun has two APIs for tools, bots and websites. Both only see somtum.fun's own players and scores; nothing here comes from osu.ppy.sh's accounts.

| | Address | For |
| :-- | :-- | :-- |
| [API v2](#api-v2) | `https://osu.somtum.fun/api/v2` | Anything written for osu!'s API v2 |
| [bancho.py API](#bancho-py-api) | `https://api.somtum.fun/v1` | Tools and bots written for bancho.py servers |

osu!'s old **API v1** (`/api/get_user?k=...` and the rest) isn't available on somtum.fun. Use API v2, or the bancho.py API, which covers most of what v1 did.

Please be gentle with both: cache what you can, and don't send more than about one request a second. Tools that put too much load on the server can be blocked.

## API v2 {id=api-v2}

This is osu!'s API v2, served by our website, so libraries and code written for osu.ppy.sh work after you change the address.

| | |
| :-- | :-- |
| API | `https://osu.somtum.fun/api/v2` |
| Get a token | `https://osu.somtum.fun/oauth/token` |
| Ask a player to sign in | `https://osu.somtum.fun/oauth/authorize` |
| Reference (every endpoint) | [osu.somtum.fun/docs](https://osu.somtum.fun/docs/) |

1. Make an OAuth application in your [account settings](/home/account/edit#oauth) (**New OAuth Application**). You get a client id and a client secret. Keep the secret private.
2. Get a token. For public data (players, scores, beatmaps, rankings), use the client credentials grant:

   ```sh
   curl -X POST https://osu.somtum.fun/oauth/token \
     -d client_id=YOUR_CLIENT_ID -d client_secret=YOUR_CLIENT_SECRET \
     -d grant_type=client_credentials -d scope=public
   ```

3. Send the token with every request:

   ```sh
   curl https://osu.somtum.fun/api/v2/users/2/osu \
     -H "Authorization: Bearer YOUR_TOKEN" -H "Accept: application/json"
   ```

To act for a player (read their friends, send chat messages, ...), use the authorization code grant with `/oauth/authorize`, as on osu!. Tokens last a day; get a new one when yours runs out.

What's different from osu.ppy.sh:

- Players, scores, ranks and pp are somtum.fun's. Beatmaps are osu!'s, plus sets uploaded here (their ids start at 10,000,000).
- Relax and Autopilot scores aren't in API v2's rankings or score lists, which only know osu!'s own mods; use the [bancho.py API](#bancho-py-api) for them.
- Rankings leave out players who haven't set a score in that mode for 180 days, until their next one.

## bancho.py API {id=bancho-py-api}

The public API of [bancho.py](https://github.com/osuAkatsuki/bancho.py) (the server somtum.fun ran on before), with the same paths, parameters and answers, so tools made for bancho.py servers keep working. No key is needed, and it only reads.

| | |
| :-- | :-- |
| Address | `https://api.somtum.fun/v1` |
| Also at | `https://osu.somtum.fun/bpy-api/v1` |

Modes are bancho.py's: `0` to `3` osu!, taiko, catch and mania; `4` to `6` Relax (osu!, taiko, catch); `8` Autopilot.

```sh
curl "https://api.somtum.fun/v1/get_player_info?id=2&scope=all"
curl "https://api.somtum.fun/v1/get_leaderboard?mode=4&sort=pp&limit=50"
```

| Endpoint | What it gives |
| :-- | :-- |
| `GET /get_player_info` | A player (`id` or `name`): `scope` = `info`, `stats`, `all` or `history` |
| `GET /get_player_scores` | A player's scores: `scope` = `recent`, `best` or `first`; `mode`, `mods`, `limit`, `include_loved`, `include_failed` |
| `GET /get_player_status` | Whether a player is online, and what they're doing |
| `GET /get_player_achievements` | A player's medals |
| `GET /get_player_most_played` | A player's most played beatmaps |
| `GET /get_player_count` | Players online and in total |
| `GET /search_players` | Players by name |
| `GET /get_leaderboard` | The rankings of a mode: `sort` = `pp`, `tscore`, `rscore`, `acc`, `plays` or `playtime`; `country` |
| `GET /get_map_info` | A beatmap (`id` or `md5`) |
| `GET /get_beatmapset_info` | A beatmap set |
| `GET /search_beatmaps` | Beatmaps by title, artist or mapper |
| `GET /get_map_scores` | A beatmap's leaderboard: `scope` = `best` or `recent` |
| `GET /get_score_info` | One score |
| `GET /get_replay` | One score's replay (`.osr`) |
| `GET /get_recent_scores` | The newest scores |
| `GET /get_top_osu_std_scores` | The best osu! scores (Vanilla, Relax and Autopilot) |
| `GET /get_top_play` | The best play of a mode |
| `GET /get_rank_one_history` | Who held #1 on a beatmap |
| `GET /get_clan`, `GET /get_clans_leaderboard` | Teams (bancho.py calls them clans) |
| `GET /get_recent_players`, `GET /get_all_users`, `GET /special_players` | Players: the newest, all of them, and staff |
| `GET /statistics`, `GET /get_total_scores` | Server totals |

A few things work a little differently from bancho.py: restricted players aren't found at all, osu! scores mix osu!(stable) and TumThai plays (a TumThai play's `score` is lazer's score), and Relax and Autopilot have no play time.
