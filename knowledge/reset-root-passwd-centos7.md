# Knowledge

## วิธีการ RESET ROOT PASSWORD บน CENTOS7

> Note: ควรทำการ snapshot ก่อนการแก้ไข เนื่องจากหากมีการแก้ไขผิดพลาดจากขั้นตอนที่ระบุไว้ตามเอกสาร อาจทำให้ระบบพังและไม่สามารถ boot ได้อีก

1.Access เข้า Console ของเครื่อง และ reboot เครื่องด้วย Ctrl-Alt-Del   
![](../.gitbook/assets/k_reset_password_centos7_001.png)

2.เมื่อเครื่อง reboot ขึ้นมา ให้กด e เพื่อ edit (บรรทัดที่ไม่ใช่ rescue)   
![](../.gitbook/assets/k_reset_password_centos7_002.png)

3.แก้ไข บรรทัด Linux16 แก้ไขให้เป็น   
```rw init=/bin/bash```   
จากเดิม   
![](../.gitbook/assets/k_reset_password_centos7_003.png)
แก้ไขเป็น
![](../.gitbook/assets/k_reset_password_centos7_004.png)

4.กด Ctrl-x เพื่อ boot จาก config ที่แก้ไข เมื่อ boot เสร็จจะเข้า single user mode ดังภาพ
![](../.gitbook/assets/k_reset_password_centos7_005.png)

5.ตรวจสอบว่า vda ถูก mount บน / และมีสถานะเป็น rw
![](../.gitbook/assets/k_reset_password_centos7_006.png)

6.ใช้ command passwd เพื่อ set password ให้กับ user root   
และ touch /.autorelabel เพื่อให้เกิดการ relabel ของ SELinux เมื่อ boot
![](../.gitbook/assets/k_reset_password_centos7_007.png)

7.reboot ด้วย command ดังนี้   
```exec /sbin/init```


8.ทดสอบ login ด้วย password ใหม่
![](../.gitbook/assets/k_reset_password_centos7_008.png)