# Project management

Project คือกลุ่มของ Resource ที่สามารถเข้าถึงได้โดยสมาชิกของโปรเจค นั้น ๆ ซึ่งสมาชิกนั้นจะมีอยู่ด้วยกัน 3 ประเภท ได้แก่

* **Owner** คือ เจ้าของและผู้ที่สร้าง Project มีสิทธิ์ในการเข้าถึง Resource ทุกอย่างของ Project สามารถจัดการการชำระเงินของ Project ผ่านหน้า Billing รวมถึงมีสิทธิ์ในการจัดการ Project และ สมาชิกของ Project ได้
* **Billing** คือ สมาชิกที่สามารถจัดการการชำระเงินของโปรเจค ผ่านหน้า Billing ได้
* **Member** คือ สมาชิกที่มีสิทธิ์ในการเข้าถึง Resource ทุกอย่างของ Projectได้

{% hint style="info" %}
Document นี้จะพูดถึงการจัดการโปรเจคและสมาชิกของโปรเจค ดังนั้นจะสามารถทำได้เฉพาะสมาชิกที่เป็น **Owner** เท่านั้น
{% endhint %}

**Table of contents**

1. [Create a Project](Project-management.md#create-a-Project)
2. [Manage member](Project-management.md#manage-member)
3. [Edit contact](Project-management.md#edit-contact)
4. [Change Project & billing types](Project-management.md#change-Project-and-billing-types)
5. [Remove Projec](Project-management.md#remove-Project)t

## **Create a Project**

เนื่องจาก User 1 คนสามารถเป็นสมาชิกได้มากกว่า 1 Project เพื่อจัดการงานและ Resource กับหลากหลายทีม ซึ่งเมื่อ User สมัครสมาชิกเข้ามาใน NCP ก็ได้มี Project ของตัวเองเป็นพื้นฐานอยู่แล้ว 1 Project แต่เมื่อเราต้องการสร้างทีมใหม่ๆ สิ่งที่ต้องทำก็คือต้องสร้าง Project ใหม่ขึ้นมา โดยการสร้าง Project มีขั้นตอนดังต่อไปนี้

1.เมื่อ Login เข้ามาใน NCP จะพบ Dropdown สำหรับเลือกเปลี่ยน Project และตัวเลือกสุดท้ายของ Dropdown จะเป็นปุ่ม ![](https://lh4.googleusercontent.com/udc6vOXZZ7JPLmzsrbLl3f3wqYQ0v1IUvsrXTExIcqU7yrI2iFxPLzlhFnH61JRAoQTmJcPeAjgKgTpW6gAk8yScWjwdx7JMRm7nOsNKE35c3C8uj7PesSAhTMOidW3QO015mO0) ให้คลิกเพื่อเข้าสู่หน้าสร้าง Project

![](https://lh4.googleusercontent.com/g5P_vgETVlD0_WSc6EMHowuOKX-4ymly6zg-kuVYPsuW_d8rj7-QpTqz1oIrnCh0Ttz7NOQvv0Rqd2if59g0Mz0LgxRm_Zu1whcuSSm6S9cUt1RP_9PVBSxjkJJ2yj9XfwzocLY)

ที่หน้า **Create Project** ให้ใส่ข้อมูลดังต่อไปนี้

* **Project name**: ชื่อ Project ที่จะแสดงที่ Dropdown และ page Project
* **Contact phone number**: เบอร์โทรศัพท์ที่ Admin ของเราจะใช้ในการติดต่อเมื่อเกิดปัญหากับ Project ของคุณ โดยจะมีเบอร์โทรศัพท์ของ User ปัจจุบัน เป็นค่าพื้นฐาน
* **Contact email\(s\):** \(maximum email input limit 10\) email ที่ใช้ในการแจ้งข่าวสารต่างๆ โดยจะมี email ของสมาชิก Project เป็นค่าพื้นฐาน และสามารถเพิ่ม email อื่นๆได้อีกไม่เกิน 10 email

![](https://lh6.googleusercontent.com/nxlbz1NsqgXGdbUZ13zWlZ8nv2kX3dWLy4HoK8kensPzBLmH4n0DJ6BPBIiT07bs9x5Pr0mNZFBrULEn8bDBUL58nMRFuYsKKTyJlRe4bVMDSsy8lv35hlLe0m5_6e3DLHZM204)

2.ตรวจสอบข้อมูลที่ใส่ให้ถูกต้อง แล้วกดปุ่ม Create Project หลังจากนั้น ระบบจะพาไปที่หน้า Project พร้อมเลือก Project ที่สร้างเสร็จแล้วให้ทันที เพื่อใช้งานอื่น ๆ ต่อไป

![](https://lh6.googleusercontent.com/Juw1i0bjDrn6EYRhrYzTfbY0BefGnHfOKmUy-qgePaaF4G-cgFcB6hr7CVj6aYvu9IT8ctS22buF3QSdkIgJ858UWWTQBgdyaC2pOIRtBsqnST0TkyD5dShRJkbV7GFQg4FLM-I)

## **Manage member**

เมื่อเรามี Project แล้ว แต่ Project เป็น Concept ที่สร้างขึ้นเพื่อทำงานร่วมกัน ดังนั้นก็จะต้องมีการจัดการสมาชิกในโปรเจ็ค เช่นการ เพิ่ม-ลบ สมาชิกใน Project และการกำหนดสิทธิ์ให้แต่ละคน

### **Add member**

การเพิ่มสมาชิกมีขั้นตอนดังนี้

1.ที่หน้า Project ให้คลิกที่ปุ่ม ![](https://lh6.googleusercontent.com/7OAa9QILUnStkWvk_gtqD68djtW1lmO9RLZgtkKZlsNy42rccOlg46q40OIu2-0a66oYrsMTTG-zvkRJyTTNtiME4MMLdM0fsV5SkJUDHd5_Nxe_OCXKeQzZlhjaw1JNvRKzfUs) จะเป็นการเปิดหน้าต่างเพิ่มสมาชิกขึ้นมา

![](https://lh6.googleusercontent.com/6QVol-UIzvb5lQoL_waEbPMFSuNKEVmInG5icG4VVHI3bpmfDuWlwWWQUljvM7H36WMYxniwolv41eCVSIiR_aH6WUv3yvCPh58yZkPzRA8R8IRbaw9bxe8sYXVuKielFnt8ZXI)

ที่หน้า **Add user** ให้ใส่ข้อมูลดังต่อไปนี้

* **Email\(s\):** ใส่ Email ของ User ที่ต้องการเพิ่มเข้ามาใน Project โดยสามารถใส่ได้ทั้ง email ของ User ที่มีในระบบ NCP และไม่ได้อยู่ในระบบ NCP ด้วย
* **Role:** เลือกประเภทของสมาชิกที่ต้องการเพิ่มใน Project

![](https://lh4.googleusercontent.com/pLSikyzk-aqGyAfEcAtVF6TU66pxxa2zGT40wK_b6tybZmx-H_J-rOXwk-Pt2CsrMs6mz5JuJndVC0O_loJLgOkh6fxP3TA-TQH4udqhbnh0d4LlFMQshTs3IkPvZrbn1w-kPQM)

2.ตรวจสอบข้อมูลที่ใส่ให้ถูกต้อง แล้วกดปุ่ม Next หลังจากนั้น ระบบจะพาไปที่หน้าสรุป ที่จะบอกว่ามี Email ใดบ้างที่มีในระบบและจะถูกเพิ่มเข้ามาใน Project ทันที และ Email ใดบ้างที่ไม่มีในระบบ และจะถูกส่ง Email ชวนสมัครสมาชิกไป

![](https://lh3.googleusercontent.com/YRsZkez-PkKvH3Jh00I9wJJOqwcD7IbwWZEbILzgqUZSV43Weu0IY8Od7aua41cYJT2TCXmdwDES0Sk1Z-NtJH5sGCnkKL8NMtFbSuMYjjEOQ46E6m2KudKbruC1zWy-y2QMdSs)

3.ตรวจสอบข้อมูลให้ถูกต้องแล้วกดปุ่ม Confirm ระบบจะพาไปที่หน้า Project แสดงให้เห็นสมาชิกที่เพิ่มขึ้นมา 2 คน โดย Email ที่ถูกเพิ่มมาใน Project แล้วจะมี Status เป็น Active ส่วน Email ที่ยังไม่ถูกเพิ่มมาจะมี Status เป็น Pending แต่เมื่อ Email นี้สมัครเข้ามาแล้วสถานะจะเปลี่ยนไปเป็น Pending Invite

![](https://lh6.googleusercontent.com/GjbYTXMEA-9DnbVjx6DEKzTlu6JJJ2cB9sUUyuQb56MLBV8pWoNgWF2MMJD9TOfiPh7h7Pd2kgbEI1FVxv_ksKdYgS49Ki4J_FfkPTWag0zx2JNvfgPJWcW-HS5opZMWMRrLdMs)

4.เมื่อ Status ของสมาชิกกลายเป็น **Pending invite** ให้กดที่ปุ่ม more แล้วเลือก **Confirm Invite** เพื่อเพิ่มเข้าเป็นสมาชิก Project ทันที

### **Change role**

การปรับเปลี่ยนสิทธิ์ของสมาชิก Project สามารถทำได้ดังนี้

1.กดปุ่ม more ที่สมาชิกที่ต้องการปรับเปลี่ยนสิทธิ์ แล้วเลือก Change role

![](https://lh5.googleusercontent.com/o3YXHHBlUyKey3EJhfjNULsJDAN3zLf6arQXiyfiPDDG0xhBIte04szLOVjd9wFXZSIWURLcjBmrKUdIaoLY1CHyb582ukg48W1CIZq9gxCrVqVC2f-RAu3ycl-XPpIzKgjfNlg)

2.เลือกประเภทที่ต้องการ โดยจะเลือกได้แค่ **Biller** และ **Member** ไม่สามารถให้สิทธิ์ Owner กับสมาชิกคนอื่นได้

![](https://lh3.googleusercontent.com/r-nFh7HYrAKJosDDkpkK7xyS_Q2q94aGVGk4lJ93Gr2x0I6sFO5bzNkDFEwhFqgvnJYzPC5QjgETNdHrJCsYfrd6PMxEW-_rnUYwNGBAiAXqz4jfsjGGrs8ApjvIXz9ETwsI2Gs)

3.ตรวจสอบข้อมูลที่เลือกให้ถูกต้อง แล้วกดปุ่ม Confirm หลังจากนั้น ระบบจะพาไปที่หน้า Project พร้อมแสดงสิทธิ์ที่เปลี่ยนไป

![](https://lh5.googleusercontent.com/xIvotRuOsUX2ynnuiCiXM0qVGLPhV0W-q2zh2wste4RHzc-3wT04FSD10kuoJoZ5YgHhrQ0kAwX_p1j_rgnm5Q9U3CupI5uM2wP2NqPM11GTmnMcSV-sTKdxiL1pvM6VlIi3I0c)

### **Remove  member**

การลบสมาชิกออกจาก Project สามารถทำได้ทั้งกับสมาชิกที่มี status เป็น **active**, **pending** หรือ **pending invite** โดยมีขั้นตอนดังนี้

1.กดปุ่ม more ที่สมาชิกที่ต้องการปรับเปลี่ยนสิทธิ์ แล้วเลือก **Leave Project**

![](https://lh3.googleusercontent.com/TH_zorkt374TIe7Oz-_hkLRjb_je085ycF_PkuIJhkxtbwDoeva6eDOE3sWTONX7LGnEYRhi636bmsJqf_kzCLmciVe82ZpC7Q3O-PVXoOK0KIFsWIohQFMP5KCn7CC-eybeUMQ)

2.หน้าต่าง Confirm จะแสดงขึ้นมา ให้กด Confirm

![](https://lh4.googleusercontent.com/Cc4ls3MdUlxyN71yoG2IwH_IREbPhovs0bKBdL4h_TmwLJ-Knp1Hm_f_2Wq5xvMNFIcD77DSqA_gjHudLi2c5t_NdQrfo8KmCc9Qf-UHsXAKK3y3y_vmzZW7J2X5Co5MZroFPcY)

3.หลังจากนั้น ระบบจะพาไปที่หน้า Project พร้อมแสดงสมาชิกที่เปลี่ยนไป

![](https://lh6.googleusercontent.com/nPDUSUPPr1lMTHJgU3rvfSYzbRKeKGwJCbDiLkyAg2GfqlZaI5qHtLSOfK1fRVzqqZl2Bto59uFmMF2wMSQa1XP2Kh0l7EaTjbN6TM9BrlHphGGlfnA9br1areLa_sfu4Hnp3sA)

## **Edit contact**

Owner สามารถแก้ไขเบอร์โทรศัพท์ และ Email ที่ใช้ในการติดต่อสื่อสารได้ตลอดเวลา โดยมีขั้นตอนดังต่อไปนี้

1.ที่หน้า Project กดปุ่ม ![](https://lh4.googleusercontent.com/BGDpH1xsHB8jagbpYjHNDLcA-zRKNmFIcN0gJUylm0e9cYQSbPsLqWHDvdmkh6BQOeA5NP0zKJ2bQCEwWsnhZIsME9JPiw04KPs9zzZFtumkRlqirfqt_IJS0x_NXNvXSJ49mdQ)

![](https://lh3.googleusercontent.com/dgOHDivc8MUr6tHeLBM-hmkTo26Ns8Cps2wzCPgLVD3KWZsZCmDejFzHpXRhBeFiTK7DCJPxCGOlUVnpQb6psmOWWHSeEGelY0FbnPkyd5GdD_RNGrB1r8t9LuWHI7ZKuw_tIPc)

แก้ไขเบอร์โทรศัพท์ หรือ เพิ่ม-ลด Email ได้ดังต่อไปนี้

* **Phone number:** เบอร์โทรศัพท์ที่ Admin ของเราจะใช้ในการติดต่อเมื่อเกิดปัญหากับ Project ของคุณ
* **Contact email\(s\):** \(Maximum email input limit 10\) Email ที่ใช้ในการแจ้งข่าวสารต่างๆ โดยจะมี Email ของสมาชิก Project เป็นค่าพื้นฐาน และสามารถเพิ่ม Email อื่นๆได้อีกไม่เกิน 10 Email 

![](https://lh3.googleusercontent.com/gh3F7VtMjSiD4o1p4-HguGK6PfHaUAkjzumxOyZSDjlTeWBDthhMJ5yqQ-q0wmeoI0FoGGiC3c2QjuEIn2bmXVUSSFuiLTNBL8pnX8CV1kA-DT_LwE5vpj3X9Yp_cOoypw2_Rl0)

2.ตรวจสอบข้อมูลที่ใส่ให้ถูกต้อง แล้วกดปุ่ม Confirm หลังจากนั้น ระบบจะพาไปที่หน้า Project พร้อมแสดงข้อมูลที่เปลี่ยนไป

![](https://lh3.googleusercontent.com/s7ycYQSttglgsEKHEjht0dLgkQH5pVj6NUX1znFDnGdt-9aloJWdmbxTDKNE1YVPY6SQuAaV4JWMTVoI7AJsWpLk4g8NJ7v00W4npjmtoZNB4FNk6Kx5gSg5pOjS3F7bpvs4J28)

## **Change Project & billing types**

{% hint style="info" %}
โดยพื้นฐานทุก ๆ Project จะเป็นประเภท **Individual** แต่ Owner สามารถส่งคำร้องขอเปลี่ยนเป็นประเภท **Company** ได้
{% endhint %}

รวมถึงรูปแบบการชำระเงินที่มีค่าพื้นฐานเป็น Prepaid หรือการเติมเงินไปก่อน จึงจะใช้ได้ แต่ **Owner** สามารถส่งคำร้องขอเปลี่ยนเป็นแบบ postpaid หรือการใช้งานไปก่อน แล้วค่อยออกบิลไปเก็บเงินได้ แต่จะต้องผ่านการพิจารณาจากทีมงานของ NCP ก่อน

### **Change Project type**

การส่งคำร้องขอเปลี่ยน Project type มีขั้นตอนดังต่อไปนี้  
1.ที่หน้า Project กดปุ่ม ![](https://lh6.googleusercontent.com/4wPOJQ1dmlL0UV2bBwlKJ27A0WYz4qeLIE89dvZUyya3OXIXPjqpxvm2S1y2DUy1qiQ8B8ZNluuHPAhaujtwzC8rIYL6LhZuBOWU_99KBKrXv7rBJs_swhKoeet9HzE4CzABhMw) และเลือก **Change Project Type**

![](https://lh3.googleusercontent.com/xOpe78pZd19311ctXSXTwFFqb2qrJKcBoZA-EmMT4M9stRxDbbO148y8pAldZpSq0fzDhPUCBAgrhxJ8oIroAUphe7xEGr12h7YGwUKlXTEyAq410pWYiuUe5PE-9J0MA1pkdfY)

ที่หน้า **"Request for change Project type"** ให้ใส่ข้อมูลดังต่อไปนี้

* **Contact name:** ใส่ชื่อที่ใช้ในการติดต่อกับทีมงานของ NCP
* **Tax ID:** เลขผู้เสียภาษีของบริษัท
* **Name:** ชื่อของบริษัท
* **Phone:** เบอร์โทรศัพท์ของบริษัท ที่สามารถติดต่อได้
* **Address:** ที่อยู่ของบริษัท
* **Attachment:** แนบเอกสารจดทะเบียนบริษัท

![](https://lh6.googleusercontent.com/3M3oLzkNbTU63xLYy7shTn3a6_Ny2sWWE2_8C-UMvycHqBQMKgeA3BYBkmbqotNZoTjphjvOWFbtfz1LaUzXB2Zjo9kv4jlBRcFoHflOeFrrfuP2wVqZ27qIlEbejkZPZGLhbwk)

ตรวจสอบข้อมูลให้ครบถ้วนถูกต้องแล้วกด Confirm ระบบจะพากลับไปที่หน้า Project จะเห็นว่าที่ Project type จะมี

* สัญลักษณ์ ![](https://lh6.googleusercontent.com/E-Jm9zYIaw6-0JqrF0smn8-FndUiHRnPuT9ay9HvVHKJ1RJtUgobS3v1yuRJHAAJl-mie_AByNkR662Q6DGqShkmKWNLTsA5tlJU8ayRFy4FtUxacNiOc-ljcYRgduxPf64PgQs)หมายถึงคำขอของคุณ กำลังรอการพิจารณาอยู่
* สัญลักษณ์ ![](https://lh5.googleusercontent.com/qZ9MuVbEFROtfS8sT67ffVoPFommvNtXm5SS_48mmR3ljs-sXg2_O__6lE0w4FlpVUftLMLp1sJxuJT22uFQ6VIpqG46BUquNCvkl-Ygtve7LHbNhcZl3V2nA1_zckhcmEFw7FY)หมายถึงคำขอของคุณ ได้รับการอนุมัติ

![](https://lh4.googleusercontent.com/nGD0k12z9DpmlCSgs0JEhkpFK7Yz071_-3dEQgYHmWTEVYfyEmde-7nFPO3GGgpYdsF9K9eTdOehMDRvRI9OqyqDPBbMxc-6YChr8C8N5IC3NagFMIsKE9xvnj728y3hppyHIHY)

### **Change billing type**

การส่งคำร้องขอเปลี่ยนการคิดเงิน มีขั้นตอนดังต่อไปนี้

1.ที่หน้า Project กดปุ่ม ![](https://lh6.googleusercontent.com/4wPOJQ1dmlL0UV2bBwlKJ27A0WYz4qeLIE89dvZUyya3OXIXPjqpxvm2S1y2DUy1qiQ8B8ZNluuHPAhaujtwzC8rIYL6LhZuBOWU_99KBKrXv7rBJs_swhKoeet9HzE4CzABhMw) และเลือก **Change Billing Type**

![](https://lh6.googleusercontent.com/zDv5fvoneR5SR8uf2oQrm6pa05Prk6mdnkwM1yqI6Fg9z8TNFa0jj88C1j6iHHr1cLGKZ8v-yThbOxGRJXVK6kYj6PsKBVhObK50uyXXnI_MTmEk1axGtPMdW-Z2XuIsqi_Fq4s)

ที่หน้า **"Request for change billing type"** ให้ใส่ข้อมูลดังต่อไปนี้

* **Contact name:** ใส่ชื่อที่ใช้ในการติดต่อกับทีมงานของ NCP
* **Type:** ชนิดของการคิดเงิน โดยปัจจุบันจะมีให้เลือกเพียง Postpaid

![](https://lh3.googleusercontent.com/hlR62SXmHK-5VZK0-CS-oz29QChjc1T5xSJOeeqmB-PWqe1pJVHW8ntfplAlOXJFdHjRWiEgrmMDLtAJjojX7pjxOsbXhQ-SwxYDILPC3pKqwBISq3pOGEkT4Lov0E9s_-luyIg)

2.ตรวจสอบข้อมูลให้ครบถ้วนถูกต้องแล้วกด Confirm ระบบจะพากลับไปที่หน้า Project จะเห็นว่าที่ Billing type จะมีสัญลักษณ์ ![](https://lh6.googleusercontent.com/E-Jm9zYIaw6-0JqrF0smn8-FndUiHRnPuT9ay9HvVHKJ1RJtUgobS3v1yuRJHAAJl-mie_AByNkR662Q6DGqShkmKWNLTsA5tlJU8ayRFy4FtUxacNiOc-ljcYRgduxPf64PgQs)อยู่ ซึ่งหมายถึงคำขอของคุณกำลังรอการพิจารณาอยู่ และจะเปลี่ยนเป็น ![](https://lh5.googleusercontent.com/qZ9MuVbEFROtfS8sT67ffVoPFommvNtXm5SS_48mmR3ljs-sXg2_O__6lE0w4FlpVUftLMLp1sJxuJT22uFQ6VIpqG46BUquNCvkl-Ygtve7LHbNhcZl3V2nA1_zckhcmEFw7FY)เมื่อได้รับการอนุมัติ

![](https://lh6.googleusercontent.com/mxEPya_NZYoYiAdw0F_5H_emfhKv32zMlrcOmkLo4Wu_GPmntB3kvNtvT0lPlL9lfSKpexuvTtBGAf_lNcA-IWIA0QuhZ8YVhFhwOIfWliD4aYJ476z7tc-GZoIl7XigwaIFh4c)

## Remove Project

เมื่อคุณไม่ต้องการ Project แล้ว ก็สามารถลบ Project ออก เพื่อไม่ให้เหลือ resource เก่าไว้ได้ โดยมีขั้นตอนดังต่อไปนี้  
1.ที่หน้า Project กดปุ่ม ![](https://lh6.googleusercontent.com/4wPOJQ1dmlL0UV2bBwlKJ27A0WYz4qeLIE89dvZUyya3OXIXPjqpxvm2S1y2DUy1qiQ8B8ZNluuHPAhaujtwzC8rIYL6LhZuBOWU_99KBKrXv7rBJs_swhKoeet9HzE4CzABhMw) และเลือก **Delete Project**

![](https://lh4.googleusercontent.com/peo36_dBOKRc040R3ZIFUTpq2ljnRc4b_cMtXAmHQ5GfX_tiSixG3J6uGC3qYiN6lA-jPvuYBc1Eki39eT7hsf3woWi3J8iaL0okRy-d9mfZXWMy7AqMBSIYwwhZs3MCYwCzGqE)

2.หน้าต่าง Confirm จะแสดงข้อความบอกว่า หากลบ Project นี้ไปแล้ว จะไม่สามารถเข้าถึง Resource ต่างๆได้ แต่จะยังสามารถกู้คืนได้ภายใน 7 วัน ถ้ายอมรับเงื่อนไข ให้กด Confirm

![](https://lh5.googleusercontent.com/QGEA-lh8g6aWR3Sgdu6vAR0dSTf8ksmoZK-rU6ksh96H29VQqMGLgixlsZCCSjopBEfe8kBvteY8_7j-MNYIWolF_m_DhU_rK4DtTaDJP3JmjIPZk76CyTIrPyixejkQBIhJbXg)

3.ระบบจะพามาที่หน้า **Restored Project** ที่จะมีเวลาบอกว่า Project จะถูกลบถาวรภายในวันไหน

![](https://lh5.googleusercontent.com/KOG-EOV_ZRErBvwKHz-IKKLAQQVMUFxXWrBCu4cTRd-AZw4Ld_KOfFcFiBZ0HF5illgDr7p6SKYbLMq6wtl-UPwlX2Hzkgh3KoA8SusKTZJ_8rJ5MDj4arXNPP5kWxev0Pw145s)

4.หากต้องการกู้ Project คืน ให้กดที่ปุ่ม ![](https://lh5.googleusercontent.com/yELXqK_Wbl6pv1AtjFKtSvCovnLRTip4Ug2x2psO0VHRULJ0783dwZB8Yfh8KUb1NPWXPKznEFsAYK9JHlqja9rxtGk4WtVZaGMDHCoWyTYB7K05t5gsq-TgBhJmuFjvi3H7PZQ)แล้วระบบจะพากลับไปที่หน้า Project และสามารถกลับไปใช้งานได้ทันที

![](https://lh6.googleusercontent.com/X-ZkXLwNwSjv-EucZRKmlHvYDDKmjLXUECmmjsZKTo0JGeAStCxKalU34eVcMDKtkFSRAZHu0yE7p-rML26CLCOmPNLdvdMRuN5uE6qAsn0ULJEon4Q03u9sf_dfBfcUURv73ws)

