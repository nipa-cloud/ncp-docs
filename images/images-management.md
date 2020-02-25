---
description: >-
  Image คือ resource ที่เอาไปใช้เป็น base ในการ launch instance ได้
  โดยสามารถสร้างได้จากการ create snapshot ซึ่งจะเป็นการบันทึก state ของ instance
  ตัวนัั้นเอาไว้
---

# Images Management

### Restore Image

เมื่อเราต้องการเอา image ที่มีอยู่ ไป build บน instance ตัวเดิม เพื่อเป็นการเปลี่ยน OS หรืออื่นๆ โดยไม่ต้องตั้งค่า IP, port, network, ฯลฯ ใหม่ สามารถทำได้โดยการใช้คำสั่ง restore image ซึ่งก็จะคล้ายกับการ rebuild instance \(ดูได้ที่ [Instances Management](../instances/instances-management.md#rebuild)\) โดยการ restore image มีขั้นตอนดังนี้

1. เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Images ภายใต้กลุ่ม Storage ที่ sidebar เพื่อเข้าสู่ image page

![Images Page](../.gitbook/assets/restoreimage01.png)

2. กดที่ more หลัง image ที่ต้องการ build ทับลงไปที่ instance เพื่อเปิด image menu

![Image Menu](../.gitbook/assets/restoreimage02.png)

3. กดที่ Restore image to existing instance เพื่อเข้าสู่ restore image page

![Restore Image Page](../.gitbook/assets/restoreimage03.png)

4. เลือก instance ที่ต้องการทำการ restore โดยจะต้องเป็น shutoff instance เท่านั้น \(ดูการ stop instance ได้ที่ [Instances Management](../instances/instances-management.md#stop)\) จากนั้นกด Restore แล้วระบบจะพากลับมาที่ images page

![Images Page](../.gitbook/assets/restoreimage04.png)

5. คลิกที่ Instances ภายใต้กลุ่ม Compute ที่ sidebar เพื่อเข้าสู่ instances page จะเห็นว่า instance ที่เลือกจะกำลังดำเนินการอยู่ รอจนกว่าจุดแสดงสถานะ instance จะกลายเป็นสีเทา

![Instances Page](../.gitbook/assets/restoreimage04-1.png)

6. ทำการ start instance \(ดูการ start instance ได้ที่ [Instances Management](../instances/instances-management.md#start)\) และกลับมาใช้งานได้ทันที



### Share Image

เมื่อเราสร้าง image ตัวหนึ่งขึ้นมา แล้วต้องการใช้ร่วมกันกับ user อื่น สามารถทำได้ 2 วิธี คือการเพิ่ม user นั้น เข้ามาใน project เดียวกัน แต่หากไม่ต้องการใช้งาน project ร่วมกัน สามารถทำได้โดยการ share image โดยมีขั้นตอนดังนี้

#### ผู้ส่ง

{% hint style="info" %}
image ที่ share จะยังเป็นของ project ที่สร้างอยู่ แต่สามารถเข้าถึงได้โดย project ที่ share ให้ได้ ซึ่งหมายความว่า หากผู้สร้างลบ image นี้ทิ้ง project อื่นๆก็จะมองไม่เห็น image นั้นอีกต่อไป
{% endhint %}

1. เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Images ภายใต้กลุ่ม Storage ที่ sidebar เพื่อเข้าสู่ image page

![Images Page \(Before Share\)](../.gitbook/assets/restoreimage01.png)

2. กดที่ more หลัง image ที่ต้องการ share เพื่อเปิด image menu

![Image Menu](../.gitbook/assets/restoreimage02.png)

3. กดที่ Manage image sharing เพื่อเข้าสู่ manage image sharing page

![Manage Image Sharing Page](../.gitbook/assets/shareimage01-1.png)

4. ที่ช่อง Project\(s\) ให้ใส่ project ID ของ ผู้รับ share \(ดูได้จาก project page\) แล้วกด enter โดยสามารถ share ได้มากกว่า 1 project และกด Coonfirm เพื่อ share ระบบจะพากลับไปที่ images page พร้อม visibility ของ image ที่ share จะกลายเป็น shared

![Images Page \(After Share\) ](../.gitbook/assets/shareimage02.png)

#### ผู้รับ

1. เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Images ภายใต้กลุ่ม Storage ที่ sidebar เพื่อเข้าสู่ image page

![Images Page \(Before Accept\)](../.gitbook/assets/shareimage05.png)

2. กด accept ที่ image ในหมวด shared เพื่อเข้า confirm accept image page

![Confirm Accept Image Page](../.gitbook/assets/shareimage03.png)

3. กดปุ่ม Confirm เพื่อรับการ share ระบบจะพากลับไปที่ images page พร้อมแสดงสถานะของ image ที่รับมาเป็น active

![](../.gitbook/assets/shareimage04.png)

