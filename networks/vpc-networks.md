---
description: >-
  Virtual Private Cloud (VPC) ช่วยเพิ่มความปลอดภัยของ Network บน Cloud ซึ่งแยก
  Subnetworks ของผู้ใช้หลายคนและป้องกันการสื่อสารข้าม Virtual networks
  ของผู้ใช้ที่แตกต่างกัน
---

# VPC Networks

## Create Network

### Network

1.เข้าหน้า VPC Network แล้วคลิกที่ปุ่ม "Create" ที่ด้านขวาบน เพื่อสร้าง Network  

![](../.gitbook/assets/vcp_network_1.png)

2.คลิกที่ปุ่ม "Network"  

![](../.gitbook/assets/vcp_network_2.png)

3.กรอกข้อมูลและ Setting ต่างๆของ Router โดยมีรายละเอียดดังต่อไปนี้  
   **Name** : ตั้งชื่อของ Router \(ภายในช่องข้อความระบบจะมีชื่อ Default ให้ โดยทางผู้ใช้งานสามารถตั้งชื่อใหม่ได้\)  
   **CIDR** : ระบุว่าที่อยู่ IP จะมีจำนวนบิตเท่าใด  
   **Cloud firewall** : กำหนดว่า Router จะมี Cloud firewall หรือไม่  
   **DHCP** : กำหนดว่า Router จะมี DHCP หรือไม่  
   **Gateway to router** : กำหนดว่า Router จะ Attach Router ไว้หรือไม่  

![](../.gitbook/assets/vcp_network_3.png)

4.คลิกที่ปุ่ม "Create"  

![](../.gitbook/assets/vcp_network_4.png)

## Action

### Remove

1.คลิกที่ "more"  ใน Column "action" ของ Network ที่ต้องการทำ Action  

![](../.gitbook/assets/vcp_network_9.png)

2.เลือกเมนู "Remove"  

![](../.gitbook/assets/vcp_network_10.png)

3.ระบบจะแจ้งเตือน Subnet และ Port ที่จะโดนลบไปพร้อมกับ Network ด้วย หากเรายืนยันต้องการจะลบ ให้คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_11.png)

### Rename

1.คลิกที่ "more"  ใน Column "action" ของ Network ที่ต้องการทำ Action  

![](../.gitbook/assets/vcp_network_9_2.png)

2.เลือกเมนู "Rename"  

![](../.gitbook/assets/vcp_network_12.png)

3.กรอกชื่อใหม่ที่ต้องการตั้งให้ Router ลงในช่อง แล้วคลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_13.png)

### Disable defualt cloud firewall

1.คลิกที่ "more"  ใน Column "action" ของ Network ที่ต้องการทำ Action  

![](../.gitbook/assets/vcp_network_9_3.png)

2.เลือกเมนู "Disable defualt cloud firewall"  

![](../.gitbook/assets/vcp_network_14.png)

3.คลิกที่ปุ่ม "Disabled"  

![](../.gitbook/assets/vcp_network_15.png)

## Setting Subnet

### DHCP

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการทำการ Setting  

![](../.gitbook/assets/vcp_network_16.png)

2.คลิกที่ปุ่ม "Setting"  

![](../.gitbook/assets/vcp_network_17.png)

3.คลิกที่สวิตช์ที่มุมขวาบน "Enable/Disable dhcp" เพื่อเปิดหรือปิด DHCP  

![](../.gitbook/assets/vcp_network_18.png)

4.คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_19.png)

### DNS nameservers

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการทำการ Setting  

![](../.gitbook/assets/vcp_network_16_2%20%281%29.png)

2.คลิกที่ปุ่ม "Setting"  

![](../.gitbook/assets/vcp_network_17_2.png)

3.เลือกเมนู "DNS nameservers"  

![](../.gitbook/assets/vcp_network_20.png)

4.กำหนด DNS ลงในช่องข้อความ \(สูงสุด 2 IP\)  

![](../.gitbook/assets/vcp_network_21.png)

5.คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_22.png)

### Allocation pools

**Allocation Pool** คือ ช่วงที่อยู่ IP ใน CIDR Network Block ที่อนุญาตให้ใช้โดยบริการ Cloud หากต้องการยกเว้นที่อยู่ IP บางส่วนจาก Subnet คุณสามารถลดขนาด Pool และเพิ่มช่วงที่อยู่ IP ใหม่ที่ไม่ต่อเนื่องกันได้ \(Non-contiguous IP address range\)

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการทำการ Setting  

![](../.gitbook/assets/vcp_network_16_3.png)

2.คลิกที่ปุ่ม "Setting"  

![](../.gitbook/assets/vcp_network_17_3.png)

3.เลือกเมนู "Allocation pools"   

![](../.gitbook/assets/vcp_network_23.png)

4.คลิกที่สวิตช์ "Set IP addresses" เพื่อเปิดการ Set IP  

![](../.gitbook/assets/vcp_network_24.png)

5.กำหนด IP Range ลงในช่องข้อความ  

![](../.gitbook/assets/vcp_network_25.png)

6.คลิกที่ปุ่ม "Add" หากต้องการเพิ่ม IP Range \(Optional\)  

![](../.gitbook/assets/vcp_network_26.png)

7.คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_27.png)

### Host router

ใช้ในกรณีต้องการกำหนด Traffic route ไปยัง Gateway ที่ไม่ใช่ Default

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการทำการ Setting  

