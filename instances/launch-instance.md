# Launch Instance

ในการสร้าง instance ควรทำความเข้าใจถึงข้อมูลต่างๆที่ใช้ในการสร้าง instance ก่อน ดังนี้

| **หัวข้อ** | **คำอธิบาย** | Optional |
| :--- | :--- | :---: |
| Hostname | ชื่อ instance |  |
| Image | ระบบปฏิบัติการ \(Operating System\) ของ instance |  |
| Machine Type | spec ของ instance |  |
| Cloud firewall | ส่วนที่ระบุการเข้าถึง instance |  |
| Authentication | ส่วนที่กำหนด keypair หรือ password ในการเข้าใช้งาน |  |
| How many instance | จำนวนที่ต้องการสร้าง |  |
| Instance Volume | ขนาดของ volume \(สามาถระบุได้ในกรณีที่สร้างแบบ boot volume\) | / |
| Network | ส่วนที่กำหนด network ที่ต้องการใช้งาน โดยสามารถกำหนด IP Address ที่ต้องการใช้งานได้ | / |
| External IP | ส่วนที่กำหนด IP Address ที่ใช้ในการเชื่อมต่อ instance กับ network ภายนอก |  |
| Auto Backup | ส่วนที่กำหนดถึงการให้ระบบจัดการเก็บข้อมูล backup instance โดยอัตโนมัติ |  |



1. กรอก **Hostname** \(ชื่อ Instance\) ที่ต้องการ \(ภายในช่องกรอกระบบจะมีชื่อ default ให้ โดยทางผู้ใช้งานสามารถตั้งชื่อใหม่ได้\)
2. เลือก **Image** ที่ต้องการสร้าง โดย image จะประกอบไปด้วย 4 ประภท ดังนี้  **** _Distributions_: image หลักของระบบ เช่น Ubuntu, Windows, Centos เป็นต้น   _Marketplace:  image ที่มี template สำเร็จรูป โดยเมื่อผู้ใช้งานสร้าง จะสร้างมานำไปใช้งานได้เลย ไม่ต้องติดตั้งเพิ่มเติม เช่น Docker, GitLab, Wordpress เป็นต้น_

