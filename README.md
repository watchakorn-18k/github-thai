## Github Thai

![i](https://cdn.discordapp.com/attachments/372372440334073859/1189870689709211698/image.png?ex=659fbc6f&is=658d476f&hm=42347e2ac304f9d8ed708338d4293cbf6e41df1837181ef15702c41ab6591553&)

## 🚩 ฟังก์ชั่น

-   แถบเมนู GitHub ภาษาไทย ชื่อ ปุ่ม และส่วนประกอบสาธารณะอื่น ๆ
-   รักษาและปรับปรุงการทำงานปกติ

## 🌐 เบราว์เซอร์และตัวจัดการสคริปต์

|              เบราว์เซอร์              |                                        ตัวจัดการสคริปต์                                         |
| :-----------------------------------: | :---------------------------------------------------------------------------------------------: |
| Chrome หรือเบราว์เซอร์ที่ใช้ Chromium | [Tampermonkey](https://www.tampermonkey.net/),[Violentmonkey](https://violentmonkey.github.io/) |
|                Safari                 |                                 [Macaque](https://macaque.app/)                                 |
|          เบราว์เซอร์ Firefox          |                                           ไม่ได้ทดสอบ                                           |

## 💽 งานติดตั้ง

1. กรุณาติดตั้ง User Script Manager ก่อน
1. จากนั้นคลิกลิงก์ใดลิงก์หนึ่งเพื่อติดตั้งสคริปต์
    - [github-thai](https://github.com/watchakorn-18k/github-thai/raw/gh-pages/mainTh.user.js)
1. รีเฟรชหน้าแล้วคุณจะพบว่าเว็บไซต์ถูกแปลงเป็นภาษาจีน

## วิธีการดีบักไฟล์ในเครื่อง

1. คุณต้องติดตั้งตัวจัดการปลั๊กอิน Tampermonkeyอื่นๆ อาจไม่รองรับ

1. ในการจัดการปลั๊กอินของเบราว์เซอร์ ให้เปิดใช้งาน "Allow access to file URLs" ของ Tampermonkey ดังแสดงในรูป:

<div align="center">
 <picture>
   <source media="(prefers-color-scheme: light)" srcset="https://cdn.discordapp.com/attachments/372372440334073859/1190330028232278177/image.png"/>
   <source media="(prefers-color-scheme: dark)" srcset="https://cdn.discordapp.com/attachments/372372440334073859/1190330028232278177/image.png"/>
   <img src="https://cdn.discordapp.com/attachments/372372440334073859/1190330028232278177/image.png" width="75%" />
 </picture>
</div>

3. กลับไปที่ตัวจัดการปลั๊กอินและแก้ไขเส้นทางไฟล์

```
// @require https://raw.githubusercontent.com/maboloshi/github-chinese/gh-pages/locals.js?v1 .9.0
```

เปลี่ยน URL ไฟล์ที่อยู่ในเครื่อง เช่น

```
// @require file:///G:\FILE_GITHUB\github-thai\local_th.js
```

> [เคล็ดลับ]
> ลากไฟล์ไปยังแถบที่อยู่ของเบราว์เซอร์โดยตรง จากนั้นคัดลอกที่อยู่ในแถบที่อยู่
