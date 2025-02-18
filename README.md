# iKB-1 Plugin for KidBrightIDE

ปลั๊กอินสำหรับบอร์ด iKB-1 ต่อขยายขาของบอร์ด KidBright32 ให้มีขาต่อใช้งาน-

 1. เซ็นเซอร์ / อุปกรณ์ดิจิทัลอินพุตเอาพุต / อุปกรณ์แอนาล็อกเอาต์พุต จำนวน 8 ช่อง
 2. เซอร์โวมอเตอร์ รองรับรุ่น 180 องศา และ 360 องศา จำนวน 6 ช่อง
 3. มอเตอร์ ไดร์ภายใน 2 ช่อง และไดร์ภายนอกจำนวน 2 ช่อง
 4. Serial / UART / RS232 (TTL) จำนวน 1 ช่อง

![โครงสร้างบอร์ด iKB-1](https://sv1.picz.in.th/images/2018/12/21/9wPDr0.png)

## การติดตั้ง

### สำหรับ KidBrightIDE เวอร์ชั่น New UI

ใช้การติดตั้งจาก Source code

 1. ดาวน์โหลดไฟล์ปลั๊กอินเวอร์ชั่น Source code ได้ที่ส่วนดาวน์โหลด (อยู่ด้านล่างของหน้านี้)
 2. เปิดโปรแกรม KidBrightIDE กด Plugins > Install Plugins
 3. เลือกไฟล์ปลั๊กอินที่ดาวน์โหลดไว้
 4. โปรแกรม KidBrightIDE จะปิดแล้วเปิดใหม่ บล็อกใหม่จะอยู่ในเมนู iKB-1

### สำหรับ KidBright เวอร์ชั่นเก่า

ใช้การติดตั้งด้วยโปรแกรมช่วยติดตั้ง

 1. ดาวน์โหลดไฟล์ปลั๊กอินเวอร์ชั่น Installer ได้ที่ส่วนดาวน์โหลด (อยู่ด้านล่างของหน้านี้)
 2. แตกไฟล์ zip ออกมา จะได้ไฟล์ชื่อ `iKB-1 Installer Vx.x.x.exe` ให้ดับเบิลคลิกเปิดไฟล์นี้
 3. ปลั๊กอินจะถูกติดตั้งให้อัตโนมัติ และแจ้งผลการติดตั้ง
 4. เปิดโปรแกรม KidBrightIDE บล็อกจะอยู่ในเมนู ปลั๊กอิน > iKB-1

### สำหรับ KidBright ที่ Clone มาจาก GitLab

กรณีต้องการใช้ตัวช่วยติดตั้ง

 1. ดาวน์โหลดไฟล์ปลั๊กอินเวอร์ชั่น Installer ได้ที่ส่วนดาวน์โหลด (อยู่ด้านล่างของหน้านี้)
 2. แตกไฟล์ zip ออกมา จะได้ไฟล์ชื่อ `iKB-1 Installer Vx.x.x.exe` ให้ดับเบิลคลิกเปิดไฟล์นี้
 3. โปรแกรมช่วยติดตั้งจะแจ้งค้นหาโปรแกรม KidBrightIDE ไม่เจอ พร้อมแจ้งให้เลือกโฟลเดอร์ kbide
 4. เลือกโฟลเดอร์ `kbide` ที่สั่ง Clone มา
 5. ปลั๊กอินจะถูกติดตั้งให้อัตโนมัติ และแจ้งผลการติดตั้ง
 6. เปิดโปรแกรม KidBrightIDE บล็อกจะอยู่ในเมนู ปลั๊กอิน > iKB-1

กรณีต้องการติดตั้งเอง

 1. ดาวน์โหลดไฟล์ปลั๊กอินเวอร์ชั่น Source code ได้ที่ส่วนดาวน์โหลด (อยู่ด้านล่างของหน้านี้)
 2. แตกไฟล์ที่ได้ดาวน์โหลดมา จะได้โฟลเดอร์ ikb_1_plugin
 3. ย้ายโฟลเดอร์ `ikb_1_plugin` ไปไว้ที่โฟลเดอร์ `kbide/plugins`
 4. เปิดโปรแกรม KidBrightIDE บล็อกจะอยู่ในเมนู ปลั๊กอิน > iKB-1

## การใช้งาน

ต่อบอร์ด iKB-1 เข้ากับบอร์ด KidBright32 ด้วยสาย KB Chain ที่แถมมาด้วย

![914LxP.jpg](https://sv1.picz.in.th/images/2018/12/21/914LxP.jpg)

## บล็อกอ่านค่าดิจิทัล

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านค่าดิจิทัล](https://sv1.picz.in.th/images/2018/12/25/9iQKWI.png) | ![digital read](https://sv1.picz.in.th/images/2018/12/25/9ixIk2.png) |

ใช้อ่านค่าดิจิทัลจากช่อง 0 ถึง 7 (JST สีแดง) ให้ค่าออกมาเป็นตัวเลข 0, 1 และจริง เท็จตามลอจิกที่อ่านได้จริง ใช้งานกับบล็อกเงื่อนไข (if) และบล็อกไม่ (Not) ได้

**ตัวอย่างการนำไปใช้**

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![โค้ดโปรแกรมแสดงรูปยิ้มเมื่อมีคนเดินผ่าน](https://sv1.picz.in.th/images/2018/12/25/9iEqln.png) | ![9iE5Gg.png](https://sv1.picz.in.th/images/2018/12/25/9iE5Gg.png) |

ใช้บล็อกนี้เพื่ออ่านค่าจาก PIR เซ็นเซอร์ - เมื่อ PIR ตรวจจับความเคลื่อนไหวได้ จะให้เอาต์พุตออกมาเป็นลอจิก 1 บล็อกอ่านค่าดิิจิตอล อ่านค่าได้ 1 จึงเข้าเงื่อนไข แล้วแสดงรูปยิ้มออกมาทางหน้าจอของบอร์ด KidBright

## บล็อกเขียนค่าดิจิทัล

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกเขียนค่าดิจิทัล](https://sv1.picz.in.th/images/2018/12/25/9iQwnZ.png) | ![digital write](https://sv1.picz.in.th/images/2018/12/25/9iQWXy.png) |

ใช้เขียนค่าลอจิก 0/1 หรือ จริง/เท็จ ไปที่ช่อง 0 ถึง 7 (ช่อง JST สีแดง) เพื่อสั่งงานอุปกรณ์ต่าง ๆ เช่น หลอด LED

**ตัวอย่างการนำไปใช้**

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![โค้ดไฟวิ่ง](https://sv1.picz.in.th/images/2018/12/25/9ibNPZ.png) | ![9ibWaq.png](https://sv1.picz.in.th/images/2018/12/25/9ibWaq.png) |

ใช้บล็อกนี้เพื่อสั่งหลอด LED - ในวันคริสมาสต้องการให้หลอดไฟที่ต้นคริสมาสติดตามรูปแบบที่กำหนด จึงเขียนโปรแกรมสั่งให้หลอด LED ติดทีละดวงไปเรื่อย ๆ โดยดวงสุดท้ายติดอยู่ที่ดาวของต้นคลิสมาส จึงให้สว่างค้างนานกว่างดวงอื่น ๆ

## บล็อกอ่านค่าแอนาล็อก

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านค่าแอนาล็อก](https://sv1.picz.in.th/images/2018/12/25/9iQZKP.png) | ![analog read](https://sv1.picz.in.th/images/2018/12/25/9ixMO1.png) |

ใช้อ่านค่าแอนาล็อก ความละเอียด 10 บิต จากช่อง 0 ถึง 7 (ช่อง JST สีแดง) ให้ค่าออกมาเป็นตัวเลข 0 ถึง 1023

**ตัวอย่างการนำไปใช้**

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![โค้ดเครื่องวัดความสุขของต้นไม้](https://sv1.picz.in.th/images/2018/12/25/9ib3ae.png) | ![9ibT4l.png](https://sv1.picz.in.th/images/2018/12/25/9ibT4l.png) |

ใช้บล็อกนี้กับเซ็นเซอร์วัดความชื้นในดิน - ต้องการสร้างเครื่องวัดความสุขของต้นไม้ จึงรวบรวมสิ่งที่บ่งบอกได้ว่าต้นไม้มีความสุข หนึ่งในนั้นคือความชื้นในดิน หากความชื้นในดินพอเหมาะ ก็จะทำให้ต้นไม้ได้รับสารอาหารเพียงพอ ส่งผลให้ต้นไม้มีความสุข

จึงใช้บล็อกอ่านค่าแอนาล็อกอ่านค่าแอนาล็อกจากเซ็นเซอร์ออกมา แล้วแปลงออกมาเป็นคะแนนความสุขของต้นไม้ 1 ถึง 5

## บล็อกควบคุมมอเตอร์

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกควบคุมมอเตอร์](https://sv1.picz.in.th/images/2018/12/21/9w85XP.png) | ![set motor](https://sv1.picz.in.th/images/2018/12/25/9iQ3aR.png) |

ใช้ควบคุมมอเตอร์ที่ต่อช่อง 1, 2 (ไดร์บนบอร์ด) และช่อง 3, 4 (ไดร์ภายนอก) ควบคุมทิศทาง หมุนตาม/หมุนทวน และควบคุมความเร็ว 0 ถึง 100%

**ตัวอย่างการนำไปใช้**

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![โค้ดสั่งหุ่นยนต์หมุนรอบตัวเอง](https://sv1.picz.in.th/images/2018/12/21/9wVNlD.png) | ![9ibcPV.png](https://sv1.picz.in.th/images/2018/12/25/9ibcPV.png) |

ใช้ควบคุมการหมุนของล้อในหุ่นยนต์เดินตามเส้น - ต้องการให้หุ่นยนต์หมุนรอบตัวเอง 3 รอบ จึงใช้บล็อกควบคุมมอเตอร์ สั่งให้ล้อขวาไม่วิ่ง (ล้อขวาต่อกับมอเตอร์ และมอเตอร์ต่อกับช่องขับมอเตอร์ 1) และใช้บล็อกควบคุมมอเตอร์สั่งให้ล้อซ้ายหมุนตามเข็มที่ความเร็ว 50% ทดสอบหุ่นยนต์หมุน 1 รอบใช้เวลา 4 วินาที จึงหน่วงเวลา 3 รอบ * 4 วินาที = 12 วินาที

## บล็อกควบคุมเซอร์โวมอเตอร์ 180 องศา

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกควบคุมเซอร์โวมอเตอร์ 180 องศา](https://sv1.picz.in.th/images/2018/12/21/9wV8w1.png) | ![set servo](https://sv1.picz.in.th/images/2018/12/25/9iQtxu.png) |

ใช้ควบคุมเซอร์โว 180 องศา ที่ต่อช่อง 10 ถึง 15 (ในโปรแกรม ช่อง 1 คือช่อง 10) ให้หมุน 0 ถึง 200 องศา

**ตัวอย่างการนำไปใช้**

![9wXRA1.jpg](https://sv1.picz.in.th/images/2018/12/21/9wXRA1.jpg)

*ที่มา: https://blog.arduino.cc/2016/09/05/unlock-your-door-with-a-simple-hand-gesture/*

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![โค้ดล็อกประตูด้วยเซอร์โวมอเตอร์](https://sv1.picz.in.th/images/2018/12/21/9waQZe.png) | ![9ibxbn.png](https://sv1.picz.in.th/images/2018/12/25/9ibxbn.png) |

สั่งเซอร์โวมอเตอร์ให้ล็อกประตู - ต้องการสร้างกลอนล็อกประตูอิเล็กทรอนิกส์ พบว่ากลอนที่ใช้อยู่เป็นแบบเลื่อนล็อก จึงใช้เซอร์โวมอเตอร์มาต่อกับกลอนประตู ทดสอบการทำงานโดยกดปุ่ม S1 ให้ล็อกประตู และกดปุ่ม S2 ให้ปลดล็อก

ทดสอบสั่งงานเซอร์โวมอเตอร์แล้ว หากต้องการให้ประตูล็อก ต้องสั่งใหเซอร์โวมอเตอร์หมุน 100 องศา และหากต้องการปลดล็อก ต้องสั่งให้หมุน 5 องศา จึงเขียนโปรแกรมเมื่อกดปุ่ม S1 ให้เซอร์โวหมุน 100 องศา และเมื่อกดปุ่ม S1 ให้เซอร์โวหมุน 5 องศา

## บล็อกควบคุมเซอร์โวมอเตอร์ 360 องศา

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกควบคุมเซอร์โวมอเตอร์ 360 องศา](https://sv1.picz.in.th/images/2018/12/21/9waoUQ.png) | ![set servo 2](https://sv1.picz.in.th/images/2018/12/25/9iQT40.png) |

ใช้ควบคุมเซอร์โวปรับแต่ง ที่ต่อช่อง 10 ถึง 15 (ในโปรแกรม ช่อง 1 คือช่อง 10) ให้ หมุนตาม/หมุนทวน และควบคุมความเร็ว 0 ถึง 100%

**ตัวอย่างการนำไปใช้**

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![โค้ดสั่งให้หุ่นยนต์เดินหน้า 1 เมตร](https://sv1.picz.in.th/images/2018/12/21/9wvdhy.png) | ![9ibLUl.png](https://sv1.picz.in.th/images/2018/12/26/9ibLUl.png) |

ใช้ควบคุมเซอร์โวมอเตอร์ที่ต่อกับล้อของหุ่นยนต์ - ต้องการให้หุ่นยนต์ส่งของวิ่งไปที่จุดส่งของที่ห่างออกไป 1 เมตร ตัวหุ่นยนต์ใช้เซอร์โวมอเตอร์ 360 องศา เป็นตัวขับเคลื่อน ทดสอบแล้วที่ความเร็ว 100% ใช้เวลา 5 วินาที จะวิ่งได้ 1 เมตรพอดี ในโค้ดโปรแกรมจึงกำหนดให้เซอร์โวมอเตอร์หมุน 100% เป็นเวลา 5 วินาที

**หมายเหตุ** ในโค้ดให้หุ่นบนต์หมุนล้อเดียวเพื่อเป็นตัวอย่างเท่านั้น ความเป็นจริงต้องสั่งให้ล้อหมุน 2 ล้อพร้อมกัน หุ่นยนต์จึงจะวิ่งตรง

## บล็อกเกี่ยวกับการสื่อสารผ่าน Serial

บล็อกเกี่ยวการสื่อสารผ่าน Serial สามารถใช้งานได้กับโมดูลบลูทูธ HC-05 / HC-06 และโมดูลอื่นที่สื่อสารผ่าน Serial มีบล็อกให้ใช้งานดังนี้

### บล็อกตั้งค่า Baud rate

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกตั้งค่า Baud rate](https://sv1.picz.in.th/images/2018/12/21/9wv1zZ.png) | ![serial baud rate](https://sv1.picz.in.th/images/2018/12/25/9iQBeq.png) |

ใช้ตั้งค่า baud rate ของการรับ-ส่งข้อมูลผ่าน Serial สามารถตั้งได้ 9600/2400/57600 หรือ 115200

### บล็อกส่งข้อความ

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกส่งข้อความ](https://sv1.picz.in.th/images/2018/12/21/9wv5aN.png) | ![serial write](https://sv1.picz.in.th/images/2018/12/25/9i5txy.png) |

ใช้ส่งข้อความที่เป็น String ผ่าน Serial โดยมี 2 บล็อกให้เลือก คือส่งข้อมูลอย่างเดียว หรือส่งข้อมูลพร้อมขึ้นบรรทัดใหม่

### บล็อกอ่านข้อมูลที่รออ่านจากบัฟเฟอร์

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านข้อมูลที่รออ่านจากบัฟเฟอร์](https://sv1.picz.in.th/images/2018/12/21/9wvoWn.png) | ![serial available](https://sv1.picz.in.th/images/2018/12/25/9iQ0zD.png) |

บัฟเฟอร์เปรียบเสมือนที่เก็บข้อมูลชั่วคราว เมื่อมีการส่งข้อมูลมา ข้อมูลจะถูกเก็บลงบัฟเฟอร์ เมื่อต้องการอ่านข้อมูล จึงไปอ่านจากบัฟเฟอร์ บล็อกนี้ใช้อ่านจำนวนข้อมูลที่รออ่านจากบัฟเฟอร์ ให้ข้อมูลเป็นตัวเลข 0 ถึง 255

### บล็อกอ่านข้อมูล 1 ไบต์

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านข้อมูล 1 ไบต์](https://sv1.picz.in.th/images/2018/12/22/9KTqPI.png) | ![serial read one byte](https://sv1.picz.in.th/images/2018/12/25/9iQzWb.png) |

ใช้อ่านข้อมูล 1 ไบต์ จะให้เอาต์พุตออกมาเป็นตัวเลขรหัสแอสกี้

### บล็อกอ่านข้อมูลเป็น String ตามจำนวนตัวอักษรที่กำหนด

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านข้อมูลเป็น String ตามจำนวนตัวอักษรที่กำหนด](https://sv1.picz.in.th/images/2018/12/21/9wvjnS.png) | ![9iQ7x9.png](https://sv1.picz.in.th/images/2018/12/25/9iQ7x9.png) |

ใช้อ่านข้อมูลเป็นชุดแบบ String ตามจำนวนตัวอักษรที่กำหนด สามารถนำเอาต์พุตจากบล็อกนี้ ไปใส่บล็อก แอลอีดี 16x8 (ทุกบล็อก) ได้

### บล็อกอ่านข้อความ

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านข้อความ](https://sv1.picz.in.th/images/2018/12/22/9KTUZZ.png) | ![serial read string](https://sv1.picz.in.th/images/2018/12/25/9iQ4Kf.png) |

ใช้อ่านข้อมูลเป็นชุดแบบ String โดยจะคำนวณตัวอักษรที่ต้องอ่านออกมาอัตโนมัติ สามารถนำเอาต์พุตจากบล็อกนี้ ไปใส่บล็อก แอลอีดี 16x8 (ทุกบล็อก) ได้

### บล็อกอ่านข้อความ 1 บรรทัด

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านข้อความ 1 บรรทัด](https://sv1.picz.in.th/images/2018/12/22/9KT5mP.png) | ![serial read line](https://sv1.picz.in.th/images/2018/12/25/9iQS6J.png)

ใช้อ่านข้อมูลเป็นชุดแบบ String โดยจะตัดข้อความออกมาเมื่อเจอตัวขึ้นบรรทัดใหม่ (\n) สามารถนำเอาต์พุตจากบล็อกนี้ ไปใส่บล็อก แอลอีดี 16x8 (ทุกบล็อก) ได้

### บล็อกอ่านข้อความ จำกัดความยาวจากตัวอักษรที่กำหนด

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![บล็อกอ่านข้อความ จำกัดความยาวจากตัวอักษรที่กำหนด](https://sv1.picz.in.th/images/2018/12/22/9KTO9t.png) | ![serial read until](https://sv1.picz.in.th/images/2018/12/25/9iQNAa.png) |

ใช้อ่านข้อมูลเป็นชุดแบบ String โดยจะตัดข้อความออกมาเมื่อเจอตัวอักษรที่กำหนด โดยตัวอักษรที่กำนดจะต้องมีความยาว 1 ตัวอักษรเท่านั้น สามารถนำเอาต์พุตจากบล็อกนี้ ไปใส่บล็อก แอลอีดี 16x8 (ทุกบล็อก) ได้

**ตัวอย่างการนำไปใช้**

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![9ij0lS.png](https://sv1.picz.in.th/images/2018/12/26/9ij0lS.png) | ![9ijYBg.png](https://sv1.picz.in.th/images/2018/12/26/9ijYBg.png) |

แสดงค่าอุณหภูมิบนแอพพลิเคชั่น รับ-ส่งข้อมูลด้วยบลูทูธโดยใช้ HC-05 - ศูนย์ข้อมูลหนึ่งต้องการมอนิเตอร์อุณหภูมิตลอดเวลา เพื่อตรวจสอบการทำงานของแอร์ เมื่อแอร์เสียเจ้าหน้าที่สามารถสั่งปิดเครื่องเซอร์เวอร์ได้ เพื่อไม่ให้เกิดความเสียหายกับเครื่องเซิร์ฟเวอร์เมื่ออุณหภูมิสูงเกิน

จากความต้องการดังกล่าว หัวหน้าผู้ดูแลศูนย์ข้อมูลต้องการข้อมูลแบบทันที จึงใช้เซ็นเซอร์บนบอร์ด KidBright32 วัดอุณหภูมิ แล้วส่งข้อมูลผ่านบอร์ด iKB-1 ไปที่ HC-05 และข้อมูลจึงถูกส่งไปยังหัวหน้าผู้ดูแลศูนย์ข้อมูลแบบทันที

หัวหน้าผู้ดูแลศูนย์ข้อมูลต้องการทดสอบการทำงานของระบบที่ออกแบบขึ้น จึงให้บอร์ด KidBright32 แสดงผลข้อมูลที่รับได้จากบลูทูธด้วย

## บล็อกเสริมสำหรับทำ Robot Car

บล็อกส่วนนี้ สร้างมาเพื่อให้นำ iKB-1 ไปใช้งานร่วมกับบอร์ด KidBright สร้างรถเดินตามเส้น รถบังคับ หรือรถแบบอื่น ๆ อำนวยความสะดวกด้วยบล็อกกำหนดการทำงานของมอเตอร์ที่ใช้งานง่ายขึ้น

### บล็อกวิ่งไปข้างหน้าแบบกำหนดความเร็ว

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjbM1.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjbM1.jpg) | ![tcOvmu.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOvmu.jpg) |

ใช้สั่งให้รถวิ่งไปข้างหน้าด้วยความเร็วตามที่กำหนด โดยกำหนดความเร็วได้ 0 ถึง 100%

### บล็อกวิ่งถอยหลังแบบกำหนดความเร็ว

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjlwy.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjlwy.jpg) | ![tcOps0.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOps0.jpg) |

ใช้สั่งให้รถวิ่งถอยหลังด้วยความเร็วตามที่กำหนด โดยกำหนดความเร็วได้ 0 ถึง 100%

### บล็อกสั่งให้รถเดินหน้ากำหนดความเร็วล้อ

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjoDD.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjoDD.jpg) | ![tcOJ9Z.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOJ9Z.jpg) |

ใช้สั่งให้รถเดินหน้าโดยกำหนดความเร็วแต่ละล้อเอง ใช้แก้ปัญหารถวิ่งไม่ตรงได้

### บล็อกสั่งให้รถเดินหน้ากำหนดความเร็วล้อ

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjDL9.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjDL9.jpg) | ![tcOLbI.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOLbI.jpg) |

ใช้สั่งให้รถเดินหน้าโดยกำหนดความเร็วแต่ละล้อเอง ใช้แก้ปัญหารถวิ่งไม่ตรงได้

### บล็อกเลี้ยวซ้ายแบบกำหนดความเร็ว

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjPhJ.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjPhJ.jpg) | ![tcOepP.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOepP.jpg) |

ใช้สั่งให้รถเลี้ยวซ้ายด้วยความเร็วตามที่กำหนด โดยกำหนดความเร็วได้ 0 ถึง 100%

### บล็อกเลี้ยวขวาแบบกำหนดความเร็ว

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjsEb.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjsEb.jpg) | ![tcOyNt.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOyNt.jpg) |

ใช้สั่งให้รถเลี้ยวขวาด้วยความเร็วตามที่กำหนด โดยกำหนดความเร็วได้ 0 ถึง 100%

### บล็อกหมุนซ้ายแบบกำหนดความเร็ว

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcj2Xf.jpg](https://sv1.picz.in.th/images/2019/03/15/tcj2Xf.jpg) | ![tcOFQe.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOFQe.jpg) |

ใช้สั่งให้รถหมุนซ้ายด้วยความเร็วตามที่กำหนด โดยกำหนดความเร็วได้ 0 ถึง 100%

### บล็อกหมุนขวาแบบกำหนดความเร็ว

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjuYa.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjuYa.jpg) | ![tcOIrl.jpg](https://sv1.picz.in.th/images/2019/03/15/tcOIrl.jpg) |

ใช้สั่งให้รถหมุนขวาด้วยความเร็วตามที่กำหนด โดยกำหนดความเร็วได้ 0 ถึง 100%

### บล็อกสั่งให้รถหยุด

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcj6Rq.jpg](https://sv1.picz.in.th/images/2019/03/15/tcj6Rq.jpg) | ![tcbW0k.jpg](https://sv1.picz.in.th/images/2019/03/15/tcbW0k.jpg) |

ใช้สั่งให้รถหยุดวิ่ง

### ข้อแตกต่างระหว่างรถเลี้ยวและรถหมุน

กรณีรถเลี้ยวซ้าย/หมุนซ้าย

|  | ล้อซ้าย | ล้อขวา |
|--|--|--|
| รถเลี้ยว | หยุด | วิ่งไปข้างหน้า |
| รถหมุน | วิ่งถอยหลัง | วิ่งไปข้างหน้า |

กรณีรถเลี้ยวขวา/หมุนขวา

|  | ล้อซ้าย | ล้อขวา |
|--|--|--|
| รถเลี้ยว | วิ่งไปข้างหน้า | หยุด |
| รถหมุน | วิ่งไปข้างหน้า | วิ่งถอยหลัง |

**ตัวอย่างการนำไปใช้**

โค้ดสั่งให้รถวิ่งวน

| บล็อกภาษาไทย | บล็อกภาษาอังกฤษ |
|--|--|
| ![tcjpkZ.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjpkZ.jpg) | ![tcjXLu.jpg](https://sv1.picz.in.th/images/2019/03/15/tcjXLu.jpg) |

## แหล่งจ่ายไฟ

บนบอร์ด iKB-1 ใช้แรงดันไฟฟ้า 5V และ 3.3V ซึ่งแต่ละจุดต่อจะให้แรงดันเอาต์พุตไม่เท่ากันดังนี้

### แหล่งจ่ายไฟ 3.3V

แหล่งจ่ายไฟ 3.3V ได้รับแรงดันไฟฟ้ามาจาก 2 ส่วน คือแรงดันที่ได้จากบอร์ด KidBright32 ผ่านช่อง KB Chain และแรงดันที่มาจากช่อง DC Input 7-9Vdc ผ่านเรกกูเลเตอร์ 2A

แหล่งจ่ายไฟ 3.3V ใช้จ่ายไฟเลี้ยงให้กับไอซีไมโครคอนโทรลเลอร์หลักของบอร์ด ดังนั้นเพียงเสียบสาย KB Chain ก็ทำให้บอร์ดทำงานได้เลย และทำให้บอร์ดสามารถใช้งานกับอุปกรณ์บางอย่างได้

ช่องต่อที่ใช้แหล่งจ่ายไฟ 3.3V มีดังนี้

 * ช่อง GPIO 0-7 (JST สีแดง)
 * ช่องต่อ Serial RX/TX
 * ช่องต่อมอเตอร์ ชุดที่ 3 และ 4

ช่องต่อเหล่านี้จำเป็นต้องใช้งานกับอุปกรณ์ที่ใช้แรงดันไฟฟ้า 3.3V เท่านั้น **มิฉนั้นอาจจะทำให้บอร์ด iKB-1 เสียหาย**

### แหล่งจ่ายไฟ 5V

แหล่งจ่ายไฟ 5V ได้รับแรงดันไฟฟ้ามาจากช่อง DC Input 7-9Vdc ผ่านเรกกูเลเตอร์ 2A ช่วยจ่ายไฟให้ช่องต่อ ต่อไปนี้

 * ช่องต่อมอเตอร์ ชุดที่ 1 และ 2
 * ช่องต่อเซอร์โวมอเตอร์
 
**ไม่สามารนำอุปกรณ์ที่ใช้แรงดันไฟเลี้ยง 3.3V มาต่อกับช่องดังกล่าวได้**

### สรุปเรื่องแหล่งจ่ายไฟ

![ผังแรงดันไฟฟ้าในแต่ละจุดของบอร์ด iKB-1](https://sv1.picz.in.th/images/2019/02/27/TyMmH0.png)

ช่องเสียบต่อไปนี้ เสียบเข้ากับช่องต่อแล้วใช้งานได้เลย

 * ช่อง GPIO 0-7 (JST สีแดง)
 * ช่องต่อ Serial RX/TX
 * ช่องต่อมอเตอร์ ชุดที่ 3 และ 4
 
และช่องเสียบต่อไปนี้ ต้องเสียบอะแดปเตอร์ 7-9Vdc เพิ่มเติม

 * ช่องต่อมอเตอร์ ชุดที่ 1 และ 2
 * ช่องต่อเซอร์โวมอเตอร์
