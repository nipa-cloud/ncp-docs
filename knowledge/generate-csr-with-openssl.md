# วิธี GENERATE ไฟล์ CSR ด้วย OPENSSL

## วิธี GENERATE ไฟล์ CSR ด้วย OPENSSL

1.Login เข้า Server ผ่านทาง ssh 2.สร้าง CSR และ Private Key ด้วย Command line ดังนี้

```text
openssl req -new -newkey rsa:2048 -nodes -keyout server.key -out server.csr
```

> Note: เปลี่ยน “server” เป็นชื่อ Domain ของท่าน.

1. โปรแกรมจะถามรายละเอียดของ CSR ดังนี้
   * Country: รหัสย่ออย่างเป็นทางการของประเทศ 2 ตัวอักษรพิมพ์ใหญ่ ของประเทศไทยคือ TH
   * State or Province:  ชื่อจังหวัดที่ตั้งอยู่ขององค์กร เช่น Bangkok
   * City or Locality:  ชื่อเมืองที่ตั้งอยู่ขององค์กร เช่น Bangrak
   * Organization Name: ชื่อเต็มองค์กร \(ชื่อบริษัท\) เช่น NIPA Technology Co.,Ltd.
   * Organization Unit \(OU\):  ชื่อหน่วยงานเช่น ‘Information Technology’ หรือ เว้นว่างไว้
   * Common Name: ชื่อ Domain ที่ต้องการใช้งาน certificate เช่น www.nipa.cloud
   * A challenge password: เว้นว่าง

> Note: ไม่จำเป็นต้องใส่รหัสผ่าน เนื่องจากถ้ามีการใส่ไว้เวลามีการ Restart Web Server จะมีการสอบถามรหัสผ่านนี้ทุกครั้งถ้าไม่กรอกรหัสผ่านที่ตั้งไว้นี้หรือลืมรหัสผ่าน Web Service จะไม่สามารถใช้งานได้ และในกรณีลืมรหัสผ่านต้องทำการ Generate Certificate ใหม่

