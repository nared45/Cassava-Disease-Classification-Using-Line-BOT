<h1 align="center" id="title">Digital Image Processing Project: Cassava Disease Classification Using Line-BOT</h1>
[ ⚠️ this project was in progress... ]
<p id="description">Project นี้เป็นส่วนหนึ่งของรายวิชา Digital Image Processing Project 02204412-60</p>

## สมาชิกในทีม

| ชื่อ | หน้าที่ |
| --- | --- |
| นายเฉลิมชัย กำลังเดช | Project Manager, AI Developer |
| นายปวิช สังข์วารี | AI Developer , Line Developer |
| นายนเรศ เฟื่องเวโรจน์สกุล | AI Developer , Line Developer |
| นายภูวรินทร์ สังฆมาศ | AI Developer , Plant Pathologist |
| นายธนภัทร ทุเรียนงาม | AI Developer |

## ลำดับการทำงาน
- [x] I. วางแผนการทำงานโครงการ
- [x] II. Paper survey (Model classification, One class classification, Cassava Disease)
- [x] III. Dataset and Preprocessing
- [ ] IV. Train Model / Evaluate (Model Classification)
- [ ] V   Train Model / Evaluate (Model One class classification)
- [ ] V.  Line-BOT UI Design
- [ ] VI. Deploy ML model in Line-BOT

## รายละเอียดแต่ละงาน
I. วางแผนการทำงานโครงการ
| Technology | Function | รายละเอียด
| --- | --- | --- |
|<a href="https://jupyter.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/1200px-Jupyter_logo.svg.png" alt="jupyter" width="80" height="80"/> </a>| IDE | ใช้สำหรับ Coding Python ในการสร้าง Model
|<a href="https://manager.line.biz/" target="_blank" rel="noreferrer"> <img src="https://iconframework.com/assets/img/line-oa.png" alt="Line OA" width="80" height="40"/> </a>| Front-end | ใช้สำหรับการพัฒนาหน้า UI Design ของตัว Line-BOT
|<a href="https://developers.line.biz/en/" target="_blank" rel="noreferrer"> <img src="https://i.scdn.co/image/bc3fe2e52ff72b04e349883f754736b2ae9d799c" alt="LineDev" width="80" height="80"/> </a>| Back-end | ใช้สำหรับการส่ง Webhook และ Deploy ML Model เข้าสู่ Line-BOT
|<a href="https://ngrok.com/" target="_blank" rel="noreferrer"> <img src="https://curity.io/images/resources/tutorials/deploy/tutorials-ngrok.png" alt="ngrok" width="80" height="40"/> </a>| Tool open source | ใช้สำหรับการพัฒนาระบบทำให้ระบบที่พัฒนาอยู่ในเครื่องสามารถ online ได้บน internet สามารถเข้าระบบจากที่ไหนก็ได้ โดยสามารถเข้าใช้งานผ่าน url ของ ngrok

III. Dataset and Preprocessing
<p>Dataset จากการแข่งขัน Research Code Competition : Cassava Leaf Disease Classification เป็นรูปภาพใบมันสำปะหลังที่รวบรวมมาจากชาวไร่ในประเทศยูกันดาและมีการ label ด้วยผู้เชี่ยวชาญจาก National Crops Resources Research Institute (NaCRRI) ร่วมกับ Makerere University </p>

| Disease | Figure | Discription | Amount
| --- | --- | --- | --- |
| cassava bacterial blight (CBB) |<a href="https://apps.lucidcentral.org/pppw_v10/text/web_full/entities/cassava_bacterial_blight_173.htm" target="_blank" rel="noreferrer"> <img src="https://apps.lucidcentral.org/pppw_v10/images/entities/cassava_bacterial_blight_173/cassavabb.jpg" alt="CBB" width="100" height="100"/> </a>| # | 1087
|cassava brown streak disease (CBSD) |<a href="https://apps.lucidcentral.org/pppw_v10/text/web_full/entities/cassava_brown_streak_disease_439.htm" target="_blank" rel="noreferrer"> <img src="https://apps.lucidcentral.org/pppw_v10/images/entities/cassava_brown_streak_disease_439/dsc03920.jpg" alt="CBSB" width="100" height="100"/> </a>| # | 2189
|cassava mosaic disease (CMD) |<a href="https://apps.lucidcentral.org/pppw_v11/text/web_full/entities/cassava_mosaic_diseases_520.htm" target="_blank" rel="noreferrer"> <img src="https://apps.lucidcentral.org/pppw_v11/images/entities/cassava_mosaic_diseases_520/h_holms2.jpg" alt="CMD" width="100" height="100"/> </a>| # | 13158
| Healthy |<a href="https://agrictoday.com.gh/2021/03/19/lifestyle-the-amazing-medicinal-benefits-of-cassava-leaves-that-need-to-be-known/" target="_blank" rel="noreferrer"> <img src="https://agrictoday.com.gh/wp-content/uploads/2021/03/cassava-leaves.jpg" alt="Healthy" width="100" height="100"/> </a>| # | 2577

<p>There are 4 classes of training data, 19,011 photos.</p>
