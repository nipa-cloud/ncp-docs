# Allow MySQL Connection on On-Premise

Note: ควรทำด้วยความระมัดระวังและไม่ควรใช้รหัสที่สั้น/ไม่ปลอดภัย โดยเฉพาะ Dictionary Password และควรหมั่นเปลี่ยน Password ทุกๆ3เดือน

## Requirement

```text
ได้ Allow Cloud Firewall port 3306 ไว้แล้ว
```

## step

1.Login ด้วย User Root

2.ตรวจสอบดูว่า MySQL Listen ที่ Interface ใด

```text
# netstat -lntp |grep 3306
tcp 0 0 127.0.0.1:3306 0.0.0.0:* LISTEN 3442/mysqld
```

3.\(optional\) หากเป็น 127.0.0.1 จะแสดงว่า Listen ที่ Interface loopback ต้องทำการเปลี่ยนเพื่อให้รับ Connection จาก Interface ของ Internet ได้

แก้ไขไฟล์/etc/mysql/mysql.conf.d/mysqld.cnf

```text
[mysqld]
bind-address = 127.0.0.1
```

เป็น

```text
[mysqld]
bind-address = 0.0.0.0
```

แล้ว restart service mysql เพื่อให้เปลี่ยนค่าใหม่  
systemctl restart mysql  
ควรได้ค่า listen เป็นดังนี้

```text
# netstat -lntp |grep 3306
tcp 0 0 0.0.0.0:3306 0.0.0.0:* LISTEN 4489/mysqld
```

4.Login เข้า MySQL

```text
mysql -u root
use mysql;
```

5.ตรวจสอบสิทธิ์ปัจจุบันว่าเคยมีสร้างไว้แล้วหรือไม่

```text
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

6.Grant สิทธิ์ Login

* หากต้องการ ให้สิทธิ์ Login จาก IP ภายนอก IP ใดๆก็ตาม ให้ใช้คำสั่งดังนี้

  ```text
  create user 'root'@'%' identified by 'H@rdSecretP@ssw0rd';
  grant all privileges on *.* to 'root'@'%' with grant option;
  ```

โดย H@rdSecretP@ssword คือรหัสที่ต้องการใช้สำหรับ login

* หากต้องการให้สิทธิ์ login จาก IP ภายนอก เฉพาะ IP ให้ใช้คำสั่งดังนี้

  ```text
  create user 'root'@'103.212.37.6' identified by 'H@rdSecretP@ssw0rd';
  grant all privileges on *.* to 'root'@'103.212.37.6' with grant option;
  ```

โดย 103.212.37.6 เป็น Public IP address ฝั่ง On-premise ที่ต้องการใช้ connect

7.Flush privileged เพื่อให้ค่าที่ set ไป effect ทันที

```text
flush privileges;
```

