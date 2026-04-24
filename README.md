# 📱 คู่มือสร้าง APK ด้วย PWABuilder (ไม่ต้องติดตั้งโปรแกรม!)

วิธีนี้ใช้เว็บฟรีในการสร้าง APK ไม่ต้องลง Android Studio ไม่ต้องพิมพ์คำสั่ง

**ใช้เวลารวม:** ประมาณ 20-30 นาที

---

## 🎯 ภาพรวมขั้นตอน

1. สมัคร GitHub (ฟรี)
2. อัพไฟล์ขึ้น GitHub
3. เปิด GitHub Pages
4. ใช้ PWABuilder สร้าง APK
5. ติดตั้งในมือถือ

---

## ✅ STEP 1: สมัคร GitHub

1. ไปที่ **https://github.com/signup**
2. ใส่อีเมล → สร้างรหัสผ่าน → ตั้ง username
3. ยืนยันอีเมล
4. เสร็จ! ฟรี 100%

---

## ✅ STEP 2: สร้าง Repository ใหม่

1. หลัง login กดปุ่มเขียว **New** (มุมซ้ายบน) หรือไปที่ **https://github.com/new**
2. ตั้งชื่อ repo เช่น `meditation-app`
3. เลือก **Public** (สำคัญ! ต้อง Public เท่านั้น)
4. กด **Create repository**

---

## ✅ STEP 3: อัพไฟล์ขึ้น GitHub

1. ในหน้า repo ที่เพิ่งสร้าง กดลิงก์ **"uploading an existing file"**  
   (หรือกดปุ่ม **Add file → Upload files**)

2. **ลากไฟล์ทั้ง 5 ไฟล์นี้** ไปวาง:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`

3. เลื่อนลงล่างสุด กด **Commit changes**

---

## ✅ STEP 4: เปิด GitHub Pages

1. ในหน้า repo กด tab **Settings** (มุมขวาบน)
2. เมนูซ้าย กด **Pages**
3. ที่หัวข้อ **Source** เลือก:
   - Branch: **main**
   - Folder: **/ (root)**
4. กด **Save**
5. **รอ 1-2 นาที** แล้ว refresh หน้า จะเห็นข้อความ:
   > Your site is live at **https://USERNAME.github.io/meditation-app/**

6. **Copy URL นี้ไว้** จะใช้ในขั้นต่อไป

**ทดสอบก่อน:** เปิด URL นี้ในเบราว์เซอร์ → ควรเห็นแอปสมาธิทำงาน ถ้าเห็น = พร้อมต่อได้

---

## ✅ STEP 5: สร้าง APK ด้วย PWABuilder

1. เปิด **https://www.pwabuilder.com**
2. ในช่อง **"Enter URL to get started"** วาง URL ของคุณ เช่น:
   ```
   https://yourname.github.io/meditation-app/
   ```
3. กดปุ่ม **Start**
4. รอให้สแกน PWA (30 วินาที)
5. จะเห็นหน้ารายงานคะแนน → กด **Package for Stores** (มุมขวาบน)
6. เลือก **Android** → กด **Generate Package**

**ตั้งค่าก่อน generate (ใช้ default ได้):**
- Package ID: `com.meditation.game` (หรือเปลี่ยนได้)
- App name: `สมาธิเกม`
- Host: URL ของคุณ
- เลื่อนลงไปกด **Download**

7. จะได้ไฟล์ **zip** กลับมา → แตกไฟล์ → ข้างในมี:
   - `app-release-signed.apk` ← **ตัวนี้แหละ!**
   - `signing-key-info.txt` (เก็บไว้ด้วย เผื่อ update)

---

## ✅ STEP 6: ติดตั้งลงมือถือ

1. **ส่งไฟล์ APK ไปมือถือ** (เลือกวิธีใดก็ได้):
   - Upload Google Drive แล้วดาวน์โหลดในมือถือ
   - ส่งทาง Line ให้ตัวเอง (Keep)
   - ต่อสาย USB แล้ว copy

2. **ในมือถือ** กดเปิดไฟล์ APK

3. ถ้าขึ้นเตือน **"ไม่อนุญาตให้ติดตั้งจากแหล่งนี้"**:
   - กดปุ่ม **ตั้งค่า** → เปิด **อนุญาตจากแหล่งนี้**
   - กลับมากดติดตั้ง

4. กด **ติดตั้ง** → รอเสร็จ → **เปิด** 🎉

---

## 🔄 อยากแก้ไขแอป?

1. แก้ไฟล์ในคอม
2. ไปหน้า GitHub repo → คลิกไฟล์ที่แก้ → กดไอคอนดินสอ → copy โค้ดใหม่ทับ → Commit
3. **หรือ** ลบไฟล์เก่า → Upload ไฟล์ใหม่ทับ
4. รอ 1 นาที → เข้า URL PWA → ดูว่าเปลี่ยนแล้วหรือยัง
5. กลับไป PWABuilder → ใส่ URL เดิม → Generate ใหม่ → ได้ APK เวอร์ชันใหม่

---

## 💡 ข้อดีของวิธีนี้

- ✅ ไม่ต้องลงโปรแกรมใดๆ ในคอม
- ✅ ฟรี 100%
- ✅ APK ที่ได้ติดตั้งได้ทันที แจกเพื่อนได้
- ✅ ใช้งานออฟไลน์ได้ (มี service worker)
- ✅ เปิดแอปแล้วเหมือนแอปจริง (ไม่มี address bar)
- ✅ อัพขึ้น Google Play Store ได้เลย (ใช้ไฟล์ .aab ที่ได้จาก PWABuilder)

---

## 🆘 ปัญหาที่อาจเจอ

### GitHub Pages ไม่ขึ้น
- รอ 2-5 นาทีหลัง enable แล้ว refresh
- ตรวจว่า repo เป็น **Public**
- ตรวจว่าเลือก branch **main**

### PWABuilder บอก "PWA not detected"
- เปิด URL ในเบราว์เซอร์ก่อน → ดูว่าแอปรันได้ไหม
- ตรวจว่ามีไฟล์ `manifest.json` และ `sw.js` ในโฟลเดอร์เดียวกับ `index.html`

### ติดตั้ง APK ในมือถือไม่ได้
- ไปที่ **การตั้งค่า → ความปลอดภัย → ติดตั้งแอปที่ไม่รู้จัก**
- เลือกเบราว์เซอร์/แอปจัดการไฟล์ที่ใช้เปิด APK → เปิด **อนุญาต**

### APK ติดตั้งแล้วเปิดไม่ได้ / ค้าง
- ต่อเน็ตเปิดครั้งแรก (เพื่อโหลด library)
- ครั้งต่อไปใช้ offline ได้

---

## 📝 สรุปไฟล์ที่ต้องอัพขึ้น GitHub

```
meditation-app/
├── index.html       ← ตัวแอปหลัก
├── manifest.json    ← ข้อมูลแอป (ชื่อ, ไอคอน)
├── sw.js            ← Service Worker (offline)
├── icon-192.png     ← ไอคอน 192x192
└── icon-512.png     ← ไอคอน 512x512
```

มีทุกไฟล์นี้ในโฟลเดอร์ที่ผมส่งให้แล้ว ตรงแตกไฟล์แล้ว**ลากขึ้น GitHub ได้เลย**
