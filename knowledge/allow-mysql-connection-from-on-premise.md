# Knowledge

## ALLOW MYSQL CONNECTION FROM ON-PREMISE

> Note: ควรทำด้วยความระมัดระวังและไม่ควรใช้รหัสที่สั้น/ไม่ปลอดภัย โดยเฉพาะ Dictionary password และควรหมั่นเปลี่ยน password ทุกๆ3เดือน

### Requirement
    ได้ Allow Cloud Firewall port 3306 ไว้แล้ว

### step
1.login ด้วย user root

2.ตรวจสอบดูว่า MySQL listen ที่ interface ใด
```
# netstat -lntp |grep 3306
tcp 0 0 127.0.0.1:3306 0.0.0.0:* LISTEN 3442/mysqld
```
3.(optional) หากเป็น 127.0.0.1 จะแสดงว่า listen ที่ interface loopback ต้องทำการเปลี่ยนเพื่อให้รับ connection จาก interface ของ internet ได้

แก้ไขไฟล์/etc/mysql/mysql.conf.d/mysqld.cnf
```
[mysqld]
bind-address = 127.0.0.1
```
เป็น
```
[mysqld]
bind-address = 0.0.0.0
```

แล้ว restart service mysql เพื่อให้เปลี่ยนค่าใหม่   
systemctl restart mysql   
ควรได้ค่า listen เป็นดังนี้
```
# netstat -lntp |grep 3306
tcp 0 0 0.0.0.0:3306 0.0.0.0:* LISTEN 4489/mysqld
```

4.login เข้า MySQL
```
mysql -u root
use mysql;
```

5.ตรวจสอบสิทธิ์ปัจจุบันว่าเคยมีสร้างไว้แล้วหรือไม่
```
select Host,User from user;
+———–+——————+
| Host | User |
+———–+——————+
| localhost | debian-sys-maint |
| localhost | mysql.session |
| localhost | mysql.sys |
| localhost | root |
| localhost | wordpress |
+———–+——————+
5 rows in set (0.00 sec)
```

6.Grant สิทธิ์ login

  * หากต้องการ ให้สิทธิ์ login จาก IP ภายนอก IP ใดๆก็ตาม ให้ใช้คำสั่งดังนี้
```
create user ‘root’@’%’ identified by ‘H@rdSecretP@ssw0rd’;
grant all privileges on *.* to ‘root’@’%’ with grant option;
```
โดย H@rdSecretP@ssword คือรหัสที่ต้องการใช้สำหรับ login

   * หากต้องการให้สิทธิ์ login จาก IP ภายนอก เฉพาะ IP ให้ใช้คำสั่งดังนี้
```
create user ‘root’@’103.212.37.6’ identified by ‘H@rdSecretP@ssw0rd’;
grant all privileges on *.* to ‘root’@’103.212.37.6’ with grant option;
```

โดย 103.212.37.6 เป็น Public IP address ฝั่ง On-premise ที่ต้องการใช้ connect

7.Flush priviledge เพื่อให้ค่าที่ set ไป effect ทันที
```
flush privileges;
```