# FloodWatch Thailand

ตั้งค่า secret GOOGLE_FLOOD_API_KEY บน Sites ด้วยคีย์ที่มีสิทธิ์ใช้ Google Flood Forecasting API สำหรับ local คัดลอก .dev.vars.example เป็น .dev.vars แล้วใส่คีย์ ห้าม commit คีย์ เริ่มเว็บด้วย npm install และ npm run dev

ขอสิทธิ์: https://support.google.com/flood-hub/answer/16364306

API เรียกฝั่งเซิร์ฟเวอร์ด้วย regionCode TH พร้อม pagination และ cache 5 นาที เว็บรีเฟรชทุก 5 นาทีขณะเปิด การแจ้งเตือนใช้ Notification API เฉพาะสถานีที่ติดตามและมีสถานะ SEVERE/EXTREME ขณะหน้าเว็บทำงาน ไม่แจ้งเมื่อปิดเว็บ ข้อมูลสมมติเปิดเองและไม่ใช้แจ้งเตือนจริง พื้นที่ที่ไม่มีสถานีไม่หมายความว่าปลอดภัย ข้อมูลเก่ากว่า 48 ชั่วโมงแสดง UNKNOWN (เกณฑ์ของแอป) ไม่มีการเปลี่ยนเป็น demo อัตโนมัติเมื่อ API ผิดพลาด

แผนที่ใช้ Leaflet 1.9.4 และ OpenStreetMap tiles ผ่าน CDN ต้องมีอินเทอร์เน็ต

