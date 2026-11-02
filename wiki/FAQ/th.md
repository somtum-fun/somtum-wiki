# คำถามที่พบบ่อย (FAQ)

คำตอบของคำถามที่เราได้ยินบ่อยที่สุด หาคำตอบไม่เจอ? ดู[ศูนย์ช่วยเหลือ](/wiki/Help_centre)

## somtum.fun คืออะไร? {id=what-is-somtum-fun}

somtum.fun เป็นเซิร์ฟเวอร์ส่วนตัวของเกมจังหวะ osu! ที่แฟน ๆ ดูแลกันเอง มีบัญชี อันดับ บีทแมพ และชุมชนของตัวเอง ไม่มีส่วนเกี่ยวข้องกับ ppy Pty Ltd และบัญชีกับคะแนนของคุณบน osu.ppy.sh จะไม่ถูกแชร์มาที่นี่ เราใช้ซอฟต์แวร์เซิร์ฟเวอร์ของเราเอง ไม่ใช่ bancho.py หรือ g0v0 ดู[ทำไมต้อง somtum.fun?](/wiki/Why_somtum.fun)

## เชื่อมต่ออย่างไร? {id=how-do-i-connect}

ไฟล์ทั้งหมดอยู่ใน[หน้าดาวน์โหลด](/home/download) วิธีที่ง่ายที่สุดคือ **Somtum Launcher** ซึ่งติดตั้งและอัปเดตทุกอย่างด้านล่าง และเปิดเกมให้คุณ

