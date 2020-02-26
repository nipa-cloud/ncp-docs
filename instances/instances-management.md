---
description: >-
  Instance คือ resource หลัก สำหรับ Nipa.Cloud จึงมี operation มากมาย
  ที่ใช้ในการจัดการ  instance
---

# Instances Management

### Stop

เมื่อไม่ต้องการใช้งาน instance แต่ยังไม่ต้องการลบ instance ตัวนั้นทั้ง หรือต้องการทำ operation อื่นๆ ที่ทำได้เฉพาะตอนที่ instance อยู่ในสถานะ shutoff สามารถทำการ shutoff instance ด้วยคำสั่ง stop ได้ โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการ stop

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. ที่ instance detail page ให้เลือกที่ power tab เพื่อเข้าสู่ power page

![Power Page \(Active Instance\)](../.gitbook/assets/cleaninstall03.png)

3. ที่ power page ให้กดปุ่ม stop เพื่อเข้า stop instance page

![Stop Instance Page](../.gitbook/assets/cleaninstall04.png)

4. กดที่ปุ่ม "Confirm" เพื่อ stop instance 

![Power Page \(Shutoff Instance\)](../.gitbook/assets/cleaninstall05.png)



### Start 

เมื่อต้องการกลับมาใช้งาน instance ที่อยู่ในสถานะ shutoff ทำได้โดยการสั่ง start instance โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการ start

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. ที่ instance detail page ให้เลือกที่ power tab เพื่อเข้าสู่ power page

![Power Page \(Shutoff Instance\)](../.gitbook/assets/cleaninstall09.png)

3. กดที่ปุ่ม Start เพื่อเข้า start instance page

![Start Instance Page](../.gitbook/assets/cleaninstall10.png)

4. กดที่ปุ่ม Confirm เพื่อเริ่มใช้งาน instance

![Power Page \(Active Instance\)](../.gitbook/assets/cleaninstall11.png)



### Soft Reboot

เมื่อต้องการ reboot instance ด้วย command ของ OS สามารถทำได้โดยการสั่ง soft reboot โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการทำ soft reboot

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. ที่ instance detail page ให้เลือกที่ power tab เพื่อเข้าสู่ power page

![Power Page \(Shutoff Instance\)](../.gitbook/assets/cleaninstall09.png)

3. กดที่ปุ่ม Soft Reboot เพื่อเข้าสู่ soft reboot page

![Soft Reboot Page](../.gitbook/assets/softreboot01.png)

4. กดที่ปุ่ม Confirm เพื่อเริ่มการ soft reboot ระบบจะใช้เวลาสักครู่หนึ่ง เมื่อเสร็จแล้วจะเห็นจุดสีเขียว แสดงสถานะ active ของ instance

![Power Page \(Active Instance\)](../.gitbook/assets/cleaninstall11.png)



### Hard Reboot

เมื่อต้องการ reboot instance ที่ตัวเครื่อง physical สามารถทำได้โดยการสั่ง hard reboot โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการทำ hard reboot

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. ที่ instance detail page ให้เลือกที่ power tab เพื่อเข้าสู่ power page

![Power Page \(Shutoff Instance\)](../.gitbook/assets/cleaninstall09.png)

3. กดที่ปุ่ม Hard Reboot เพื่อเข้าสู่ hard reboot page

![Hard Reboot Page](../.gitbook/assets/hardreboot01.png)

4. กดที่ปุ่ม Confirm เพื่อเริ่มการ hard reboot ระบบจะใช้เวลาสักครู่หนึ่ง เมื่อเสร็จแล้วจะเห็นจุดสีเขียว แสดงสถานะ active ของ instance

![Power Page \(Active Instance\)](../.gitbook/assets/cleaninstall11.png)



### Rescue

เมื่อ instance เกิดปัญหากับ OS ทำให้เข้าใช้งานไม่ได้ แต่ต้องการเข้าไปกู้ข้อมูลที่อยู่ภายใน สามารถทำได้โดยการสั่ง rescue โดยคำสั่งนี้ ระบบจะทำการ mount OS เปล่าเข้าไป เพื่อให้สามารถเข้าถึงข้อมูลภายใน instance ได้ โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการทำ rescue

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. กดที่ปุ่ม Rescue เพื่อเข้า rescue page

![](../.gitbook/assets/rescue01.png)

3. ที่ Select image ให้เลือก image ที่ต้องการใช้ในการ mount เพื่อ rescue instance นี้ แล้วกดที่ปุ่ม Confirm เพื่อเริ่มทำ mount image ที่เลือกเข้าไปที่ instance ระบบจะใช้เวลาซักครู่นึง เมื่อเสร็จแล้วจะเห็นจุดสีเหลืองแสดงสถานะ rescue ของ instance

![Power Page \(Rescue Instance\)](../.gitbook/assets/rescue02.png)

4. เข้าใช้งาน instance ได้ตามปกติ ผ่าน rescue OS ที่ mount ลงไป



