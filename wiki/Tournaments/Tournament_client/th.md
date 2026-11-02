# Tournament client

tournament client แสดงผู้เล่นทุกคนในแมตช์มัลติเพลเยอร์เคียงกันสำหรับสตรีม มีสองแบบ: ของ TumThai และของ osu!(stable) ทั้งสองใช้บัญชี somtum.fun ของคุณ

## TumThai {id=tumthai}

tournament client ของ TumThai ใช้บน somtum.fun ได้เลย เปิด TumThai ด้วย `--tournament`:

```
tumthai.exe --tournament
```

บน Windows สร้าง shortcut ไปที่ `tumthai.exe` แล้วเติม ` --tournament` ท้าย target ได้ มันใช้เซิร์ฟเวอร์เดียวกับเกม จึงไม่ต้องตั้งค่าอะไรเพิ่ม วิธีใช้อยู่ใน [wiki ของ osu!](https://osu.ppy.sh/wiki/osu!_tournament_client)

## osu!(stable) {id=osu-stable}

tournament client ของ osu!(stable) เปิดหน้าต่างเกมหนึ่งหน้าต่างต่อผู้เล่นหนึ่งคน มันเปิดหน้าต่างเหล่านั้นเอง โดยไม่มี `-devserver somtum.fun` ที่ปกติใช้เปิด osu! หน้าต่างเหล่านั้นจึงจะเชื่อมต่อ osu! แทนที่จะเป็นเรา จนกว่า patcher ของเราจะทำให้ได้ ให้ส่งมันมาที่ somtum.fun ด้วย [Fiddler Classic](https://www.telerik.com/fiddler/fiddler-classic) เครื่องมือฟรีบน Windows ที่เปลี่ยนปลายทางของคำขอเว็บในคอมของคุณได้

::: alert-warning
ระหว่างที่ Fiddler ทำงานด้วยกฎนี้ **ทุกอย่างในคอมที่ไปที่ ppy.sh จะไปที่ somtum.fun แทน** รวมถึงเว็บไซต์ osu! ในเบราว์เซอร์ เปิดเฉพาะตอนใช้ tournament client และปิดเมื่อเลิกใช้
:::

::: alert-warning
**Discord:** ระหว่างที่ Fiddler เปิดอยู่ อย่าเข้าเซิร์ฟเวอร์ใหม่หรือทำอะไรสำคัญบน Discord (เช่น เปลี่ยนการตั้งค่าบัญชี อีเมล หรือรหัสผ่าน หรือซื้ออะไร) Fiddler ส่งข้อมูลทั้งหมดของ Discord ผ่านตัวมันเอง และ Discord อาจมองว่าเป็นบัญชีที่ถูกแฮกแล้ว**แบนบัญชี** แชทเสียงและข้อความปกติใช้ได้ ปิด Fiddler ก่อนถ้าต้องทำอย่างอื่นบน Discord
:::

### 1. ตั้งค่า Fiddler {id=set-up-fiddler}

1. ดาวน์โหลดและติดตั้ง [Fiddler Classic](https://www.telerik.com/fiddler/fiddler-classic)
2. เปิดโปรแกรม แล้วไปที่ **Tools → Options → HTTPS**
3. ติ๊ก **Capture HTTPS CONNECTs** และ **Decrypt HTTPS traffic** กด **Yes** เมื่อ Windows ถามว่าจะเชื่อถือใบรับรองของ Fiddler หรือไม่

ใบรับรองนี้ทำให้ Fiddler อ่านและเปลี่ยนคำขอ HTTPS ในคอมของคุณได้ ซึ่งจำเป็นต่อการส่งคำขอของ osu! มาที่เรา ทำแบบนี้บนคอมของคุณเองเท่านั้น

### 2. เพิ่มกฎ {id=add-the-rule}

1. ไปที่ **Rules → Customize Rules...** (หรือแท็บ **FiddlerScript**)
2. หา `static function OnBeforeRequest(oSession: Session) {` แล้ววางโค้ดนี้ต่อจากบรรทัดนั้น:

```js
        if (oSession.RequestMethod != "CONNECT") {
            var h = oSession.hostname.ToLower();
            if (h == "ppy.sh" || h.EndsWith(".ppy.sh")) {
                var newHost = h.Substring(0, h.Length - 6) + "somtum.fun";
                oSession.utilCreateResponseAndBypassServer();
                oSession.oResponse.headers.HTTPResponseCode = 307;
                oSession.oResponse.headers.HTTPResponseStatus = "307 Temporary Redirect";
                oSession.oResponse["Location"] = "https://" + newHost + oSession.PathAndQuery;
                oSession.oResponse["Cache-Control"] = "no-cache";
            }
        }
```

3. บันทึก (**Ctrl+S**) Fiddler จะตรวจสคริปต์ตอนบันทึก

### 3. เปิด tournament client {id=start}

1. ตรวจว่า Fiddler เปิดอยู่และกำลังดักข้อมูล (**File → Capture Traffic** หรือ **F12**)
2. ตั้งค่า `tournament.cfg` ในโฟลเดอร์ osu! ตามปกติ (ดู [wiki ของ osu!](https://osu.ppy.sh/wiki/osu!_tournament_client))
3. เปิด `osu!.exe` **โดยไม่ใส่** `-devserver` เมื่อ Fiddler ทำงานอยู่ osu! และทุกหน้าต่างที่มันเปิดจะเชื่อมต่อ somtum.fun
4. ล็อกอินด้วยชื่อผู้ใช้และรหัสผ่าน somtum.fun

### เมื่อใช้เสร็จ {id=when-done}

1. ปิด tournament client แล้วปิด Fiddler การปิด Fiddler จะทำให้การเชื่อมต่อของคอมกลับเป็นปกติ
2. ถ้าจะไม่ใช้อีก ให้ลบใบรับรองของ Fiddler: **Tools → Options → HTTPS → Actions → Reset All Certificates**

## ปัญหา {id=problems}

- **หน้าต่างขึ้นว่าเชื่อมต่อไม่ได้ หรือไปล็อกอิน osu! แทน** ตรวจว่า Fiddler เปิดอยู่และกำลังดักข้อมูล และเปิดการถอดรหัส HTTPS แล้ว
- **เว็บไซต์ osu! หรือเกมอื่นใช้ไม่ได้ระหว่างเปิด Fiddler** นั่นคือผลของกฎ ปิด Fiddler เมื่อไม่ได้ใช้ tournament client

ยังติดอยู่? ถามใน [Discord](https://discord.gg/U6Ztb3mRyz) ของเรา
