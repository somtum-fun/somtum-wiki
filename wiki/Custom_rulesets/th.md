# รูลเซ็ตเสริม (Custom rulesets)

นอกจาก osu!, osu!taiko, osu!catch และ osu!mania คุณยังเล่น**รูลเซ็ตเสริม**บน somtum.fun ได้ ซึ่งเป็นโหมดเกมที่ชุมชนทำสำหรับ osu!lazer จาก [rulesets.info](https://rulesets.info/) แต่ละตัวมีลีดเดอร์บอร์ด อันดับ และแท็บในโปรไฟล์ของตัวเองที่นี่ จัดอันดับ**ตามคะแนน**

## รูลเซ็ตที่รองรับ {id=supported}

นี่คือรูลเซ็ตที่ somtum.fun จัดอันดับอยู่ตอนนี้ ทีมงานจะเพิ่มเรื่อย ๆ รายการใน TumThai (ดู[ด้านล่าง](#install)) เป็นรายการล่าสุดเสมอ

| รูลเซ็ต | คืออะไร | ผู้สร้าง |
| :-- | :-- | :-- |
| [sentakki](https://github.com/LumpBloom7/sentakki) | แตะ กดค้าง และสไลด์ตามจังหวะ ได้แรงบันดาลใจจาก maimai | LumpBloom7 |
| [Tau](https://github.com/taulazer/tau) | กวาดโน้ตด้วยแป้นรอบวงกลม | taulazer |
| [Rush!](https://github.com/Beamographic/rush) | อิงจาก Muse Dash แบบหลวม ๆ | Beamographic |
| [Hishigata](https://github.com/LumpBloom7/hishigata) | บล็อกลูกศรที่พุ่งเข้ามา | LumpBloom7 |
| [soyokaze](https://github.com/goodtrailer/soyokaze) | คล้ายมินิเกม Ballads of Breeze ใน Genshin Impact | goodtrailer |
| [osu!fps](https://github.com/wuaht/osu-fps) | osu! มุมมองบุคคลที่หนึ่ง อิงจาก FPoSu ของ McOsu | wuaht |
| [FPSosu!](https://github.com/theokrueger/FPSosu) | ฝึกเล็งมุมมองบุคคลที่หนึ่ง | theokrueger |
| [Swing](https://github.com/EVAST9919/lazer-swing) | โหมดจังหวะแบบเฉพาะตัว | EVAST9919 |
| [Sandbox](https://github.com/EVAST9919/lazer-sandbox) | ของสนุก ๆ ที่ทำด้วย osu!framework | EVAST9919 |
| [bosu](https://github.com/EVAST9919/bosu) | อิงจาก "I wanna be the Boshy" | EVAST9919 |
| [touhosu](https://github.com/EVAST9919/touhosu) | อิงจาก Touhou | EVAST9919 |

แต่ละรูลเซ็ตเป็นของผู้พัฒนา บั๊กในตัวเกมเพลย์ให้รายงานที่หน้าของรูลเซ็ตนั้น ส่วนปัญหาเรื่องคะแนนหรือลีดเดอร์บอร์ดให้รายงานกับเรา

## ติดตั้งรูลเซ็ต {id=install}

รูลเซ็ตเสริมใช้ได้ใน **TumThai** (ไคลเอนต์ osu!lazer ของเรา) บน Windows, Linux และ macOS และใน **TumThai!Next** บน Android ด้วย (เลือก TumThai!Next ใน[หน้าดาวน์โหลด](/home/download?stream=next)) ใช้ไม่ได้ใน osu!(stable) ไคลเอนต์รุ่นเก่า หรือแอป Android ของ TumThai

1. ล็อกอิน TumThai
2. เปิด **Settings → General → Custom rulesets** แล้วกด **Install custom rulesets…**
3. กด **Install** ข้างรูลเซ็ต มันจะขึ้นในแถบรูลเซ็ตด้านบนของจอทันที

หน้าต่างเดียวกันจะแสดงเมื่อรูลเซ็ตมี**อัปเดต**: กด **Update** แล้วรีสตาร์ต TumThai การลบรูลเซ็ตก็มีผลเมื่อรีสตาร์ต TumThai เช่นกัน

ส่งคะแนนได้เฉพาะเวอร์ชันที่ somtum.fun จัดอันดับ ดังนั้นให้ติดตั้งและอัปเดตรูลเซ็ตจากหน้าต่างนี้ ไฟล์รูลเซ็ตที่คุณวางในโฟลเดอร์ `rulesets` ของ TumThai เองยังเล่นได้ แต่จะส่งคะแนนได้ก็ต่อเมื่อเป็นไฟล์เดียวกัน ถ้ารูลเซ็ตขึ้นว่า *Doesn't work with this TumThai version* แปลว่าต้องรอผู้พัฒนาอัปเดต ระหว่างนั้นจะเล่นไม่ได้

### บนมือถือและแท็บเล็ต {id=touch}

รูลเซ็ตเสริมถูกทำมาสำหรับ PC ก่อน และ**ส่วนใหญ่ไม่ได้ออกแบบมาสำหรับจอสัมผัส** บนมือถือหรือแท็บเล็ต บางตัวเล่นด้วยการสัมผัสได้ไม่ดี บางปุ่มอาจหายไปหรือใช้ยาก และบางตัวอาจใช้ไม่ได้เลย ปัญหานี้มาจากวิธีที่แต่ละรูลเซ็ตถูกสร้าง เราจึงแก้จากฝั่งเราไม่ได้ มีแค่ผู้พัฒนารูลเซ็ตที่เพิ่มการรองรับจอสัมผัสได้

- **sentakki** ทำมาสำหรับจอสัมผัส และเหมาะที่สุดสำหรับเริ่มต้น
- **osu!fps, FPSosu!, Tau, bosu และ touhosu** ต้องใช้เมาส์และคีย์บอร์ด อาจเปิดบนมือถือได้ แต่จะเล่นยากมากหรือเล่นไม่ได้
- การต่อเมาส์หรือคีย์บอร์ดเข้ากับมือถือช่วยได้กับบางตัว

ถ้ารูลเซ็ตแครชหรือโหลดไม่ขึ้นบนมือถือ ให้เล่นบน PC แทน หรือแจ้งผู้พัฒนาที่หน้าของรูลเซ็ตนั้น (ลิงก์อยู่ในตารางด้านบน)

## คะแนนและอันดับ {id=scores}

- **จัดอันดับตามคะแนน** รูลเซ็ตเสริมไม่ให้ performance points (pp) จึงไม่มีอันดับ pp
- **การเล่นที่นับ:** การผ่านบนแมพ osu! ที่มีลีดเดอร์บอร์ด (ranked, approved, qualified หรือ loved) การเล่นด้วย Autoplay หรือ Cinema หรือม็อดเล่นอัตโนมัติของรูลเซ็ตเองไม่นับ
- **ลีดเดอร์บอร์ด:** แต่ละแมพมีลีดเดอร์บอร์ดแยกตามรูลเซ็ต พร้อมคะแนนที่ดีที่สุดของคุณ การเล่น Relax และ Autopilot มีบอร์ดแยกเหมือนใน osu!
- **อันดับ:** [อันดับรูลเซ็ตเสริม](/rankings/rulesets) รวมคะแนนที่ดีที่สุดของทุกคนในแต่ละแมพ ranked (ranked score)
- **โปรไฟล์ของคุณ**มีแท็บสำหรับทุกรูลเซ็ตที่เคยเล่น พร้อมอันดับ คะแนน และประวัติอันดับ
- **ระดับดาว**แสดงสำหรับรูลเซ็ตที่คำนวณได้ (เช่น Tau และ soyokaze)

คะแนนใหม่ของคุณจะขึ้นบนเว็บไซต์และในบอต Discord ทันทีที่ส่ง TumThai 2026.1026.1 ขึ้นไปยังแสดงอันดับใหม่ในหน้าผลลัพธ์ด้วย

## สิ่งที่ยังไม่รองรับ {id=not-supported}

- **Performance points**: อันดับตามคะแนนเท่านั้น
- **มัลติเพลเยอร์และการดูคนอื่นเล่น**
- **การเรนเดอร์รีเพลย์**: หน้าคะแนนและบอต Discord จะบอกว่าเรนเดอร์ไม่ได้สำหรับรูลเซ็ตเสริม
- **เหรียญ**
- **osu!(stable) ไคลเอนต์รุ่นเก่า และแอป Android ของ TumThai** (TumThai!Next บน Android ใช้ได้)

## ดูเพิ่มเติม {id=see-also}

- [FAQ](/wiki/FAQ)
- [Performance points](/wiki/Performance_points)
- [rulesets.info](https://rulesets.info/) แหล่งที่มาของรูลเซ็ตเหล่านี้