### Clean Install

เมื่อใช้งาน instance ไปได้ซักพักนึง ก็อาจเกิดปัญหาบางอย่างขึ้น ที่ไม่สามารถแก้ไขได้ หรือแก้ไขได้ยาก การสร้าง instance ใหม่ตั้งแต่ต้นเลยอาจจะดีกว่า แต่ก็จะต้องเสียเวลาย้าย IP, Port, Network, ฯลฯ ที่เคยใช้งานใน instance ตัวเดิม ไปยัง instance ตัวใหม่อีก ทางออกนึงของปัญหานี้ก็คือการใช้ feature clean install ที่จะเป็นการล้าง instance ให้กลับไปเป็นเหมือนตอนสร้างขึ้นมาใหม่นั่นเอง โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการทำ clean install

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. stop instance ตามวิธีการด้านบน [Instance Operation](instances-management.md#stop)

3. ที่ instance detail page ให้เลือกที่ power tab เพื่อเข้าสู่ power page และเลื่อนลงมาด้านล่างจะพบปุ่ม clean install

![Power Page](../.gitbook/assets/cleaninstall06.png)

4. กดที่ปุ่ม Clean install เพื่อเข้า clean install page

![Clean Install Page](../.gitbook/assets/cleaninstall07.png)

5. กดที่ปุ่ม "Confirm" เพื่อเริ่มทำ clean install ระบบจะใช้เวลาซักครู่นึง เมื่อเสร็จแล้วจะเห็นจุดสีเทาแสดงสถานะของ instance

![Power Page \(Shutoff Instance\)](../.gitbook/assets/cleaninstall09.png)

6. start instance ตามวิธีด้านบน [Instance Operation](instances-management.md#start) และใช้งานต่อได้เลย



### Rebuild

เมื่อเราต้องการเปลี่ยน OS ของ instance หรือต้องการ instance ที่มี image ตัวอื่น แต่ด้วย config, spec, IP, port, network, ฯลน เดิม เราไม่จำเป็นจะต้อง launch instance ขึ้นมาใหม่แล้ว setting ใหม่ทั้งหมด เราสามารถใช้ feature rebuild เพื่อ build image ใหม่ ไปที่ instance ตัวเดิมได้ โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการทำ clean install

![](../.gitbook/assets/cleaninstall02.png)

2. stop instance ตามวิธีการด้านบน [Instance Operation](instances-management.md#stop)

3. ที่ instance detail page ให้เลือกที่ power tab เพื่อเข้าสู่ power page และเลื่อนลงมาด้านล่างจะพบปุ่ม rebuild

![Power Page \(Active Instance\)](../.gitbook/assets/cleaninstall06.png)

4. กดที่ปุ่ม Rebuild เพื่อเข้า rebuild page

![Rebuild Page](../.gitbook/assets/rebuild01%20%281%29.png)

5. ที่ Select image ให้เลือก image ใหม่ที่ต้องการ build ลงไปใน instance นี้ แล้วกดที่ปุ่ม Confirm เพื่อเริ่มทำ rebuild ระบบจะใช้เวลาซักครู่นึง เมื่อเสร็จแล้วจะเห็นจุดสีเทาแสดงสถานะของ instance

![Power Page \(Shutoff Instance\)](../.gitbook/assets/cleaninstall09.png)

6. start instance ตามวิธีด้านบน [Instance Operation](instances-management.md#start) และใช้งานต่อได้เลย



### Resize

เมื่อเราสร้าง instance มาแล้ว ทำงานไปได้ซักพักนึง ความต้องการของระบบอาจจะมากขึ้น RAM, CPU ไม่พอ การที่จะ launch instance ขึ้นมาใหม่แล้วถ่ายโอนทุกอย่างไปก็คงจะเป็นเรื่องยาก วิธีนึงที่ช่วยได้ก็คือการ resize ที่จะเพิ่มขนาดและประสิทธิภาพของ instance โดยไม่ต้องสร้างใหม่ โดยมีวิธีการดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการทำ resize

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. stop instance ตามวิธีการด้านบน [Instance Operation](instances-management.md#stop)

3. ที่ instance detail page ให้เลือกที่ resize tab เพื่อเข้าสู่ resize pag

![Resize Page](../.gitbook/assets/resize01.png)

4. เลือก spec ใหม่ที่ต้องการ แล้วกดปุ่ม Resize ที่ด้านล่างเพื่อเข้าสู่ Confirm Resize Page

![Confirm Resize Page](../.gitbook/assets/resize02.png)

5. กดปุ่ม Confirm เพื่อทำการ resize ระบบจะใช้เวลาสักครุ่ เมื่อเสร็จแล้วระบบจะพากลับไปที่ resize page พร้อมแสดง spec ใหม่ และสถานะของ instance เป็นสีเท่า

![](../.gitbook/assets/resize03.png)

6. start instance ตามวิธีด้านบน [Instance Operation](instances-management.md#start) และใช้งานต่อได้เลย



### Attach Volume

เมื่อเราใช้งาน instance ไปได้สักพักหนึ่ง ความต้องการระบบก็อาจจะเพิ่มขึ้น นอกจากการ resize \(ดูการ resize [Instances Management](instances-management.md#resize)\) ที่เพิ่ม RAM, CPU, ROM แล้ว เรายังสามารถเพิ่ม SSD storage เข้าไปที่ instance เข้าเราได้ โดยการ attach volume โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการ attach volume

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. ที่ instance detail page ให้เลือกที่ volumes tab เพื่อเข้าสู่ attach volume page

![Attach Volume Page \(Without Volume\)](../.gitbook/assets/resize01-1.png)

3. กดปุ่ม Attach เพื่อเข้า confirm attach volume page

![Confirm Attach Volume Page](../.gitbook/assets/attachvolume02.png)

4. เลือก volume ที่ต้องการ \(หากไม่มี สามารถสร้างได้โดยมีขั้นตอนดังนี้ [Volumes Management](../storages/volumes-management.md#create-volume)\) แล้วกด Confirm เพื่อทำการ attach เมื่อเสร็จแล้ว ระบบจะพากลับมาที่ attach volume page โดยจะเห็นว่ามี volume เพิ่มขึ้นมาก็เป็นอันเสร็จ

![Attach Volume Page \(Volume Attached\)](../.gitbook/assets/attachvolume03.png)



### Detach Volume

เมื่อเราต้องการ launch instance ใหม่ เพื่อเปลี่ยนแปลงระบบ แต่ยังต้องการใช้ volume ตัวเดิม เราก็จะต้อง detach volume ตัวนั้น ออกจาก instance ตัวเก่าก่อน โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการ detach volume

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2. ที่ instance detail page ให้เลือกที่ volumes tab เพื่อเข้าสู่ attach volume page

![Attach Volume Page \(Volume Attached\)](../.gitbook/assets/attachvolume03.png)

3. ที่ volume ที่ต้องการ detach ให้กดที่ปุ่ม Detach ด้านขวา เพื่อเข้าสู่ confirm detach volume page

![Confirm Detach Volume Page](../.gitbook/assets/detachvolume01.png)

4. กดที่ปุ่ม Confirm เพื่อทำการ detach volume เมื่อเสร็จแล้ว ระบบจะพากลับไปที่ attach volume page โดย volume ที่เคย attach อยู่จะหายไป

![Attach Volume Page \(Volume Detached\)](../.gitbook/assets/detachvolume02.png)



### Edit Name

เมื่อเราต้องการเปลี่ยนชื่อของ Instance เพื่อให้ง่ายต่อการจดจำ สามารถทำได้ตามขั้นตอนต่อไปนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการเปลี่ยนชื่อ

![Instance Detail Page](../.gitbook/assets/cleaninstall03.png)

2. คลิกที่ชื่อของ instance ที่อยู่ด้านบนของ page เพื่อเข้าสู่ edit name page

![Edit Name Page](../.gitbook/assets/editname01.png)

3. ที่ช่อง Name ใส่ชื่อใหม่ที่ต้องการตั้งให้ instance นี้ แล้วกดที่ปุ่ม Confirm เพื่อทำการเปลี่ยนชื่อ instance ระบบจะพากลับไปที่ instance detail page และแสดงให้เห็นชื่อ instance ที่เปลี่ยนไป

![Instance Detail Page \(Name Edited\)](../.gitbook/assets/editname02.png)



### Destroy Instance

เมื่อเราไม่ต้องการ instance แล้ว ก็ควรทำการลบทิ้ง เพื่อไม่ให้ระบบเก็บเงินต่อไป โดยมีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP จะพบกับ instance page ให้เลือก instance ที่ต้องการลบ

![Instance Detail Page](../.gitbook/assets/cleaninstall03.png)

2. ที่ instance detail page ให้เลือกที่ destroy tab เพื่อเข้าสู่ destroy page

![Destroy Page](../.gitbook/assets/destroy01.png)

3. กดที่ปุ่ม Destroy เพื่อเข้าสู่ confirm destroy page

![Confirm Destroy Page](../.gitbook/assets/destroy02.png)

4. ในการลบ instance เราสามารถลบ external IP ที่ผูกอยู่กับ instance ตัวนี้ไปด้วยได้ โดยการเช็คที่ Remove External IP หรือหากต้องการเก็บไว้ ให้เอาเช็คออก ก่อนกด Confirm เพื่อทำการลบ instance 

{% hint style="danger" %}
เมื่อทำการลบ instance แล้ว จะไม่สามารถู้คืนได้อีก หากต้องการเก็บข้อมูลใน instance เอาไว้ ให้ลองศึกษาที่การ Create Snapshot เพื่อบันทึก state ของ instance เอาไว้ 
{% endhint %}





