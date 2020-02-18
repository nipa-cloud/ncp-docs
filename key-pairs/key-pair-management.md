# Key pair management

ในส่วนของการเข้าถึง instance นั้น จำเป็นต้องมี key หรือรหัสผ่าน เพื่อความปลอดภัยของข้อมูลภายใน instance ของผู้ใช้งานเอง โดยผู้ใช้งานสามารถสร้าง key ได้ด้วยตนเอง ซึ่ง key ที่ได้จากการสร้าง เรียกว่า "Key pair" เมื่อสร้างแล้วผู้ใช้งานจะสามารถนำ public key ที่ได้ ไปใช้งาน โดยผู้ใช้งานสามารถจัดการกับ key pair ได้ ดังนี้

**Table of contents**

* \*\*\*\*[**Create**](key-pair-management.md#create)\*\*\*\*
  * [Generate Key](key-pair-management.md#generate-key)
  * [Import Key](key-pair-management.md#import-key)
* \*\*\*\*[**Set Default**](key-pair-management.md#set-default)\*\*\*\*
* \*\*\*\*[**Remove**](key-pair-management.md#remove)\*\*\*\*



## Create

### Generate Key

เป็นการสร้าง โดยทางระบบจะ generate key ให้

1.คลิก Create Key pair

![](../.gitbook/assets/create_keypair_1.png)

2.หลังจากคลิกแล้ว หน้า popup จะแสดงขึ้นมา เลือก tab "Import" ซึ่งจะประกอบด้วยข้อมูล ดังนี้  
     - **name**: ระบบจะทำการ random ชื่อ key pair ให้ เป็น default ผู้ใช้งานสามารถแก้ไขได้

![](../.gitbook/assets/create_keypair_2.png)

3.คลิก Generate ระบบจะ download file key pair \(.pem\) ที่ generate มาให้ผู้ใช้งานสามารถนำ public key ไปใช้งานได้  โดยชื่อไฟล์จะเป็นชื่อตามที่ผู้ใช้งานกรอกตอน create และจะแสดงรายชื่อ key pair ภายใน table

![&#xE44;&#xE1F;&#xE25;&#xE4C; Key pair](../.gitbook/assets/create_keypair_4.png)

![](../.gitbook/assets/create_keypair_5.png)

{% hint style="info" %}
ผู้ใช้งานสามารถ คลิก show ในตารางส่วนของ column "public key" เพื่อ copy public key ไปใช้งาน instance ได้
{% endhint %}

![](../.gitbook/assets/create_keypair_8%20%281%29.png)

### Import Key

ผู้ใช้งานสามารถ import key ของตนเองได้ โดยทางระบบจะรองรับ key ประเภท **rsa**, **dsa**, **ecdsa** และ **ed25519**

1.คลิก Create Key pair

![](../.gitbook/assets/create_keypair_1.png)

2.หลังจากคลิกแล้ว หน้า popup จะแสดงขึ้นมา เลือก tab "Import" ซึ่งจะประกอบด้วยข้อมูล ดังนี้  
     - **Name**: ระบบจะทำการ random ชื่อ key pair ให้ เป็น default ผู้ใช้งานสามารถแก้ไขได้  
     - **Public key**: ส่วนที่ให้ผู้ใช้งานกรอก key ของตนเอง โดยระบบจะรองรับ key โดยทางระบบจะรองรับ key ประเภท **rsa**, **dsa**, **ecdsa** และ **ed25519**

![](../.gitbook/assets/create_keypair_6.png)

3.คลิก Confirm ระบบจะทำการสร้าง key pair ตามที่ผู้ใช้งานกรอก และแสดงรายชื่อ key pair ภายใน table

![](../.gitbook/assets/create_keypair_7.png)

{% hint style="info" %}
ผู้ใช้งานสามารถ คลิก show ในตารางส่วนของ column "public key" เพื่อ copy public key ไปใช้งาน instance ได้
{% endhint %}

![](../.gitbook/assets/create_keypair_8.png)

## Set Default

การ set default key pair คือ การตั้งค่าในการเลือก default key pair ในขณะที่สร้าง instance ผู้ใช้งานสามารถจัดการได้ด้วยตนเอง เมื่อสร้าง key pair เรียบร้อยแล้ว เริ่มต้น status จะเป็น Disable

1.คลิก Enable หรือ Disable \(ขึ้นอยู่กับ status ขณะนั้น\) ในส่วนของ column "default" key pair

![&#xE40;&#xE23;&#xE34;&#xE48;&#xE21;&#xE15;&#xE49;&#xE19;  status: Disable](../.gitbook/assets/set_default_1.png)

![](../.gitbook/assets/set_default_3.png)

2.หลังจากคลิกแล้ว หน้า popup จะแสดงขึ้นมา ให้คลิก Confirm

![](../.gitbook/assets/set_default_2.png)

3.ระบบจะแสดง status ตามที่ผู้ใช้งานตั้งค่า

![Status: Enable](../.gitbook/assets/set_default_3%20%281%29.png)

![Status: Disable](../.gitbook/assets/set_default_1%20%281%29.png)

## Remove

1.เลือก key pair ที่ต้องการลบ \(ผู้ใช้งานสามารถลบหลาย key pair พร้อมกันได้\)

![](../.gitbook/assets/remove_1.png)

2.คลิกปุ่ม Remove

![](../.gitbook/assets/remove_2.png)

3.หลังจากคลิกแล้ว หน้า popup จะแสดงขึ้นมา และแสดงรายชื่อ key pair ที่ต้องการลบ ให้คลิก Confirm

![](../.gitbook/assets/remove_3.png)

4.key pair ที่เลือกจะถูกลบไป ซึ่งจะไม่ปรากฏในตาราง

![](../.gitbook/assets/remove_4.png)

