---
description: >-
  Volume คือ Resource ที่เพิ่มขีดจำกัดในการทำงานของ Instance ในด้านของ Storage
  ขยายพื้นที่จัดเก็บข้อมูลเพิ่มเติมจาก Machine Type ที่เลือกไว้
---

# Volumes Management

## Create Volume

การสร้าง Volume เพื่อใช้เป็น Storage เพิ่มเติมให้กับ Instance โดยมีขั้นตอนในการสร้างดังนี้

1.เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Volumes ภายใต้กลุ่ม Storage ที่ Sidebar เพื่อเข้าสู่หน้า Volumes

![Volume Page](../.gitbook/assets/volume1.png)

2.คลิกปุ่ม Volume ที่บริเวณด้านขวาบนของหน้า เพื่อเข้าสู่หน้า Create Volume

![Create Volume Button](../.gitbook/assets/volume2.png)

![Create Volume Page](../.gitbook/assets/volume3.png)

ที่หน้า Create Volume ให้ใส่ข้อมูลดังต่อไปนี้

* **Name:** ชื่อของ Volume
* **Source:** สร้าง Volume ตัวนี้จากอะไร มีให้เลือก 3 แบบ ดังต่อไปนี้
  * Blank:  สร้าง Volume ธรรมดา
  * Image: สร้าง Volume จาก Image
  * Existing Volume: สร้าง Volume จาก Volume ที่มีอยู่
* **Size:** ขนาดของ Volume
* **Perfomance Type:** ชนิดของ Volume โดยจะมีให้เลือกแค่ Corporate เท่านั้น

![](../.gitbook/assets/volume4.png)

3.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Confirm เพื่อสร้าง Volume ระบบจะพากลับไปที่หน้า Volumes พร้อมแสดง Volume ที่ถูกสร้าง

![Volume Creation Complete](../.gitbook/assets/volume5.png)

## Extend Volume

เมื่อสร้าง Volume ขึ้นมาแล้ว แต่มีขนาดไม่เพียงพอต่อการใช้งาน สามารถขยายขนาดได้ด้วยการ Extend ซึ่งมีขั้นตอนดังนี้

1.ที่หน้า Volumes ให้กดปุ่ม more ที่ด้านขวาของ Volume ที่ต้องทำการ Extend

