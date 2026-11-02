# ฟิลเตอร์แท็บเล็ต

เล่นด้วยแท็บเล็ต? หน้านี้บอกว่าฟิลเตอร์และปลั๊กอินของ **OpenTabletDriver** (OTD) ตัวไหนใช้ได้บน somtum.fun

สรุปสั้น ๆ: ฟิลเตอร์ smoothing และ chatter ใช้ได้ ตราบใดที่ไม่ได้เล็งแทนคุณ ฟิลเตอร์ที่สร้างการเคลื่อนที่ของเคอร์เซอร์ หรือทำนายว่าปากกาจะไปทางไหน ไม่อนุญาต

การใช้ฟิลเตอร์ต้องห้าม หรือใช้ฟิลเตอร์ที่อนุญาตเกินขีดจำกัด ถือว่าผิดกฎเรื่อง[การโกง](/legal/th/Rules) และบัญชีของคุณอาจถูก[จำกัด](/legal/th/Restrictions)

## ไดรเวอร์แท็บเล็ตอื่น ๆ {id=other-drivers}

กฎในหน้านี้ใช้กับปลั๊กอินของ OpenTabletDriver **ไดรเวอร์ของผู้ผลิตเอง เช่น Wacom, Huion, XP-Pen และอื่น ๆ ใช้ได้**

output mode ที่มากับ OTD (Absolute, Relative และ Artist) ก็ใช้ได้ รวมถึงการแตะด้วยปลายปากกา

## อนุญาต {id=allowed}

ใช้ได้ตามต้องการ:

- AbstractQbit's Radial Follow Smoothing (ชุด)
- Additional Keys
- BetterCalibrator
- Kuuube's CHATTER EXTERMINATOR (ชุด)
- Circular Area (ชุด)
- Cycle Keybind
- Devocub Smoothing
- DragThreshold
- DualActionBinds
- Enhanced Output Modes
- Erase Button
- Flip Axes (ชุด)
- HawkuFilters (ชุด), รวมถึง Hawku Smoothing และ Hawku Noise Reduction
- Hover Distance Limiter
- LED Sandbox
- MabletMapping
- Monitor Toggle
- nzbasic's Hand Speed Viewer
- OpenKneeboard OTD-IPC
- Precision Control
- PSSA
- Relative Mode Area
- Scroll Bindings
- SlimyScylla
- Tablet Area Randomizer
- Tablet Calibration (ชุด)
- Tablet Debounce
- Tilt Calibration
- TouchEmu
- Touch Gestures Installer
- Ux Remote
- VMultiMode
- Wireless Kit Addon

## อนุญาตภายในขีดจำกัด {id=limits}

ใช้ได้ตราบใดที่การตั้งค่าอยู่ในขีดจำกัดเหล่านี้:

| ฟิลเตอร์ | ขีดจำกัด |
| :-- | :-- |
| Temporal Resampler | Prediction Ratio ต้องเป็น 0, Frame Time Shift ต้องเป็น 0 และ Reverse EMA ต้องเป็น 0.6 ขึ้นไป |
| Reconstructor | EMA Weight ต้องเป็น 0.6 ขึ้นไป |
| ScuffedInterpolator และ ScuffedExtrapolator ของ jaaakb | Interpolation ต้องเป็น 1 ขึ้นไป |
| Devocub Antichatter | ต้องปิด Prediction |
| Saturn (เฉพาะฟิลเตอร์ที่ไม่ใช่ interpolation) | Reverse EMA ต้องเป็น 0.6 ขึ้นไป และ stock EMA weight ต้องเป็น 1 ขึ้นไป |

อีกสองเรื่องที่ต้องระวัง:

- **ใช้ EMA ได้แค่ฟิลเตอร์เดียว** ถ้าเปิดฟิลเตอร์ที่มีการตั้งค่า EMA มากกว่าหนึ่งตัว ถือว่าเกินขีดจำกัด แม้แต่ละตัวจะอยู่ในขีดจำกัดของตัวเองก็ตาม
- **พิมพ์ค่าเอง** ถ้าการตั้งค่าในรายการนี้ถูกปล่อยว่าง OTD จะใช้ค่าเริ่มต้นของปลั๊กอิน ซึ่งเราไม่รู้ว่าเป็นเท่าไร ทีมงานต้องตรวจด้วยมือ จึงควรตั้งค่าเอง

## ใช้โดยยอมรับความเสี่ยงเอง {id=own-risk}

**MouseUtils** และ **ScriptRunner** ไม่ได้ถูกห้าม แต่ยังต้องทดสอบเพิ่ม สิ่งที่มันทำขึ้นอยู่กับการตั้งค่าของคุณ ถ้าตัวใดตัวหนึ่งทำให้คุณได้เปรียบอย่างไม่เป็นธรรม คุณต้องรับผิดชอบเอง

## ห้ามใช้ {id=banned}

ห้ามใช้เลย ไม่ว่าจะตั้งค่าอย่างไร:

- BezierInterpolator
- Chatter Generator
- MeL (ทั้งชุด)
- Position Interpolation และ Velocity Interpolation ของ Saturn
- sin(cursor)
- SpringInterpolator
- Stroke Snapping
- ปลั๊กอิน Windows Ink สำหรับ OTD เช่น output mode แบบ Windows Ink ของ VoiDPlugins

## ไม่อยู่ในหน้านี้? {id=not-listed}

ถามใน [Discord](https://discord.gg/U6Ztb3mRyz) ของเราก่อนใช้ ฟิลเตอร์ไม่ได้ถูกห้ามเพียงเพราะไม่อยู่ในหน้านี้ แต่ fork และสำเนาที่เปลี่ยนชื่อต้องทำตามกฎของฟิลเตอร์ต้นฉบับ รายการอาจเปลี่ยนได้ จึงควรกลับมาดูเมื่อเพิ่มอะไรใหม่

## สิ่งที่เราเห็น {id=what-we-see}

ระหว่างที่คุณเล่น osu!(stable) หรือไคลเอนต์รุ่นเก่าของเราโดยเปิด OpenTabletDriver อยู่ ระบบกันโกงจะอ่านการตั้งค่าของ OTD: ชื่อแท็บเล็ต output mode ฟิลเตอร์และเครื่องมือพร้อมค่าที่ตั้ง และชื่อปลั๊กอินที่ติดตั้ง ทีมงานใช้ข้อมูลนี้ร่วมกับรีเพลย์ของคุณ ถ้าไม่ได้เปิด OTD จะไม่มีการอ่านอะไรเลย

ฟิลเตอร์ที่ปิดอยู่ไม่นับเป็นความผิด แต่ควรลบตัวที่ถูกห้ามซึ่งไม่ได้ใช้ออก

ถ้าคิดว่าเราเข้าใจการตั้งค่าของคุณผิด อีเมลมาที่ [support@somtum.fun](mailto:support@somtum.fun) จากอีเมลของบัญชี ถ้าบัญชีถูกจำกัด ดู[การลงโทษและการอุทธรณ์](/legal/th/Restrictions)
