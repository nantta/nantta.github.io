#13.1.1 Generic Web Service Security
-  Verify that all application components use the same encodings and parsers
  to avoid parsing attacks that exploit different URI or file parsing behavior
  that could be used in SSRF and RFI attacks

#ChatGPT
- การตรวจสอบให้ทุกส่วนของแอปพลิเคชันใช้ การเข้ารหัส (encoding) และตัวแปลง (parser) เดียวกันช่วยป้องกัน SSRF และ RFI ซึ่งอาจเกิดจากความแตกต่างในการประมวลผล URL หรือไฟล์ ทำให้แฮ็กเกอร์ใช้ช่องโหว่เพื่อเข้าถึงทรัพยากรที่ไม่ควรเข้าถึงได้

#Gemini
- การพัฒนาเว็บแอปพลิเคชัน มันเกี่ยวข้องกับการป้องกันช่องโหว่ที่อาจนำไปสู่การโจมตีแบบ Server-Side Request Forgery (SSRF) และ Remote File Inclusion (RFI)

#Myself
- แนวคิดนี้เกี่ยวกับการรักษาความปลอดภัยของแอปพลิเคชัน โดยเฉพาะการป้องกันการโจมตีประเภท SSRF (Server-Side Request Forgery) และ RFI (Remote File Inclusion) ซึ่งอาจเกิดจาก ความไม่สอดคล้องกันในการเข้ารหัส (encoding) และการแปลงข้อมูล (parsing) ของ URI หรือไฟล์ ในแต่ละองค์ประกอบของระบบ
- สรุป: ถ้าระบบของคุณมีหลายองค์ประกอบที่ประมวลผล URL หรือไฟล์ ให้แน่ใจว่าทุกส่วน ใช้มาตรฐานเดียวกัน ในการเข้ารหัสและแปลงข้อมูล มิฉะนั้นอาจเกิดช่องโหว่ที่แฮ็กเกอร์ใช้โจมตีแอปพลิเคชัน แบบโดนนน เลยยยย

#ตัวอย่าง(เผื่อจารย์เอาครับเพิ่มให้ๆ)
- บริการย่อลิงก์ (URL Shortener) ถูกใช้ในการโจมตี SSRF
- ระบบอัปโหลดไฟล์ที่ไม่กรอง Path Traversal
- Wi-Fi Phishing ด้วย SSID Encoding
- การโจมตี Open Redirect ผ่าน SMS หรือ Email
