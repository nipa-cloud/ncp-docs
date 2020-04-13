---
description: >-
  Cloud firewall ทำหน้าที่เปรียบเสมือนตัวจัดการอนุญาตการใช้งาน port บน instance
  ระบบมีกฎสำเร็จรูปซึ่งผู้ใช้งานสามารถเลือกใช้ได้ เช่น Ping, SSH, RDP และ
  HTTP-HTTPS
---

# Cloud Firewalls

## Create

### Customize

เป็นการสร้าง Cloud firwall ตัวใหม่ขึ้นมา โดยผู้ใช้งานจะสามารถตั้งชื่อเองได้ มีขั้นตอนดังนี้

1.เข้าหน้า Cloud Firewalls แล้วคลิกที่ปุ่ม "Cloud Firewall" ที่ด้านขวาบน เพื่อสร้าง

![](../.gitbook/assets/cloud_firewall_1.png)

2.คลิกที่ "Customize"

![](../.gitbook/assets/cloud_firewall_2.png)

3.ตั้งชื่อ Cloud Firewall แล้วหลังจากนั้น คลิกที่ปุ่ม "Create"

![](../.gitbook/assets/cloud_firewall_3.png)

4.จะพบ Cloud Firewall ที่สร้างขึ้นมาอยู่ใน List ดังภาพ

![](../.gitbook/assets/cloud_firewall_4.png)

### Default

ใช้ในกรณีที่ต้องการสร้าง Cloud firewall ที่เป็น Default ของระบบใหม่อีกครั้ง ซึ่งทางระบบจะทำการสร้างขึ้นมาใหม่ให้เฉพาะตัวที่ไม่มีอยู่ในระบบ  
โดย Cloud firewall ที่เป็น Default ของระบบมีดังนี้ All, default, Http-Https, In-Cluster, Ping, Rdp, SSH มีขั้นตอนดังนี้

1.เข้าหน้า Cloud Firewalls แล้วคลิกที่ปุ่ม "Cloud Firewall" ที่ด้านขวาบน เพื่อสร้าง

![](../.gitbook/assets/cloud_firewall_5.png)

2.คลิกที่ "Default"

![](../.gitbook/assets/cloud_firewall_6.png)

3.คลิกที่ปุ่ม "Create"

![](../.gitbook/assets/cloud_firewall_7.png)

4.จะพบ Cloud Firewall ที่สร้างขึ้นมาอยู่ใน List ดังภาพ

![](../.gitbook/assets/cloud_firewall_8.png)

## Remove

ผู้ใช้งานสามารถลบ Cloud firewalls ได้ทุกตัว ยกเว้น "default"

1.คลิกเลือก Cloud Firewalls ที่ต้องการลบ

![](../.gitbook/assets/cloud_firewall_9.png)

2.คลิกที่ปุ่ม "Remove"

![](../.gitbook/assets/cloud_firewall_10.png)

3.คลิกที่ปุ่ม "Confirm"

![](../.gitbook/assets/cloud_firewall_11.png)

4.Cloud Firewalls จะเหลือเฉพาะตัวที่ยังไม่ลบ ดังภาพ

![](../.gitbook/assets/cloud_firewall_12.png)

## Add Rules

การเพิ่ม Rule ใน Cloud Firewalls มีอยู่ 2 ประเภท คือ **Ingress** และ **Egress**  
**Ingress** : คือการเขียน Rules เพื่อป้องกัน packet ที่เข้ามาจาก Internet  
**Egress** : คือการเขียน Rules เพื่อป้องกัน packet ที่ออกจาก Internal network

1.คลิกที่ปุ่ม "more" ของ Cloud Firewall ที่ผู้ใช้งานต้องการเพิ่ม Rule

![](../.gitbook/assets/cloud_firewall_13.png)

2.คลิกที่ปุ่ม "Add Rule" ของ Ingress หรือ Egress

![](../.gitbook/assets/cloud_firewall_14.png)

3.เลือกประเภทของ Rule ที่จะสร้าง  
**Express Rules** : คือ Rule สำเร็จรูปซึ่งระบบจะทำการสร้าง Rule ให้อัตโนมัติตามประเภทที่ผู้ใช้งานเลือก ซึ่งผู้ใช้งานสามารถกำหนดได้เพียง Remote  
**Customs Rule** : คือ Rule สำเร็จรูปที่สามารถ Protocols, Custom Port และ Remote ได้

![](../.gitbook/assets/cloud_firewall_15.png)

โดยสามารถทำตามขั้นตอนได้ดังนี้

### Express Rules

1.เลือก Rule ที่ต้องการ

![](../.gitbook/assets/cloud_firewall_16.png)

2.กำหนด Remote

![](../.gitbook/assets/cloud_firewall_17.png)

3.กด Confirm

![](../.gitbook/assets/cloud_firewall_18.png)

### Customs Rule

1.เลือก Rule และ Protocols ที่ต้องการ

![](../.gitbook/assets/cloud_firewall_19.png)

2.กำหนด Port

![](../.gitbook/assets/cloud_firewall_20.png)

2.กำหนด Remote

![](../.gitbook/assets/cloud_firewall_21.png)

3.กด Confirm

![](../.gitbook/assets/cloud_firewall_22.png)

จะได้ผลลัพธ์ดังภาพ

![](../.gitbook/assets/cloud_firewall_23.png)

## Remove Rules

การลบ Rule ใน Cloud Firewalls มีขั้นตอนดังนี้

1.คลิกที่ปุ่ม "more" ของ Cloud Firewall ที่ผู้ใช้งานต้องการลบ Rule

![](../.gitbook/assets/cloud_firewall_24.png)

2.คลิกที่ปุ่ม "remove" ของ Rule ที่ต้องการลบ

![](../.gitbook/assets/cloud_firewall_25.png)

3.คลิกที่ปุ่ม "Confirm"

![](../.gitbook/assets/cloud_firewall_26.png)

4.จะได้ผลลัพธ์ดังภาพ

![](../.gitbook/assets/cloud_firewall_27.png)