- **TumThai** คือ osu!lazer เวอร์ชันของเรา สำหรับ Windows, Linux, macOS และ Android ติดตั้ง (หรือแตกไฟล์เวอร์ชันพกพา) แล้วล็อกอิน มันอัปเดตตัวเอง บน Android และคอมสเปกต่ำแนะนำ **TumThai!Next**
- **osu!(stable):** เปิด osu!(stable) ของคุณด้วย **Somtum Patcher** (หรือจาก Somtum Launcher)
- **ไคลเอนต์รุ่นเก่า (2008 ถึง 2015):** ดาวน์โหลดไคลเอนต์รุ่นเก่าที่เราสร้างใหม่ แตกไฟล์ไว้ที่ไหนก็ได้ แล้วเปิด `osu!.exe` เก็บ `pkms.dll` (ระบบกันโกงของเรา) ไว้ข้าง `osu!.exe` ไม่เช่นนั้นคะแนนจะไม่ถูกส่ง ต้องใช้ Windows และ .NET Framework 3.5 (บางรุ่นปี 2015 ใช้ .NET Framework 4) หารุ่นที่ต้องการไม่เจอ? ขอได้ใน [Discord](https://discord.gg/U6Ztb3mRyz) หรือใน[ฟอรัม](/community/forums/4)

**ส่งคะแนนได้เฉพาะวิธีเหล่านี้** ตั้งแต่ตุลาคม 2026 ระบบกันโกงของเราตรวจทุกไคลเอนต์ที่เล่นที่นี่ และมีแค่ Somtum Launcher, Somtum Patcher, TumThai และไคลเอนต์รุ่นเก่าที่เราสร้างใหม่เท่านั้นที่ผ่าน คุณยังเชื่อมต่อด้วยวิธีอื่นได้ ล็อกอิน แชท เล่น และเข้ามัลติเพลเยอร์ได้ แต่**คะแนนจะไม่ถูกส่ง** เพราะระบบกันโกงตรวจสอบไคลเอนต์เหล่านั้นไม่ได้:

1. **`-devserver`:** osu!(stable) ที่เปิดด้วย `-devserver somtum.fun` (โดยไม่ใช้ Somtum Patcher) ยังเชื่อมต่อ somtum.fun ได้ แต่คะแนนไม่ถูกส่ง
2. **ไคลเอนต์ที่คุณดัดแปลงเอง:** ไคลเอนต์ที่คุณแพตช์หรือสร้างเอง (เช่นแบบที่ไคลเอนต์ของ Titanic เชื่อมต่อกับ Titanic) ก็เชื่อมต่อ somtum.fun ได้ แต่คะแนนไม่ถูกส่งเช่นกัน รวมถึงไคลเอนต์ lazer ตัวอื่นที่ชี้มาที่ somtum.fun (เช่นของ g0v0 หรือ osu!lazer ที่ใช้ LazerAuthlibInjection) การตั้งค่าอยู่ใน[การเชื่อมต่อด้วยไคลเอนต์ lazer ตัวอื่น](#other-lazer-clients)

**ไคลเอนต์รุ่นเก่า (2008 ถึง 2015) ต่างออกไป:** ล็อกอินได้เฉพาะไคลเอนต์รุ่นเก่าที่เราสร้างใหม่เท่านั้น รุ่นต้นฉบับ (จะใช้ hook หรือไม่ก็ตาม) หรือรุ่นที่คุณดัดแปลงหรือสร้างใหม่เอง จะขึ้น ["This old osu! build can't play on somtum.fun as it is"](#error-old-build) และเชื่อมต่อไม่ได้

ทั้งหมดนี้เพื่อให้อันดับยุติธรรมกับทุกคน ถ้าเครื่องของคุณใช้ตัวไหนของเราไม่ได้เลย บอกเราใน [Discord](https://discord.gg/U6Ztb3mRyz)

## TumThai: นำบีทแมพและรีเพลย์จาก osu!lazer มาใช้ {id=tumthai-import}

TumThai ใช้บีทแมพ สกิน และรีเพลย์ที่คุณมีอยู่แล้วใน osu!lazer ได้ ใน TumThai เปิด **Settings → Maintenance → Change folder location** แล้วเลือกโฟลเดอร์ osu!lazer ของคุณ:

- Windows: `%AppData%\osu`
- Linux: `~/.local/share/osu`
- macOS: `~/Library/Application Support/osu`

จากนั้น TumThai จะอ่านโฟลเดอร์นั้นแทนโฟลเดอร์ของตัวเอง จึงต้องปิด osu!lazer ก่อน ถ้าจะย้ายกลับ ให้เลือกโฟลเดอร์อื่นด้วยวิธีเดียวกัน

## เล่นรูลเซ็ตเสริมได้ไหม? {id=custom-rulesets}

ได้ ใน TumThai บน Windows, Linux และ macOS และใน TumThai!Next บน Android: sentakki, Tau, Rush!, osu!fps และอื่น ๆ แต่ละตัวมีลีดเดอร์บอร์ดและอันดับตามคะแนนของตัวเอง ติดตั้งได้ที่ **Settings → General → Custom rulesets** ดูรายการทั้งหมดและวิธีนับคะแนนได้ที่[รูลเซ็ตเสริม](/wiki/Custom_rulesets)

## การเชื่อมต่อด้วยไคลเอนต์ lazer ตัวอื่น {id=other-lazer-clients}

ใช้ไคลเอนต์ของ g0v0 ไคลเอนต์ที่สร้างจาก lazer ตัวอื่น หรือ osu!lazer กับ LazerAuthlibInjection? กรอกค่าเหล่านี้:

| การตั้งค่า | ค่า |
|---|---|
| API URL | `https://osu.somtum.fun` |
| Website URL | `https://osu.somtum.fun` |
| Client ID | `5` |
| Client Secret | `FGc9GAtyHzeQDshWP5Ah7dega8hJACAJpQtw6OXk` |
| Spectator URL | `https://spectator.somtum.fun/spectator` |
| Multiplayer URL | `https://spectator.somtum.fun/multiplayer` |
| Metadata URL | `https://spectator.somtum.fun/metadata` |
| Beatmap Submission Service URL | `https://osu.somtum.fun/beatmap-submission` |
| Non-g0v0 server | **เปิด** (ติ๊กถูก) |

คุณล็อกอิน แชท ดูคนอื่นเล่น และเล่นมัลติเพลเยอร์ได้ แต่**ส่งคะแนนไม่ได้เลย**บนไคลเอนต์เหล่านี้ ถ้าอยากให้คะแนนนับ ให้เล่นบน [TumThai](#how-do-i-connect)

## แอนตี้ไวรัสหรือ Windows เตือนเรื่องไฟล์ของเรา {id=antivirus}

ไฟล์ของเราไม่ได้เซ็นโค้ด การเซ็นมีค่าใช้จ่ายมากกว่า 11,000 บาทต่อปี ซึ่งมากเกินไปสำหรับเซิร์ฟเวอร์ชุมชนที่เล่นฟรี Windows จึงอาจขึ้นว่า "Windows protected your PC" (คลิก **More info** แล้วคลิก **Run anyway**) และแอนตี้ไวรัสอาจบล็อกหรือลบ Somtum Launcher, Somtum Patcher, `pkms.dll`, TumThai หรือไคลเอนต์รุ่นเก่าโดยเข้าใจผิด ให้เพิ่มข้อยกเว้นให้โฟลเดอร์ของโปรแกรมเหล่านี้ ดูขั้นตอนได้ที่[แอนตี้ไวรัสหรือ Windows บล็อกการดาวน์โหลด](/wiki/Help_centre/Common_problems#antivirus) ทำแบบนี้เฉพาะกับไฟล์จาก[หน้าดาวน์โหลด](/home/download) ของเราเท่านั้น

## สมัครบัญชีอย่างไร? {id=registration}

สมัครในเกม: เปิด TumThai หรือ osu!(stable) บน somtum.fun แล้วสมัครในเกม ไม่ใช่บนเว็บไซต์ จากนั้นล็อกอินเว็บไซต์นี้ด้วยชื่อและรหัสผ่านเดียวกัน

มาใหม่และยังไม่ได้ติดตั้งอะไร? คุณสมัครจาก osu!(stable) ที่เปิดด้วย `-devserver somtum.fun` หรือจากไคลเอนต์ lazer ตัวอื่นที่ชี้มาที่ somtum.fun ก็ได้ แต่จำไว้ว่า**ส่งคะแนนไม่ได้เลย**จนกว่าจะเล่นบนไคลเอนต์ทางการของเรา: TumThai, osu!(stable) ผ่าน Somtum Launcher (หรือ Somtum Patcher) หรือไคลเอนต์รุ่นเก่าของเรา ดู[เชื่อมต่ออย่างไร?](#how-do-i-connect)

คุณมีได้**บัญชีเดียว** การสมัครผ่าน VPN พร็อกซี Tor หรือเครือข่ายโฮสติ้งจะถูกบล็อก และแต่ละเครือข่ายสร้างบัญชีได้วันละหนึ่งบัญชี ถ้าข้อนี้ทำให้คุณสมัครอย่างสุจริตไม่ได้ อีเมลมาที่ [accounts@somtum.fun](mailto:accounts@somtum.fun)

## เล่นฟรีไหม? {id=is-it-free}

ฟรี Supporter tag เป็นตัวเลือกเสริม และช่วยจ่ายค่าเซิร์ฟเวอร์

## Relax และ Autopilot {id=relax-and-autopilot}

Relax และ Autopilot มีลีดเดอร์บอร์ด อันดับ และ pp แยกจากการเล่นปกติ ทั้งใน TumThai และ osu!(stable) เลือกได้ในหน้าอันดับและในลีดเดอร์บอร์ดของแมพ pp ของทั้งสองคำนวณด้วยตัวคำนวณอื่น ดู [Performance points](/wiki/Performance_points) และ [Relax และ Autopilot](/wiki/Relax_and_Autopilot)

## ผูกบัญชี Discord อย่างไร? {id=discord-link}

ผูกครั้งเดียว วิธีไหนก็ได้: ใน[การตั้งค่าบัญชี](/home/account/edit#connections) ใต้หัวข้อ **Connections** หรือใช้คำสั่ง `/link` กับบอต Discord ของเรา (จะได้โค้ดไปส่งให้ LimeBot) ทั้งสองวิธีผูกแบบเดียวกัน ดังนั้น**ถ้าผูก Discord บนเว็บไซต์แล้ว ไม่ต้องใช้ `/link` อีก** ดู [Linking Discord](/wiki/Map_of_the_day#linking-discord)

## ภารกิจรายวันกับแมพประจำวันคืออะไร? {id=daily}

[ภารกิจรายวัน (daily challenge)](/wiki/Daily_challenge) คือแมพใหม่ทุกวันในห้องหนึ่งใน TumThai จัดอันดับตามคะแนน ส่วน[แมพประจำวัน (map of the day)](/wiki/Map_of_the_day) คือแมพประจำวันของบอต Discord ของเรา คนที่ผ่านด้วย pp สูงสุดได้ role ใน Discord หนึ่งสัปดาห์ [ต่างกันอย่างไร](/wiki/Daily_challenge#map-of-the-day)

## เล่นบีทแมพไหนได้บ้าง? {id=beatmaps}

ทุกบีทแมพของ osu! โดยมีสถานะแรงก์เหมือนบน osu! รวมถึงแมพที่ผู้ทำแมพของเราส่งมาที่นี่ ดาวน์โหลดแมพในเกม (osu!direct) หรือจาก[รายการบีทแมพ](/beatmapsets)

## ทำไมคะแนนไม่ถูกส่ง? {id=score-not-submitted}

ทุกการเล่นบนบีทแมพที่เซิร์ฟเวอร์รู้จักจะถูกส่งและบันทึกพร้อมรีเพลย์ ไม่ว่าแมพจะมีสถานะอะไร สถานะแค่กำหนดว่าคุณจะได้อะไรจากการเล่นนั้น เหมือนบน osu!:

| สถานะแมพ | ลีดเดอร์บอร์ด | pp |
| :-- | :-- | :-- |
| Ranked, Approved | ได้ | ได้ |
| Qualified | ได้ | ไม่ได้ แมพ Qualified จะได้แรงก์หลังผ่านไป 1 วัน (ดู[คิวแรงก์](/wiki/Beatmap_ranking_procedure/Ranking_queue)) |
| Loved | ได้ | ไม่ได้ |
| Pending, WIP, Graveyard | ไม่ได้ | ไม่ได้ |

ดังนั้นการเล่นบนแมพที่ไม่ได้แรงก์แล้วไม่ได้อะไรเลย *ถูกส่งแล้ว* เพียงแต่ไม่นับในอันดับ

คะแนนจะไม่ถูกส่งจริง ๆ ก็ต่อเมื่อ:

- **TumThai ของคุณเป็นเวอร์ชันเก่า** อัปเดตจาก[หน้าดาวน์โหลด](/home/download) (TumThai ที่ติดตั้งไว้จะอัปเดตตัวเอง)
- **Somtum Patcher หรือไคลเอนต์รุ่นเก่าของคุณเก่าหรือเสียหาย** ดาวน์โหลดใหม่จาก[หน้าดาวน์โหลด](/home/download) หรือ Somtum Launcher ปกติเกมจะบอกเหตุผล ดู[ข้อความแจ้งข้อผิดพลาด](#errors)
- **บีทแมพไม่มีบนเซิร์ฟเวอร์** เช่นแมพที่คุณทำเองแต่ไม่เคยส่ง
- **คุณเชื่อมต่อด้วยวิธีอื่น** ที่ไม่ใช่ Somtum Launcher, Somtum Patcher, TumThai หรือไคลเอนต์รุ่นเก่าของเรา (เช่น `-devserver` ไคลเอนต์ที่ดัดแปลงเอง g0v0 หรือ LazerAuthlibInjection) ดู[เชื่อมต่ออย่างไร?](#how-do-i-connect)

ถ้าบัญชีของคุณถูกจำกัด (restricted) คะแนนยังถูกบันทึก แต่จะซ่อนจากคนอื่น มีแค่คุณที่เห็น (ดู[การลงโทษและการอุทธรณ์](/legal/th/Restrictions))

## บัญชีถูกจำกัด (restricted) ต้องทำอย่างไร? {id=restricted}

อ่าน[การลงโทษและการอุทธรณ์](/legal/th/Restrictions) ถ้าคิดว่าเป็นความผิดพลาด อีเมลมาที่ [support@somtum.fun](mailto:support@somtum.fun)

## การเล่นกับ Somtum Patcher {id=somtum-patcher}

Somtum Patcher เปิด osu!(stable) บน somtum.fun และดูแลให้การเล่นยุติธรรม ระหว่างที่มันทำงาน:

- **อย่ารันโปรแกรมอ่านหน่วยความจำหรือโปรแกรมโกง** (Cheat Engine, osu! trainer, pattern scanner, timing-rate hack, auto-clicker, โปรแกรมแก้รีเพลย์ และอื่น ๆ ทำนองนี้) Patcher คอยดูหน่วยความจำและ process handle ของ osu! ถ้าเจอ คะแนนของคุณจะถูกปฏิเสธ และบัญชีอาจถูกจำกัด
- **อย่าเกาะ debugger กับ osu!.exe** Patcher ถือว่า debugger คือการแทรกแซง ถ้าแค่อยากลอง ให้ปิด debugger ก่อนเปิดเกม
- **โอเวอร์เลย์อย่าง Discord, MSI Afterburner หรือ RivaTuner ใช้ได้** Patcher จับเฉพาะโปรแกรมที่อ่านหรือเขียนหน่วยความจำของ osu! เอง
- **โปรแกรมสตรีมและอัดหน้าจอใช้ได้** (OBS, ShadowPlay, โอเวอร์เลย์ของ NVIDIA/AMD) เพราะไม่ยุ่งกับเกม
- **ไดรเวอร์แท็บเล็ตใช้ได้** (OpenTabletDriver, Wacom, Huion, XP-Pen) แต่ฟิลเตอร์และปลั๊กอินบางตัวของ OpenTabletDriver ไม่อนุญาต ดู[ฟิลเตอร์แท็บเล็ต](/wiki/Rules/Tablet_filters)
- **ReShade และโปรแกรม shader อื่น ๆ ไม่อนุญาต** รวมถึงอะไรก็ตามที่คุณเพิ่มเข้าไปในโฟลเดอร์ osu! ReShade ทำงานโดยวางไฟล์ `opengl32.dll`, `d3d9.dll` หรือ `dxgi.dll` ของตัวเองไว้ข้าง `osu!.exe` แบบเดียวกับที่โปรแกรมโกงบางตัวใช้ ถ้ามีไฟล์เหล่านี้อยู่ คะแนนจะไม่ถูกส่ง ให้ลบออกแล้วเปิด osu! ใหม่ DLL อื่นที่ไม่ใช่ส่วนหนึ่งของ osu! ถือเป็นการโกง

ถ้าคุณไม่ได้ใช้อะไรพวกนี้เลยแต่คะแนนยังถูกปฏิเสธ อีเมลมาที่ [support@somtum.fun](mailto:support@somtum.fun) จากอีเมลของบัญชี พร้อมชื่อผู้ใช้และเวลาที่เล่นโดยประมาณ แล้วเราจะตรวจสอบให้

## osu!dan คืออะไร? {id=osu-dan}

คอร์สแมพ osu!mania ยาว ๆ จาก DanReform ผ่านด้วยความแม่นยำ 96% โดยไม่หยุดเกม แล้วจะถูกบันทึกในประวัติของคุณ ดูกติกาที่ [osu!dan](/wiki/osu!dan) และดูคอร์สได้ที่[หน้า osu!dan](/community/dan)

## ได้ฉายาหรือป้ายกลุ่มอย่างไร? {id=titles-and-groups}

ทีมงานเป็นคนให้ ดู[ฉายาผู้ใช้](/wiki/People/User_title) และ[กลุ่มผู้ใช้](/wiki/People/User_groups)

## เปลี่ยนชื่อผู้ใช้ได้ไหม? {id=username}

ได้ บนเว็บไซต์: [Username change](/store/products/username-change) (ในร้านค้า) ทุกคนเปลี่ยนได้ฟรี 5 ครั้งทุก 30 วัน และ [Somtum Supporter](/home/support) เปลี่ยนได้ไม่จำกัด บางชื่อใช้ไม่ได้ (ทีมงานมีรายการชื่อที่ถูกบล็อก)

ถ้าใช้ไม่ได้ อีเมลมาที่ [accounts@somtum.fun](mailto:accounts@somtum.fun) จากอีเมลของบัญชี

## รายงานบั๊กหรือผู้เล่นที่ไหน? {id=reporting}

รายงานผู้เล่นด้วยปุ่มรายงานในเกมหรือในหน้าโปรไฟล์ รายงานบั๊กได้ใน [Discord](https://discord.gg/U6Ztb3mRyz) ของเรา ถ้าเป็นเรื่องร้ายแรง ดู[รายงานการกระทำที่ไม่เหมาะสม](/wiki/Reporting_bad_behaviour/Abuse)

## ข้อความแจ้งข้อผิดพลาด {id=errors}

ความหมายของข้อความที่อาจเห็นในเกม และวิธีแก้ (ข้อความในเกมเป็นภาษาอังกฤษ เราจึงใส่ไว้ตามต้นฉบับ)

### "Authentication failed" หรือ "Incorrect password" {id=error-login}

ตรวจชื่อผู้ใช้และรหัสผ่าน ซึ่งเหมือนกับบนเว็บไซต์นี้ ลืมรหัสผ่าน? [รีเซ็ตที่นี่](/home/password-reset) การสมัครทำในเกม ไม่ใช่บนเว็บไซต์ (ดู[สมัครบัญชีอย่างไร?](#registration))

### "This is a new device, so it needs confirming first" {id=error-new-device}

คุณล็อกอินจากคอมหรือเครือข่ายที่บัญชีของคุณไม่เคยใช้ ล็อกอินเว็บไซต์นี้ เปิด[หน้ายืนยันตัวตน](/p/verify) แล้วยืนยันอุปกรณ์ จากนั้นล็อกอินเกมอีกครั้ง

### "This version of osu! can't confirm a new device" {id=error-new-device-old-client}

รุ่นเก่าแสดงหน้ายืนยันไม่ได้ ให้ยืนยันอุปกรณ์ที่[หน้ายืนยันตัวตน](/p/verify) ก่อน แล้วล็อกอินอีกครั้ง ถ้ายังไม่ได้ ให้ใช้ TumThai หรือ Somtum Patcher จาก[หน้าดาวน์โหลด](/home/download)

### "This old osu! build can't play on somtum.fun as it is" {id=error-old-build}

ไคลเอนต์ปี 2008-2015 ล็อกอินได้เฉพาะรุ่นที่เราสร้างใหม่เท่านั้น รุ่นต้นฉบับ (จะใช้ hook หรือไม่ก็ตาม) หรือรุ่นที่คุณดัดแปลงเองล็อกอินไม่ได้ ดาวน์โหลดรุ่นเดียวกันที่แพตช์แล้วจาก[หน้าดาวน์โหลด](/home/download) ถ้าไม่มี ขอได้ใน [Discord](https://discord.gg/U6Ztb3mRyz) หรือใน[ฟอรัม](/community/forums/4)

### "Something on your computer isn't allowed while playing here (a debugger or a cheat tool)" {id=error-cheat-tool}

มีโปรแกรมที่อ่านหรือแก้หน่วยความจำของ osu! ทำงานอยู่ (ดู[การเล่นกับ Somtum Patcher](#somtum-patcher)) ปิดโปรแกรมนั้นแล้วล็อกอินอีกครั้ง

### "Score submission is disabled: your Somtum Patcher isn't running" หรือ "didn't respond in time" {id=error-patcher-not-running}

osu!(stable) ถูกเปิดโดยไม่ผ่าน Somtum Patcher หรือ Patcher ถูกปิดหรือหยุดทำงานระหว่างเล่น ปิด osu! แล้วเปิดใหม่ผ่าน Somtum Patcher หรือ Somtum Launcher

### "Score submission is disabled: your Somtum Patcher failed the integrity check" {id=error-patcher-integrity}

ไฟล์ของ Patcher ถูกแก้หรือเสียหาย (บางครั้งแอนตี้ไวรัสทำ) ดาวน์โหลดใหม่จาก[หน้าดาวน์โหลด](/home/download) แล้วติดตั้งใหม่ ถ้าแอนตี้ไวรัสลบมัน ให้เพิ่มข้อยกเว้นให้โฟลเดอร์ของ Patcher

### "Your anti-cheat is out of date — score submission is disabled" {id=error-anticheat-outdated}

คุณเล่นได้ แต่ Somtum Patcher หรือไคลเอนต์รุ่นเก่าของคุณมีระบบกันโกงเวอร์ชันที่เราไม่รับแล้ว ดาวน์โหลด Somtum Patcher ตัวล่าสุดจาก[หน้าดาวน์โหลด](/home/download) (หรือให้ Somtum Launcher อัปเดต) หรือดาวน์โหลดไคลเอนต์รุ่นเก่าของคุณใหม่ แล้วเปิด osu! อีกครั้ง

### ไคลเอนต์รุ่นเก่า: "Score submission is disabled: the anti-cheat isn't running", "didn't respond in time", "failed the integrity check" หรือ "is out of date" {id=error-legacy-anticheat}

ไคลเอนต์รุ่นเก่าของเราโหลดระบบกันโกง `pkms.dll` จากโฟลเดอร์ของมันเอง และคะแนนต้องใช้ไฟล์นี้ ตรวจว่า `pkms.dll` ยังอยู่ข้าง `osu!.exe` (บางครั้งแอนตี้ไวรัสลบไป ให้เพิ่มข้อยกเว้นให้โฟลเดอร์) แล้วเปิด `osu!.exe` ใหม่ ถ้ายังไม่ได้ หรือข้อความบอกว่าเป็นเวอร์ชันเก่า ให้ดาวน์โหลดรุ่นของคุณใหม่จาก[หน้าดาวน์โหลด](/home/download) แล้วแตกไฟล์ไว้ในโฟลเดอร์ใหม่

### "Score submission is disabled: a file next to osu!.exe replaces part of Windows" {id=error-proxy-dll}

มีไฟล์อย่าง `opengl32.dll`, `d3d9.dll`, `dxgi.dll`, `dinput8.dll` หรือ `version.dll` อยู่ในโฟลเดอร์ osu! ของคุณ ไฟล์เหล่านี้มาจาก ReShade หรือโปรแกรมคล้ายกันซึ่งไม่อนุญาต (ดู[การเล่นกับ Somtum Patcher](#somtum-patcher)) ลบไฟล์นั้นออกจากโฟลเดอร์ osu! แล้วเปิด osu! ใหม่ กรณีนี้คุณไม่ได้ทำผิดอะไร

### ไคลเอนต์รุ่นเก่า: "Score submission is disabled: this osu! folder doesn't match our download" {id=error-legacy-files}

มีไฟล์ของไคลเอนต์รุ่นเก่าที่ไม่ตรงกับที่เราปล่อย: ถูกแก้ ถูกแทนที่ หรือมาจากเวอร์ชันอื่น ดาวน์โหลดรุ่นของคุณใหม่จาก[หน้าดาวน์โหลด](/home/download) แล้วแตกไฟล์ไว้ในโฟลเดอร์ใหม่ที่ว่างเปล่า

### "Your Somtum Patcher is out of date" {id=error-patcher-outdated}

ดาวน์โหลด Somtum Patcher ตัวล่าสุดจาก[หน้าดาวน์โหลด](/home/download) เวอร์ชันเก่าจะส่งคะแนนไม่ได้หลังจากมีเวอร์ชันใหม่ออกมาได้สักพัก

### osu! ปิดตัวพร้อมข้อความ "[pkms] integrity violation in 'net': server rejected flag: revoked_version" {id=error-pkms-revoked}

Somtum Patcher ของคุณเป็นเวอร์ชันที่เราไม่รับแล้ว (มักเป็นเพราะเวอร์ชันใหม่แก้ปัญหาบางอย่าง) เกมจึงหยุดเพื่อไม่ให้เล่นบนเวอร์ชันนั้น ดาวน์โหลด Somtum Patcher ตัวล่าสุดจาก[หน้าดาวน์โหลด](/home/download) หรือให้ Somtum Launcher อัปเดตตัวเอง แล้วเปิด osu! ใหม่ คุณไม่ได้ทำผิดอะไร

### osu! ปิดตัวพร้อมข้อความ "[pkms] integrity violation in 'net': pkms: launched outside injector" {id=error-pkms-outside}

ระบบกันโกงถูกโหลดโดยที่ Somtum Patcher ไม่ได้เป็นคนเปิด osu! เกิดขึ้นเมื่อ osu! รีสตาร์ตตัวเอง (หลังอัปเดต osu! หรือจากตัวเลือกของมันเอง) ขณะที่ Patcher ยังเกาะอยู่ ปิด osu! แล้วเปิดใหม่ผ่าน Somtum Patcher หรือ Somtum Launcher

### osu! ปิดตัวพร้อมข้อความ "[pkms] integrity violation in 'net': network worker terminated unexpectedly" {id=error-pkms-network}

ส่วนของระบบกันโกงที่คุยกับเซิร์ฟเวอร์ของเราถูกหยุด ส่วนใหญ่เป็นเพราะแอนตี้ไวรัสหรือไฟร์วอลล์ อนุญาตโฟลเดอร์ของ Somtum Patcher ในแอนตี้ไวรัส ปิดโปรแกรมที่ยุ่งกับ osu! แล้วเปิด osu! ใหม่ผ่าน Patcher

### osu! ปิดตัวพร้อมข้อความ "[pkms] violation handler patched", "unreadable" หรือ "stalled; failing closed" {id=error-pkms-handler}

มีบางอย่างแก้หรือทำให้ระบบกันโกงใน osu! ค้าง ปิดโปรแกรมที่อ่านหรือเขียนหน่วยความจำของ osu! (ดู[การเล่นกับ Somtum Patcher](#somtum-patcher)) แล้วเปิด osu! ใหม่ผ่าน Patcher ถ้าคุณไม่ได้รันอะไรแบบนั้นเลย อีเมลมาที่ [support@somtum.fun](mailto:support@somtum.fun) พร้อมชื่อผู้ใช้ เวลาที่เกิดโดยประมาณ และชื่อแอนตี้ไวรัสของคุณ

### ข้อความ "[pkms] integrity violation in '…'" แบบอื่น ๆ {id=error-pkms-other}

ระบบกันโกงเจอบางอย่างกำลังแก้ osu! ระหว่างทำงาน จึงปิดเกม ปิดโปรแกรมที่มันเจอ แล้วเปิด osu! ใหม่ผ่าน Patcher ถ้าเกิดซ้ำและไม่รู้สาเหตุ อีเมลมาที่ [support@somtum.fun](mailto:support@somtum.fun) พร้อมภาพหน้าจอของข้อความ

### "osu! did not finish starting within 10 seconds and has been closed" {id=error-patcher-start}

osu! ค้างระหว่างเปิด (มักเป็นตอนกำลังอัปเดต หรือตอนแอนตี้ไวรัสกำลังสแกน) เปิด `osu!.exe` เองหนึ่งครั้ง รอจนถึงเมนูหลัก ปิด แล้วใช้ Somtum Patcher อีกครั้ง ถ้ายังเกิดซ้ำ ให้ลบไฟล์แคชของตัวอัปเดตและ launcher ของ osu! ในโฟลเดอร์ osu!

### "Still verifying your client — hold on" {id=error-patcher-verifying}

ไม่ใช่ข้อผิดพลาด Patcher กำลังตรวจสอบกับเซิร์ฟเวอร์ของเรา อาจใช้เวลาถึง 45 วินาที โดยเฉพาะบน Linux ที่ใช้ Wine รอจนขึ้น "Client verified"

### "Your computer has traces of hq!osu's multi-account tool (relife)" {id=error-relife}

osu! เจอ relife ใน registry ของ Windows ปิด relife (หรือติดตั้งใหม่แล้วปิด) เพื่อไม่ให้เจออีก นี่เป็นแค่คำเตือน ไม่ใช่การจำกัดบัญชี

### "Please contact staff directly to create an account" {id=error-contact-staff}

มีการสร้างบัญชีใหม่บนคอมเครื่องเดียวกับบัญชีที่ถูกจำกัด ถ้าเป็นคอมที่ใช้ร่วมกันหรือคอมของครอบครัว และคุณไม่ใช่ผู้เล่นที่ถูกจำกัด อีเมลมาที่ [accounts@somtum.fun](mailto:accounts@somtum.fun) พร้อมชื่อผู้ใช้ทั้งสองบัญชี

### "This account is locked. Please contact staff." {id=error-locked}

ทีมงานล็อกบัญชีนี้ไว้ อีเมลมาที่ [support@somtum.fun](mailto:support@somtum.fun) จากอีเมลของบัญชี

### "You are banned" {id=error-banned}

บัญชีของคุณ หรือบัญชีอื่นบนคอมของคุณ ถูกแบน ปกติเราไม่ค่อยแบนผู้เล่น ปัญหาส่วนใหญ่จบที่การจำกัดบัญชี การแบนใช้เฉพาะเมื่อจำเป็นจริง ๆ หรือปัญหาร้ายแรงมาก บัญชีที่ถูกแบนล็อกอินเกมและเว็บไซต์นี้ไม่ได้ และการแบนครอบคลุมทั้งคอมและบัญชี osu! จะลืมรหัสผ่านที่บันทึกไว้และไม่พยายามล็อกอินเป็นเวลาหนึ่งวัน โปรดอย่าสร้างบัญชีใหม่ เพราะก็จะเข้าไม่ได้เช่นกัน ถ้าคิดว่าเป็นความผิดพลาด (เช่นใช้คอมร่วมกัน) อีเมลมาที่ [accounts@somtum.fun](mailto:accounts@somtum.fun)

### ถูกแบนที่นี่ แต่อยากเล่นเซิร์ฟเวอร์อื่น {id=error-banned-other-server}

การแบนทำให้ osu! ไม่ยอมล็อกอินทุกเซิร์ฟเวอร์เป็นเวลาหนึ่งวัน เพราะมันบันทึกค่าไว้ใน `osu!.db` ถ้าจะลบ ต้องใช้ Somtum Launcher 1.0.3 ขึ้นไป (1.0.4 บน Linux):

1. ปิด osu!
2. ใน Somtum Launcher เปิด **Settings → Advanced options** แล้วกด **Check for a ban flag**
3. ถ้าเจอ ให้กด **Remove the ban flag** ระบบจะสำรอง `osu!.db` ไว้ก่อนเป็น `osu!.db.bak`

ใน terminal ใช้ `somtum-launcher.exe --ban-flag --remove` บน Windows และ `somtum ban-flag --remove` บน Linux

วิธีนี้แก้แค่ในคอมของคุณ ไม่ได้ยกเลิกการแบนบน somtum.fun คุณยังล็อกอินที่นี่ไม่ได้

### "This account has been deleted" {id=error-deleted}

บัญชีถูกลบตามคำขอหรือโดยทีมงาน ถ้าคิดว่าเป็นความผิดพลาด อีเมลมาที่ [accounts@somtum.fun](mailto:accounts@somtum.fun)

### "Bot accounts can't log in to the game" {id=error-bot}

นี่คือ[บัญชีบอต](/wiki/Bot_account) ซึ่งแชทผ่าน IRC ได้อย่างเดียว ให้ล็อกอินเกมด้วยบัญชีของคุณเอง

### "This account has too many tournament client windows open" {id=error-tournament-windows}

ปิดหน้าต่างของ tournament client บางหน้าต่างแล้วลองใหม่ (ดู [Tournament client](/wiki/Tournaments/Tournament_client))

### osu!dan: "this attempt won't count as a clear" {id=error-dan}

คะแนนของคุณถูกบันทึกตามปกติ แค่ไม่นับเป็นการผ่าน dan ดูเหตุผลแต่ละข้อได้ที่ [osu!dan](/wiki/osu!dan#not-a-clear)

### osu!dan: "This beatmap is part of osu!dan, which can't be played in multiplayer or playlists" {id=error-dan-lazer}

TumThai (osu!lazer) แสดงข้อความนี้ใต้ "Score will not be submitted" เมื่อห้องมัลติเพลเยอร์หรือ playlist มีแมพจากคอร์ส [osu!dan](/wiki/osu!dan#lazer) แมพ dan เล่นได้แค่แบบเดี่ยว การเล่นนั้นจึงไม่ถูกบันทึก ให้เล่นแมพนั้นแบบเดี่ยว (พร้อมม็อด Classic) แทน
