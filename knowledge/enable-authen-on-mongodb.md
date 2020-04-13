# HOW TO ENABLE AUTHENTICATION ON MONGODB

## HOW TO ENABLE AUTHENTICATION ON MONGODB

เนื่องจากโดย default แล้ว MongoDB จะไม่มีการ enable authentication มาให้ตั้งแต่แรก ส่งผลให้เมื่อ connect MongoDB แล้ว จะมีสิทธิ์ admin ในทันที ซึ่งกระทบต่อ security ของระบบ ดังนั้นจึงควร enable authentication ขึ้นมา เมื่อต้องการเปิด connection จากภายนอกเข้าสู่ mongoDB

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
db.createUser(
{
user: “myadmin”,
pwd: “AdminP@ssw0rd”,
roles: [ { role: “userAdminAnyDatabase”, db: “admin” } ]
}
)
```

4.แก้ไขไฟล์ /etc/mongod.conf เพิ่มบรรทัด

```text
security:
authorization: enabled
```

5.restart service

```text
systemctl restart mongod
```

6.ทดสอบใช้งาน

```text
mongo
show dbs
```

จะต้องแสดง error message ว่า

```text
Error: listDatabases failed:{
“ok” : 0,
“errmsg” : “not authorized on admin to execute command { listDatabases: 1.0, $db: \”admin\” }”,
“code” : 13,
“codeName” : “Unauthorized”
```

7.เมื่อใช้งาน ให้ login ด้วย command ดังนี้

```text
db.auth(“myadmin”, “AdminP@ssw0rd”)
```

> Reference  
> [https://docs.mongodb.com/v3.2/tutorial/enable-authentication/](https://docs.mongodb.com/v3.2/tutorial/enable-authentication/) [https://www.blognone.com/node/88956](https://www.blognone.com/node/88956)

