# API

somtum.fun มี API สองแบบสำหรับเครื่องมือ บอต และเว็บไซต์ ทั้งสองเห็นเฉพาะผู้เล่นและคะแนนของ somtum.fun เท่านั้น ไม่มีข้อมูลจากบัญชีของ osu.ppy.sh

| | ที่อยู่ | สำหรับ |
| :-- | :-- | :-- |
| [API v2](#api-v2) | `https://osu.somtum.fun/api/v2` | ทุกอย่างที่เขียนสำหรับ API v2 ของ osu! |
| [bancho.py API](#bancho-py-api) | `https://api.somtum.fun/v1` | เครื่องมือและบอตที่เขียนสำหรับเซิร์ฟเวอร์ bancho.py |

**API v1** เก่าของ osu! (`/api/get_user?k=...` และอื่น ๆ) ไม่มีบน somtum.fun ให้ใช้ API v2 หรือ bancho.py API ซึ่งครอบคลุมสิ่งที่ v1 ทำได้เกือบทั้งหมด

โปรดใช้อย่างเบามือ: แคชเท่าที่ทำได้ และอย่าส่งเกินประมาณหนึ่งคำขอต่อวินาที เครื่องมือที่สร้างภาระให้เซิร์ฟเวอร์มากเกินไปอาจถูกบล็อก

## API v2 {id=api-v2}

นี่คือ API v2 ของ osu! ที่ให้บริการโดยเว็บไซต์ของเรา ไลบรารีและโค้ดที่เขียนสำหรับ osu.ppy.sh จึงใช้ได้เมื่อเปลี่ยนที่อยู่

| | |
| :-- | :-- |
| API | `https://osu.somtum.fun/api/v2` |
| ขอ token | `https://osu.somtum.fun/oauth/token` |
| ให้ผู้เล่นล็อกอิน | `https://osu.somtum.fun/oauth/authorize` |
| เอกสารอ้างอิง (ทุก endpoint) | [osu.somtum.fun/docs](https://osu.somtum.fun/docs/) |

1. สร้าง OAuth application ใน[การตั้งค่าบัญชี](/home/account/edit#oauth) (**New OAuth Application**) คุณจะได้ client id และ client secret เก็บ secret เป็นความลับ
2. ขอ token สำหรับข้อมูลสาธารณะ (ผู้เล่น คะแนน บีทแมพ อันดับ) ใช้ client credentials grant:

   ```sh
   curl -X POST https://osu.somtum.fun/oauth/token \
     -d client_id=YOUR_CLIENT_ID -d client_secret=YOUR_CLIENT_SECRET \
     -d grant_type=client_credentials -d scope=public
   ```

3. ส่ง token ไปกับทุกคำขอ:

   ```sh
   curl https://osu.somtum.fun/api/v2/users/2/osu \
     -H "Authorization: Bearer YOUR_TOKEN" -H "Accept: application/json"
   ```

ถ้าจะทำงานแทนผู้เล่น (อ่านรายชื่อเพื่อน ส่งข้อความแชท ฯลฯ) ให้ใช้ authorization code grant กับ `/oauth/authorize` เหมือนบน osu! token ใช้ได้หนึ่งวัน เมื่อหมดอายุให้ขอใหม่

สิ่งที่ต่างจาก osu.ppy.sh:

- ผู้เล่น คะแนน อันดับ และ pp เป็นของ somtum.fun บีทแมพเป็นของ osu! รวมกับเซ็ตที่อัปโหลดที่นี่ (id เริ่มที่ 10,000,000)
- คะแนน Relax และ Autopilot ไม่อยู่ในอันดับหรือรายการคะแนนของ API v2 ซึ่งรู้จักแค่ม็อดของ osu! เอง ให้ใช้ [bancho.py API](#bancho-py-api) แทน
- อันดับจะไม่รวมผู้เล่นที่ไม่ได้ทำคะแนนในโหมดนั้นมา 180 วัน จนกว่าจะเล่นครั้งถัดไป

## bancho.py API {id=bancho-py-api}

API สาธารณะของ [bancho.py](https://github.com/osuAkatsuki/bancho.py) (เซิร์ฟเวอร์ที่ somtum.fun เคยใช้) ด้วย path พารามิเตอร์ และผลลัพธ์เหมือนเดิม เครื่องมือที่ทำสำหรับเซิร์ฟเวอร์ bancho.py จึงใช้ต่อได้ ไม่ต้องใช้ key และอ่านได้อย่างเดียว

| | |
| :-- | :-- |
| ที่อยู่ | `https://api.somtum.fun/v1` |
| อีกที่อยู่ | `https://osu.somtum.fun/bpy-api/v1` |

โหมดเป็นแบบ bancho.py: `0` ถึง `3` คือ osu!, taiko, catch และ mania; `4` ถึง `6` คือ Relax (osu!, taiko, catch); `8` คือ Autopilot

```sh
curl "https://api.somtum.fun/v1/get_player_info?id=2&scope=all"
curl "https://api.somtum.fun/v1/get_leaderboard?mode=4&sort=pp&limit=50"
```

| Endpoint | ให้ข้อมูลอะไร |
| :-- | :-- |
| `GET /get_player_info` | ผู้เล่น (`id` หรือ `name`): `scope` = `info`, `stats`, `all` หรือ `history` |
| `GET /get_player_scores` | คะแนนของผู้เล่น: `scope` = `recent`, `best` หรือ `first`; `mode`, `mods`, `limit`, `include_loved`, `include_failed` |
| `GET /get_player_status` | ผู้เล่นออนไลน์อยู่ไหม และกำลังทำอะไร |
| `GET /get_player_achievements` | เหรียญของผู้เล่น |
| `GET /get_player_most_played` | บีทแมพที่ผู้เล่นเล่นบ่อยที่สุด |
| `GET /get_player_count` | จำนวนผู้เล่นออนไลน์และทั้งหมด |
| `GET /search_players` | ค้นหาผู้เล่นตามชื่อ |
| `GET /get_leaderboard` | อันดับของโหมด: `sort` = `pp`, `tscore`, `rscore`, `acc`, `plays` หรือ `playtime`; `country` |
| `GET /get_map_info` | บีทแมพ (`id` หรือ `md5`) |
| `GET /get_beatmapset_info` | เซ็ตบีทแมพ |
| `GET /search_beatmaps` | ค้นหาบีทแมพตามชื่อเพลง ศิลปิน หรือผู้ทำแมพ |
| `GET /get_map_scores` | ลีดเดอร์บอร์ดของบีทแมพ: `scope` = `best` หรือ `recent` |
| `GET /get_score_info` | คะแนนหนึ่งรายการ |
| `GET /get_replay` | รีเพลย์ของคะแนนหนึ่งรายการ (`.osr`) |
| `GET /get_recent_scores` | คะแนนล่าสุด |
| `GET /get_top_osu_std_scores` | คะแนน osu! ที่ดีที่สุด (Vanilla, Relax และ Autopilot) |
| `GET /get_top_play` | การเล่นที่ดีที่สุดของโหมด |
| `GET /get_rank_one_history` | ใครเคยครองอันดับ 1 ของบีทแมพ |
| `GET /get_clan`, `GET /get_clans_leaderboard` | ทีม (bancho.py เรียกว่า clan) |
| `GET /get_recent_players`, `GET /get_all_users`, `GET /special_players` | ผู้เล่น: ล่าสุด ทั้งหมด และทีมงาน |
| `GET /statistics`, `GET /get_total_scores` | ยอดรวมของเซิร์ฟเวอร์ |

บางอย่างทำงานต่างจาก bancho.py เล็กน้อย: ค้นหาผู้เล่นที่ถูกจำกัดไม่เจอเลย คะแนน osu! รวมการเล่นจาก osu!(stable) และ TumThai (`score` ของการเล่นใน TumThai เป็นคะแนนแบบ lazer) และ Relax กับ Autopilot ไม่มีเวลาเล่น