![](https://github.com/Pippint/ncp-docs/tree/05b73fbad8e759a98f8409f55506d168c80b1ab5/.gitbook/assets/extend_volume_1.png)

2.กดที่ปุ่ม Extend เพื่อเข้าหน้า Extend Volume

![Volume Options](../.gitbook/assets/volume7.png)

ที่หน้า Extend Volume ให้ใส่ข้อมูลดังต่อไปนี้

* **Volume name:** ชื่อของ Volume ที่ต้องการ Extend
* **Current size:** ขนาดปัจจุบันของ Volume
* **New size:** ขนาดใหม่ที่ต้องการ

![Extend Volume Page](../.gitbook/assets/volume8.png)

3.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Confirm เพื่อ Extend Volume ระบบจะพากลับไปที่หน้า Volumes พร้อมแสดง Volume ที่ถูก Extend แล้ว

![Volume Page with Extended Volume](../.gitbook/assets/volume9.png)

## Attach Volume

เมื่อมี Volume ตามขนาดที่ต้องการแล้ว ก็ต้องเอาไปใช้ โดยการ Attach เข้ากับ Instance โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Volumes ภายใต้กลุ่ม Storage ที่ Sidebar เพื่อเข้าสู่หน้า Volume

![](https://github.com/Pippint/ncp-docs/tree/05b73fbad8e759a98f8409f55506d168c80b1ab5/.gitbook/assets/attach_volume_1.png)

2.กดที่ปุ่ม Attach เพื่อเข้าหน้า Attach Volume

![](https://github.com/Pippint/ncp-docs/tree/05b73fbad8e759a98f8409f55506d168c80b1ab5/.gitbook/assets/attach_volume_2.png)

3.เลือกชื่อของ Instance ที่ต้องการ Attach Volume เข้าไป

![Attach Volume Page](../.gitbook/assets/volume10.png)

4.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Confirm เพื่อ Attach Volume ระบบจะพากลับไปที่หน้า Volumes พร้อมแสดง Volume ที่ถูก attach แล้ว

![Volume Page with Attached Volume \(Instance Name Show in &quot;in use by&quot;\)](../.gitbook/assets/volume11.png)

## Detach Volume

เมื่อต้องการสลับ Volume ไปใส่ไว้ที่ Instance อื่น หรือต้องการลบ Volume จะต้องทำการ Detach ก่อน โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Volumes ภายใต้กลุ่ม Storage ที่ sidebar เพื่อเข้าสู่หน้า Volume

![](https://github.com/Pippint/ncp-docs/tree/05b73fbad8e759a98f8409f55506d168c80b1ab5/.gitbook/assets/detach_volume_1.png)

2.กดที่ปุ่ม Detach เพื่อเข้าหน้า Detach Volume

![](../.gitbook/assets/volume12.png)

3.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Confirm เพื่อ Detach Volume ระบบจะพากลับไปที่หน้า Volumes พร้อมแสดง Volume ที่ถูก Detach แล้ว

![Confirm Detach Volume Page](../.gitbook/assets/volume13.png)

![Volumes Page with Instance Detached](../.gitbook/assets/volume14.png)

## Transfer Volume

นอกจากเราจะใช้ Volume เป็น Storage เพิ่มเติมกับ instance ของเราเองได้แล้ว เรายังสามารถ Transfer Volume ของเราไปให้ Project ได้อีกด้วย โดยมีขั้นตอนดังนี้

1.เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Volumes ภายใต้กลุ่ม Storage ที่ Sidebar เพื่อเข้าสู่หน้า Volume

![](../.gitbook/assets/transfer_volume_1.png)

2.กดที่ปุ่ม Transfer เพื่อเข้าสู่หน้า Transfer Volume

![](https://github.com/Pippint/ncp-docs/tree/05b73fbad8e759a98f8409f55506d168c80b1ab5/.gitbook/assets/transfer_volume_2.png)

ที่หน้า Transfer Volume ให้ใส่ข้อมูลดังต่อไปนี้

* **Transfer name:** ชื่อของการ Tansfer นี้
* **E-mail destination:** Email ของผู้รับ Volume

![Transfer Volume Page](../.gitbook/assets/volume14-1.png)

3.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Confirm เพื่อ Transfer Volume หลังจากนั้นระบบจะทำการส่ง Email ข้อมูลที่จำเป็นต้องใช้ในการรับ Transfer Volume ไปให้ และจะแสดงข้อมูลให้สามารถ Download เก็บไว้ได้ด้วย

![Volume Transfer Information Review Page](../.gitbook/assets/volume16.png)

4.ตรวจสอบข้อมูลให้ถูกต้องและ Dowload หากต้องการ เรียบร้อยแล้วแล้วกดปุ่ม Close ระบบจะพากลับไปที่หน้า Volumes พร้อมแสดง Volume ที่อยู่ในสถานะรอการรับ Transfer ซึ่งจะยังคงใช้งานได้ จนกว่าผู้รับจะทำการ Accept Transfer

![Volumes Page with a Volume Trasfer Wait For Accept](../.gitbook/assets/volume17.png)

## Accept Volume Transfer

หลังจากได้รับ Email Volume Transfer แล้ว สามารถทำการ Accept ได้ ตามขั้นตอนต่อไปนี้

1.เมื่อได้รับข้อมูลการ Volume Transfer มา โดยจะต้องประกอบด้วย Transfer ID และ Authorization Key

{% hint style="info" %}
**ตัวอย่างข้อมูล**

```text
Transfer ID: f9045302-9dcb-4473-b88e-6ad5ed86eb66
Transfer Name: sample
Authorization Key: 63f85bb5b3b20385
```
{% endhint %}

2.เมื่อ Login เข้ามาใน NCP ให้คลิกที่ Volumes ภายใต้กลุ่ม Storage ที่ Sidebar เพื่อเข้าสู่หน้า Volume

![](../.gitbook/assets/accept_volume_transfer_1.png)

3.กดที่ปุ่ม Accept Transfer เพื่อเข้าสู่หน้า Accept Transfer Volume

![Accept Transfer Volume Page](../.gitbook/assets/volume18.png)

4.ที่หน้า Accept Transfer Volume ให้ใส่ข้อมูลตามที่ได้รับมาทาง Email หรือทางอื่นๆ

![](../.gitbook/assets/volume19.png)

5.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Accept เพื่อ Accept Volume ระบบจะพากลับไปที่หน้า Volumes พร้อมแสดง Volume ที่ได้รับมา

![Volume Page with Transfered Volume](../.gitbook/assets/volume19-1.png)

