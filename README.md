# WatsaiTantin
# 🌟 WATSAIMART ทันถิ่น | ระบบศูนย์ข้อมูลท้องถิ่นอัจฉริยะ

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Vue.js](https://img.shields.io/badge/Vue.js-3.0-brightgreen.svg)
![Google Apps Script](https://img.shields.io/badge/Google_Apps_Script-Backend-orange.svg)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-Styling-06B6D4.svg)

**WATSAIMART ทันถิ่น** (Smart Local Governance System) คือเว็บแอปพลิเคชันที่พัฒนาขึ้นเพื่อยกระดับการบริหารจัดการข้อมูลของ องค์กรปกครองส่วนท้องถิ่น (อปท.) ให้ก้าวสู่การเป็นรัฐบาลดิจิทัล (Digital Government) โดยเน้นความโปร่งใส เข้าถึงง่าย และประมวลผลแบบเรียลไทม์ ภายใต้แนวคิด **S.M.A.R.T** (Seamless, Measurable, AI-driven, Real-time, Transparent)

---

## ✨ ฟีเจอร์เด่น (Key Features)

📊 **1. Executive Dashboard (กระดานข้อมูลผู้บริหาร)**
- สรุปภาพรวมงบประมาณรายจ่าย สัดส่วนการเบิกจ่าย และจำนวนโครงการแบบ Real-time
- กราฟวิเคราะห์ข้อมูล (Data Analytics) แยกตามกอง/แผนงาน/หมวดรายจ่าย

🗺️ **2. GIS & Mapping (ระบบแผนที่พิกัดโครงการ)**
- แสดงจุดดำเนินการโครงการบนแผนที่ (Google/Leaflet) พร้อมสัญลักษณ์แยกประเภทงาน
- ดึงพิกัดพิกัด GPS อัตโนมัติจากมือถือของเจ้าหน้าที่ขณะลงพื้นที่

🤖 **3. AI Assistant (ผู้ช่วยอัจฉริยะบริการประชาชน)**
- ผสานการทำงานกับ **Gemini AI** เพื่อตอบคำถามประชาชนเกี่ยวกับโครงการและงบประมาณอัตโนมัติตลอด 24 ชม.

📱 **4. QR Code & Public Engagement (การมีส่วนร่วมของประชาชน)**
- สร้างป้าย QR Code อัตโนมัติสำหรับพิมพ์ติดหน้างาน เพื่อให้ประชาชนสแกนดูรายละเอียดได้ทันที
- ระบบรับเรื่องร้องเรียน/เสนอแนะ ลิงก์ตรงเข้าสู่ระบบจัดการของเจ้าหน้าที่

📑 **5. Procurement & Reporting (ระบบจัดซื้อจัดจ้าง)**
- ติดตามสถานะสัญญา วันเริ่มต้น/สิ้นสุด และระบบแจ้งเตือนสีแดงเมื่อสัญญา "ล่าช้า"
- สร้างและส่งออก **รายงาน สขร.1** อัตโนมัติสำหรับการตรวจประเมิน ITA

📁 **6. File & Media Management (ระบบจัดการเอกสาร)**
- อัปโหลดภาพถ่ายความคืบหน้า (ก่อน-ระหว่าง-หลังดำเนินการ) พร้อมระบบบีบอัดภาพอัตโนมัติ (Image Compression)
- แนบไฟล์เอกสารสำคัญ (PDF, สัญญา, TOR) เก็บลง Google Drive อัตโนมัติ

---

## 🛠️ เทคโนโลยีที่ใช้ (Tech Stack)

**Frontend:**
- [Vue.js 3](https://vuejs.org/) (Composition API) - จัดการ State และหน้าต่าง UI (Pagination, Virtual DOM)
- [Tailwind CSS](https://tailwindcss.com/) - จัดการสไตล์และ Responsive Design
- [Chart.js](https://www.chartjs.org/) - สร้างกราฟสถิติ
- [Leaflet.js](https://leafletjs.com/) - ระบบแผนที่

**Backend & Database:**
- [Google Apps Script (GAS)](https://developers.google.com/apps-script) - ควบคุมเซิร์ฟเวอร์
- [Google Sheets](https://www.google.com/sheets/about/) - ทำหน้าที่เป็นฐานข้อมูล (Database)
- [Google Drive](https://www.google.com/drive/) - เก็บรูปภาพและไฟล์เอกสารแนบ

**API:**
- [Google Gemini API](https://aistudio.google.com/) - ระบบ AI Chatbot

---

## 📂 โครงสร้างไฟล์ (File Structure)

ระบบทำงานบน Google Apps Script โดยประกอบด้วย 4 ไฟล์หลัก:
1. `Code.gs` - ฝั่ง Backend (จัดการฐานข้อมูล Sheets, บันทึกไฟล์ลง Drive, เชื่อมต่อ AI)
2. `Index.html` - ฝั่ง Frontend UI (HTML + Tailwind Classes + องค์ประกอบ Vue)
3. `JS.html` - โลจิกฝั่ง Client (Vue Setup, ฟังก์ชันการคำนวณ, ระบบ Pagination)
4. `CSS.html` - สไตล์เพิ่มเติมและการจัดหน้าสำหรับการสั่งพิมพ์ (Print Media Query)

---

## 🚀 การติดตั้งและตั้งค่า (Installation & Setup)

1. **สร้างฐานข้อมูล:** เปิด Google Sheets สร้างไฟล์ใหม่ และไปที่เมนู `ส่วนขยาย` (Extensions) > `Apps Script`
2. **คัดลอกโค้ด:** สร้างไฟล์ตามโครงสร้างด้านบน และนำโค้ดไปวางให้ครบทั้ง 4 ไฟล์
3. **กำหนดค่าเริ่มต้น:** - ในหน้า `Code.gs` ให้เลือกฟังก์ชัน `setupDatabase` แล้วกดปุ่ม "เรียกใช้" (Run) เพื่อสร้างหัวตารางและโฟลเดอร์อัตโนมัติ
4. **Deploy ระบบ:** - กด `การทำให้ใช้งานได้` (Deploy) > `การทำให้ใช้งานได้รายการใหม่` (New Deployment)
   - เลือกประเภท `เว็บแอป` (Web App)
   - สิทธิ์การเข้าถึง: เลือก `ทุกคน` (Anyone)
5. **ตั้งค่า AI:** นำ Web App URL ไปเปิดใช้งาน กรอกรหัส PIN (ค่าเริ่มต้น `1234`) เพื่อเข้าสู่เมนูตั้งค่า และนำ **Gemini API Key** มาใส่

---

## 🔒 ระบบรักษาความปลอดภัย (Security)
- ระบบล็อกอินด้วย PIN Code
- แบ่งสิทธิ์การเข้าถึง (Role-Based Access): 
  - **Master Admin:** จัดการได้ทุกกองและเข้าถึงเมนูตั้งค่า
  - **Department Admin:** แก้ไขข้อมูลได้เฉพาะของกอง/หน่วยงานตัวเอง

---

*พัฒนาเพื่อความโปร่งใสและประโยชน์สูงสุดของพี่น้องประชาชน* 🇹🇭
