---
description: >-
 Instance คือ resource หลัก สำหรับ Nipa.Cloud จึงมี operation มากมาย
 ที่ใช้ในการจัดการ Instance 
---

# Instance s Management

### Stop

เมื่อไม่ต้องการใช้งาน Instance แต่ยังไม่ต้องการลบ Instance ตัวนั้นทั้ง หรือต้องการทำ operation อื่นๆ ที่ทำได้เฉพาะตอนที่ Instance อยู่ในสถานะ Shutoff สามารถทำการ Shutoff Instance ด้วยคำสั่ง Stop ได้ โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการ stop

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.ที่ Instance Detail Page ให้เลือกที่ Power Tab เพื่อเข้าสู่ Power Page

![Power Page \(Active Instance \)](../.gitbook/assets/cleaninstall03.png)

3.ที่ Power Page ให้กดปุ่ม Stop เพื่อเข้า Stop Instance Page

![Stop Instance Page](../.gitbook/assets/cleaninstall04.png)

4.กดที่ปุ่ม "Confirm" เพื่อ Stop Instance 

![Power Page \(Shutoff Instance \)](../.gitbook/assets/cleaninstall05.png)



### Start 

เมื่อต้องการกลับมาใช้งาน Instance ที่อยู่ในสถานะ Shutoff ทำได้โดยการสั่ง start Instance โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการ start

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.ที่ Instance Detail Page ให้เลือกที่ Power Tab เพื่อเข้าสู่ Power Page

![Power Page \(Shutoff Instance \)](../.gitbook/assets/cleaninstall09.png)

3.กดที่ปุ่ม Start เพื่อเข้า start Instance Page

![Start Instance Page](../.gitbook/assets/cleaninstall10.png)

4.กดที่ปุ่ม Confirm เพื่อเริ่มใช้งาน Instance 

![Power Page \(Active Instance \)](../.gitbook/assets/cleaninstall11.png)



### Soft Reboot

เมื่อต้องการ reboot Instance ด้วย command ของ OS สามารถทำได้โดยการสั่ง soft reboot โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการทำ soft reboot

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.ที่ Instance Detail Page ให้เลือกที่ Power Tab เพื่อเข้าสู่ Power Page

![Power Page \(Shutoff Instance \)](../.gitbook/assets/cleaninstall09.png)

3.กดที่ปุ่ม Soft Reboot เพื่อเข้าสู่ soft reboot Page

![Soft Reboot Page](../.gitbook/assets/softreboot01.png)

4.กดที่ปุ่ม Confirm เพื่อเริ่มการ soft reboot ระบบจะใช้เวลาสักครู่หนึ่ง เมื่อเสร็จแล้วจะเห็นจุดสีเขียว แสดงสถานะ active ของ Instance 

![Power Page \(Active Instance \)](../.gitbook/assets/cleaninstall11.png)



### Hard Reboot

เมื่อต้องการ reboot Instance ที่ตัวเครื่อง physical สามารถทำได้โดยการสั่ง hard reboot โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการทำ hard reboot

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.ที่ Instance Detail Page ให้เลือกที่ Power Tab เพื่อเข้าสู่ Power Page

![Power Page \(Shutoff Instance \)](../.gitbook/assets/cleaninstall09.png)

3.กดที่ปุ่ม Hard Reboot เพื่อเข้าสู่ hard reboot Page

![Hard Reboot Page](../.gitbook/assets/hardreboot01.png)

4.กดที่ปุ่ม Confirm เพื่อเริ่มการ hard reboot ระบบจะใช้เวลาสักครู่หนึ่ง เมื่อเสร็จแล้วจะเห็นจุดสีเขียว แสดงสถานะ active ของ Instance 

![Power Page \(Active Instance \)](../.gitbook/assets/cleaninstall11.png)



### Rescue

เมื่อ Instance เกิดปัญหากับ OS ทำให้เข้าใช้งานไม่ได้ แต่ต้องการเข้าไปกู้ข้อมูลที่อยู่ภายใน สามารถทำได้โดยการสั่ง Rescue โดยคำสั่งนี้ ระบบจะทำการ Mount OS เปล่าเข้าไป เพื่อให้สามารถเข้าถึงข้อมูลภายใน Instance ได้ โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการทำ Rescue

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.กดที่ปุ่ม Rescue เพื่อเข้า Rescue Page

![](../.gitbook/assets/rescue01.png)

3.ที่ Select Image ให้เลือก Image ที่ต้องการใช้ในการ Mount เพื่อ Rescue Instance นี้ แล้วกดที่ปุ่ม Confirm เพื่อเริ่มทำ Mount Image ที่เลือกเข้าไปที่ Instance ระบบจะใช้เวลาซักครู่นึง เมื่อเสร็จแล้วจะเห็นจุดสีเหลืองแสดงสถานะ Rescue ของ Instance 

![Power Page \(Rescue Instance \)](../.gitbook/assets/rescue02.png)

4.เข้าใช้งาน Instance ได้ตามปกติ ผ่าน Rescue OS ที่ Mount ลงไป



### Clean Install

