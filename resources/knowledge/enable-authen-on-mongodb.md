# Enable MongoDB Authentication

เนื่องจากโดย Default แล้ว MongoDB จะไม่มีการ Enable Authentication มาให้ตั้งแต่แรก ส่งผลให้เมื่อ Connect MongoDB แล้ว จะมีสิทธิ์ Admin ในทันที ซึ่งกระทบต่อ Security ของระบบ ดังนั้นจึงควร Enable Authentication ขึ้นมา เมื่อต้องการเปิด connection จากภายนอกเข้าสู่ MongoDB

ขั้นตอนการ enable authentication สามารถทำได้ดังนี้

1.connect เข้าไปยัง MongoDB

```text
mongo
```

2.เปลี่ยนไปใช้ database admin

```text
use admin
```

3.เปลี่ยนไปใช้ database admin

```text
db.createUser({
    user: “myadmin”,
    pwd: “AdminP@ssw0rd”,
    roles: [ { role: “userAdminAnyDatabase”, db: “admin” } ]
})
```

4.แก้ไขไฟล์ /etc/mongod.conf เพิ่มบรรทัด

```text
security:
authorization: enabled
```

5.Restart Service

```text
systemctl restart mongod
```

6.ทดสอบใช้งาน

```text
mongo
show dbs
```

จะต้องแสดง Error Message ว่า

```text
Error: listDatabases failed:{
“ok” : 0,
“errmsg” : “not authorized on admin to execute command { listDatabases: 1.0, $db: \”admin\” }”,
“code” : 13,
“codeName” : “Unauthorized”
```

7.เมื่อใช้งาน ให้ Login ด้วย Command ดังนี้

```text
db.auth(“myadmin”, “AdminP@ssw0rd”)
```

> Reference  
> [https://docs.mongodb.com/v3.2/tutorial/enable-authentication/](https://docs.mongodb.com/v3.2/tutorial/enable-authentication/) [https://www.blognone.com/node/88956](https://www.blognone.com/node/88956)