![](../.gitbook/assets/vcp_network_16_4.png)

2.คลิกที่ปุ่ม "Setting"  

![](../.gitbook/assets/vcp_network_17_4.png)

3.เลือกเมนู "Host router"  

![](../.gitbook/assets/vcp_network_28.png)

4.กรอกข้อมูลลงในช่องข้อความ  
   **Destination IP** คือ IP ต้นทาง  
   **Nexthop IP** คือ IP ปลายทาง  

![](../.gitbook/assets/vcp_network_29.png)

5.คลิกที่ปุ่ม "Add" หากต้องการเพิ่ม Traffic \(Optional\)  

![](../.gitbook/assets/vcp_network_30.png)

6.คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_31.png)

## Create Port

### Port

1.เข้าหน้า VPC Network แล้วคลิกที่ปุ่ม "Create" ที่ด้านขวาบน เพื่อสร้าง Port  

![](../.gitbook/assets/vcp_network_5.png)

2.คลิกที่ "Port"  

![](../.gitbook/assets/vcp_network_6.png)

3.กรอกข้อมูลและ Setting ต่างๆของ Port โดยมีรายละเอียดดังต่อไปนี้  
   **Name** : ตั้งชื่อของ Port \(ภายในช่องข้อความระบบจะมีชื่อ Default ให้ โดยทางผู้ใช้งานสามารถตั้งชื่อใหม่ได้\)  
   **Network** : กำหนด Network ที่จะสร้าง Port ลงไป  
   **IP Address** : กำหนด IP Address ของ Port  
   **MAC Address** : กำหนด MAC Address ของ Port  
   **Cloud firewall** : กำหนด Cloud firewall ของ Port \( Cloud firewall จะสามารถเลือกประเภทได้ตามที่กำหนดไว้ในหน้า Network -&gt; Cloud Firewalls \)  

![](../.gitbook/assets/vcp_network_7.png)

4.คลิกที่ปุ่ม "Create"  

![](../.gitbook/assets/vcp_network_8.png)

## 

## Action Port

### Enable cloud firewall

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการ Setting  

![](../.gitbook/assets/vcp_network_16_2.png)

2.คลิกที่ "more"  ใน Column "action" ของ Port ที่ต้องการ Setiing  

![](../.gitbook/assets/vcp_network_32.png)

3.เลือกเมนู "Enable cloud firewall"  

![](../.gitbook/assets/vcp_network_33.png)

4.คลิกที่ปุ่ม "Enabled"  

![](../.gitbook/assets/vcp_network_34.png)

{% hint style="info" %}
เมนู "Enable cloud firewall" จะแสดงก็ต่อเมื่อ Port นั้นๆ Disable cloud firewall อยู่
{% endhint %}

### Disable cloud firewall

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการ Setting  

![](../.gitbook/assets/vcp_network_16_3%20%281%29.png)

2.คลิกที่ "more"  ใน Column "action" ของ Port ที่ต้องการ Setiing  

![](../.gitbook/assets/vcp_network_35.png)

3.เลือกเมนู "Disable cloud firewall"  

![](../.gitbook/assets/vcp_network_36.png)

4.คลิกที่ปุ่ม "Disabled"  

![](../.gitbook/assets/vcp_network_37.png)

{% hint style="info" %}
เมนู "Disable cloud firewall" จะแสดงก็ต่อเมื่อ Port นั้นๆ Enable cloud firewall อยู่
{% endhint %}

###  Mac address pair setting

ใช้ในกรณีต้องการกำหนด MAC/IP address \(range\)  เพิ่มลงไปใน Port มีขั้นตอนดังนี้

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการ Setting  

![](../.gitbook/assets/vcp_network_16_4%20%281%29.png)

2.คลิกที่ "more"  ใน Column "action" ของ Port ที่ต้องการ Setiing  

![](../.gitbook/assets/vcp_network_38.png)

3.เลือกเมนู "Mac address pair setting"  

![](../.gitbook/assets/vcp_network_39.png)

4.กรอกข้อมูลลงในช่องข้อความ  
   **IP Address or CIDR** : กำหนด IP Address ของ Port \(สามารถกำหนดเป็น CIDR ได้\)  
   **MAC Address** : กำหนด MAC Address ของ Port  

![](../.gitbook/assets/vcp_network_40.png)

5.คลิกที่ปุ่ม "Add" หากต้องการเพิ่ม MAC/IP Address \(Optional\)

![](../.gitbook/assets/vcp_network_41.png)

6.คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_42.png)

{% hint style="info" %}
เมนู "Mac address pair setting" จะแสดงก็ต่อเมื่อ Port นั้นๆ Enable cloud firewall อยู่
{% endhint %}



### Remove

1.คลิกที่ "subnet"  ใน Column "subnet" ของ Network ที่ต้องการทำการ Setting  

![](../.gitbook/assets/vcp_network_16_5.png)

2.คลิกที่ "more"  ใน Column "action" ของ Port ที่ต้องการ Remove  

![](../.gitbook/assets/vcp_network_43.png)

3.เลือกเมนู "Remove"   

![](../.gitbook/assets/vcp_network_44.png)

4.คลิกที่ปุ่ม "Confirm"  

![](../.gitbook/assets/vcp_network_45.png)

{% hint style="info" %}
เมนู "Remove" จะแสดงก็ต่อเมื่อเป็น Port ที่ผู้ใช้งานสร้างขึ้น
{% endhint %}