เมื่อใช้งาน Instance ไปได้ซักพักนึง ก็อาจเกิดปัญหาบางอย่างขึ้น ที่ไม่สามารถแก้ไขได้ หรือแก้ไขได้ยาก การสร้าง Instance ใหม่ตั้งแต่ต้นเลยอาจจะดีกว่า แต่ก็จะต้องเสียเวลาย้าย IP, Port, Network, ฯลฯ ที่เคยใช้งานใน Instance ตัวเดิม ไปยัง Instance ตัวใหม่อีก ทางออกนึงของปัญหานี้ก็คือการใช้ feature Clean Install ที่จะเป็นการล้าง Instance ให้กลับไปเป็นเหมือนตอนสร้างขึ้นมาใหม่นั่นเอง โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการทำ Clean Install

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.Stop Instance ตามวิธีการด้านบน [Instance Operation](instances-management.md#stop)

3.ที่ Instance Detail Page ให้เลือกที่ Power Tab เพื่อเข้าสู่ Power Page และเลื่อนลงมาด้านล่างจะพบปุ่ม Clean Install

![Power Page](../.gitbook/assets/cleaninstall06.png)

4.กดที่ปุ่ม Clean Install เพื่อเข้า Clean Install Page

![Clean Install Page](../.gitbook/assets/cleaninstall07.png)

5.กดที่ปุ่ม "Confirm" เพื่อเริ่มทำ Clean Install ระบบจะใช้เวลาซักครู่นึง เมื่อเสร็จแล้วจะเห็นจุดสีเทาแสดงสถานะของ Instance 

![Power Page \(Shutoff Instance \)](../.gitbook/assets/cleaninstall09.png)

6.start Instance ตามวิธีด้านบน [Instance Operation](instances-management.md#start) และใช้งานต่อได้เลย



### Rebuild 

เมื่อเราต้องการเปลี่ยน OS ของ Instance หรือต้องการ Instance ที่มี Image ตัวอื่น แต่ด้วย config, spec, IP, port, network, ฯลน เดิม เราไม่จำเป็นจะต้อง launch Instance ขึ้นมาใหม่แล้ว setting ใหม่ทั้งหมด เราสามารถใช้ feature Rebuild เพื่อ build Image ใหม่ ไปที่ Instance ตัวเดิมได้ โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการทำ Clean Install

![](../.gitbook/assets/cleaninstall02.png)

2.Stop Instance ตามวิธีการด้านบน [Instance Operation](instances-management.md#stop)

3.ที่ Instance Detail Page ให้เลือกที่ Power Tab เพื่อเข้าสู่ Power Page และเลื่อนลงมาด้านล่างจะพบปุ่ม Rebuild 

![Power Page \(Active Instance \)](../.gitbook/assets/cleaninstall06.png)

4.กดที่ปุ่ม Rebuild เพื่อเข้า Rebuild Page

![Rebuild Page](../.gitbook/assets/rebuild01.png)

5.ที่ Select Image ให้เลือก Image ใหม่ที่ต้องการ build ลงไปใน Instance นี้ แล้วกดที่ปุ่ม Confirm เพื่อเริ่มทำ Rebuild ระบบจะใช้เวลาซักครู่นึง เมื่อเสร็จแล้วจะเห็นจุดสีเทาแสดงสถานะของ Instance 

![Power Page \(Shutoff Instance \)](../.gitbook/assets/cleaninstall09.png)

6.start Instance ตามวิธีด้านบน [Instance Operation](instances-management.md#start) และใช้งานต่อได้เลย



### Resize

เมื่อเราสร้าง Instance มาแล้ว ทำงานไปได้ซักพักนึง ความต้องการของระบบอาจจะมากขึ้น RAM, CPU ไม่พอ การที่จะ launch Instance ขึ้นมาใหม่แล้วถ่ายโอนทุกอย่างไปก็คงจะเป็นเรื่องยาก วิธีนึงที่ช่วยได้ก็คือการ Resize ที่จะเพิ่มขนาดและประสิทธิภาพของ Instance โดยไม่ต้องสร้างใหม่ โดยมีวิธีการดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการทำ Resize

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.Stop Instance ตามวิธีการด้านบน [Instance Operation](instances-management.md#stop)

3.ที่ Instance Detail Page ให้เลือกที่ Resize Tab เพื่อเข้าสู่ Resize Page

![Resize Page](../.gitbook/assets/resize01.png)

4.เลือก Spec ใหม่ที่ต้องการ แล้วกดปุ่ม Resize ที่ด้านล่างเพื่อเข้าสู่ Confirm Resize Page

![Confirm Resize Page](../.gitbook/assets/resize02.png)

5.กดปุ่ม Confirm เพื่อทำการ Resize ระบบจะใช้เวลาสักครุ่ เมื่อเสร็จแล้วระบบจะพากลับไปที่ Resize Page พร้อมแสดง Spec ใหม่ และสถานะของ Instance เป็นสีเท่า

![](../.gitbook/assets/resize03.png)

6.start Instance ตามวิธีด้านบน [Instance Operation](instances-management.md#start) และใช้งานต่อได้เลย



### Attach Volume

เมื่อเราใช้งาน Instance ไปได้สักพักหนึ่ง ความต้องการระบบก็อาจจะเพิ่มขึ้น นอกจากการ Resize \(ดูการ Resize [Instances Management](instances-management.md#resize)\) ที่เพิ่ม RAM, CPU, ROM แล้ว เรายังสามารถเพิ่ม SSD storage เข้าไปที่ Instance เข้าเราได้ โดยการ Attach Volume โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการ Attach Volume

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.ที่ Instance Detail Page ให้เลือกที่ Volumes Tab เพื่อเข้าสู่ Attach Volume Page

![Attach Volume Page \(Without Volume\)](../.gitbook/assets/resize01-1.png)

3.กดปุ่ม Attach เพื่อเข้า Confirm Attach Volume Page

![Confirm Attach Volume Page](../.gitbook/assets/attachvolume02.png)

4.เลือก Volume ที่ต้องการ \(หากไม่มี สามารถสร้างได้โดยมีขั้นตอนดังนี้ [Volumes Management](../storages/volumes-management.md#create-volume)\) แล้วกด Confirm เพื่อทำการ Attach เมื่อเสร็จแล้ว ระบบจะพากลับมาที่ Attach Volume Page โดยจะเห็นว่ามี Volume เพิ่มขึ้นมาก็เป็นอันเสร็จ

![Attach Volume Page \(Volume Attached\)](../.gitbook/assets/attachvolume03.png)


### Detach Volume

เมื่อเราต้องการ launch Instance ใหม่ เพื่อเปลี่ยนแปลงระบบ แต่ยังต้องการใช้ Volume ตัวเดิม เราก็จะต้อง Detach Volume ตัวนั้น ออกจาก Instance ตัวเก่าก่อน โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการ Detach volume

![Instance Detail Page](../.gitbook/assets/cleaninstall02.png)

2.ที่ Instance Detail Page ให้เลือกที่ Volumes Tab เพื่อเข้าสู่ Attach Volume Page

![Attach Volume Page \(Volume Attached\)](../.gitbook/assets/attachvolume03.png)

3.ที่ Volume ที่ต้องการ Detach ให้กดที่ปุ่ม Detach ด้านขวา เพื่อเข้าสู่ Confirm Detach Volume Page

![Confirm Detach Volume Page](../.gitbook/assets/detachvolume01.png)

4.กดที่ปุ่ม Confirm เพื่อทำการ Detach Volume เมื่อเสร็จแล้ว ระบบจะพากลับไปที่ Attach Volume Page โดย Volume ที่เคย Attach อยู่จะหายไป

![Attach Volume Page \(Volume Detached\)](../.gitbook/assets/detachvolume02.png)


### Edit Name

เมื่อเราต้องการเปลี่ยนชื่อของ Instance เพื่อให้ง่ายต่อการจดจำ สามารถทำได้ตามขั้นตอนต่อไปนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการเปลี่ยนชื่อ

![Instance Detail Page](../.gitbook/assets/cleaninstall03.png)

2.คลิกที่ชื่อของ Instance ที่อยู่ด้านบนของ Page เพื่อเข้าสู่ Edit Name Page

![Edit Name Page](../.gitbook/assets/editname01.png)

3.ที่ช่อง Name ใส่ชื่อใหม่ที่ต้องการตั้งให้ Instance นี้ แล้วกดที่ปุ่ม Confirm เพื่อทำการเปลี่ยนชื่อ Instance ระบบจะพากลับไปที่ Instance Detail Page และแสดงให้เห็นชื่อ Instance ที่เปลี่ยนไป

![Instance Detail Page \(Name Edited\)](../.gitbook/assets/editname02.png)


### Destroy Instance 

เมื่อเราไม่ต้องการ Instance แล้ว ก็ควรทำการลบทิ้ง เพื่อไม่ให้ระบบเก็บเงินต่อไป โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP จะพบกับ Instance Page ให้เลือก Instance ที่ต้องการลบ

![Instance Detail Page](../.gitbook/assets/cleaninstall03.png)

2.ที่ Instance Detail Page ให้เลือกที่ Destroy Tab เพื่อเข้าสู่ Destroy Page

![Destroy Page](../.gitbook/assets/destroy01.png)

3.กดที่ปุ่ม Destroy เพื่อเข้าสู่ Confirm Destroy Page

![Confirm Destroy Page](../.gitbook/assets/destroy02.png)

4.ในการลบ Instance เราสามารถลบ external IP ที่ผูกอยู่กับ Instance ตัวนี้ไปด้วยได้ โดยการเช็คที่ Remove External IP หรือหากต้องการเก็บไว้ ให้เอาเช็คออก ก่อนกด Confirm เพื่อทำการลบ Instance 

{% hint style="danger" %}
เมื่อทำการลบ Instance แล้ว จะไม่สามารถู้คืนได้อีก หากต้องการเก็บข้อมูลใน Instance เอาไว้ ให้ลองศึกษาที่การ Create Snapshot เพื่อบันทึก State ของ Instance เอาไว้ 
{% endhint %}





