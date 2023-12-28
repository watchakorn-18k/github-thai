
## 🚩 ฟังก์ชั่น

- แถบเมนู GitHub ภาษาไทย ชื่อ ปุ่ม และส่วนประกอบสาธารณะอื่น ๆ
- รักษาและปรับปรุงการทำงานปกติ
## 🌐 เบราว์เซอร์และตัวจัดการสคริปต์

เบราว์เซอร์ | ตัวจัดการสคริปต์
:---------------------------------: | :----------:
Chrome หรือเบราว์เซอร์ที่ใช้ Chromium | [Tampermonkey][Tampermonkey],[Violentmonkey][Violentmonkey]
Safari | [Macaque][Macaque]
เบราว์เซอร์ Firefox | ไม่ได้ทดสอบ

## 💽 งานติดตั้ง
1. กรุณาติดตั้ง User Script Manager ก่อน
1. จากนั้นคลิกลิงก์ใดลิงก์หนึ่งเพื่อติดตั้งสคริปต์
    - [GitHub 中文化插件 - GitHub 托管【开发版】（相对及时更新）][main.user.js]
        > สังเกต: 
        > 1. เมื่อหมายเลขเวอร์ชันไม่ได้รับการอัพเดต แม้ว่าเนื้อหาจะได้รับการอัปเดตแล้ว ตัวจัดการสคริปต์ผู้ใช้จะยังคงเพิกเฉยต่อหมายเลขเวอร์ชันดังกล่าว และคุณจะต้องติดตั้งด้วยตนเองเพื่อรับการอัปเดต
        > 2. ปัจจุบันหมายเลขเวอร์ชันการพัฒนาได้รับการอัปเดตอัตโนมัติทุกเช้าวันจันทร์
    - [GitHub 中文化插件 - GreasyFork 托管【发布版】（仅大版本更新）][main(greasyfork).user.js]
1. รีเฟรชหน้าแล้วคุณจะพบว่าเว็บไซต์ถูกแปลงเป็นภาษาจีน

## วิธีการดีบักท้องถิ่นของ Lexicon
1. คุณต้องติดตั้งตัวจัดการปลั๊กอิน [Tampermonkey][Tampermonkey] อื่นๆ อาจไม่รองรับ
1. ในการจัดการปลั๊กอินของเบราว์เซอร์ ให้เปิดใช้งาน "Allow access to file URLs" ของ [Tampermonkey][Tampermonkey] ดังแสดงในรูป:

    <picture>
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/maboloshi/github-chinese/gh-pages/preview/允许访问文件网址-light.png"/>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/maboloshi/github-chinese/gh-pages/preview/允许访问文件网址-dark.png"/>
      <img src="https://raw.githubusercontent.com/maboloshi/github-chinese/gh-pages/preview/允许访问文件网址-light.png" width="75%" />
    </picture>

1. วางไฟล์ที่แก้ไขแล้วไว้ในตำแหน่งท้องถิ่นที่สามารถเข้าถึงได้ง่าย
1. ติดตั้ง [GitHub Chinese Culture Plug-in - GitHub Hosting [เวอร์ชันการพัฒนา] (อัปเดตค่อนข้างทันเวลา)] [main.user.js] จริง ๆ แล้ว [ปลั๊กอินวัฒนธรรมจีน GitHub - GreasyFork Hosting [เวอร์ชันวางจำหน่าย] (เฉพาะเวอร์ชันหลักเท่านั้น) อัปเดตเวอร์ชัน)] [ main(greasyfork).user.js] ก็มีให้บริการเช่นกัน
1. กลับไปที่ตัวจัดการปลั๊กอินและแก้ไขเส้นทางไฟล์อรรถาภิธานซึ่งคล้ายกับ `// @require https://raw.githubusercontent.com/maboloshi/github-chinese/gh-pages/locals.js?v1 .9.0`
    เปลี่ยน URL ภาษาจีนเป็นรูปแบบพาธในเครื่อง เช่น `file:///D:/APP/github%E9%A1%B9%E7%9B%AE/github-chinese/locals.js`

   > [!เคล็ดลับ]
   > ลากไฟล์ไปยังแถบที่อยู่ของเบราว์เซอร์โดยตรง จากนั้นคัดลอกที่อยู่ในแถบที่อยู่
