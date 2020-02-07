# Launch Instance

ในการสร้าง instance ควรทำความเข้าใจถึงข้อมูลต่างๆที่ใช้ในการสร้าง instance ก่อน ดังนี้

> **Hostname** ชื่อของ instance  
> **Image** ระบบปฏิบัติการ \(Operating System\) ของ instance  
> **Machine Type** spec ของ instance  
> **Cloud firewall** ส่วนที่ระบุการเข้าถึงการใช้งาน instance  
> **Authentication** ส่วนระบุตัวตนในการใช้งาน instance  
> **How many instance ?** จำนวน instance ที่ต้องการสร้าง  
> **External IP** ส่วนที่ระบุ IP Address ของ instance ที่ต้องการเชื่อมต่อกับ network ภายนอก  
> **Auto backup** ส่วนที่ระบุถึงการให้ระบบจัดการเก็บข้อมูล backup instance โดยอัตโนมัติ  
> **Instance Volume** _**\(optional\)**_ ****ขนาดของ volume \(สามารถระบุได้ กรณีที่สร้างแบบ Boot volume\)  
> **Network** _**\(optional\)**_ ส่วนที่ระบุ network ที่ต้องการใช้งาน instance โดยสามารถกำหนด IP Address ได้



1. กรอก **Hostname** \(ชื่อ Instance\) ที่ต้องการ \(ภายในช่องกรอกระบบจะมีชื่อ default ให้ โดยทางผู้ใช้งานสามารถตั้งชื่อใหม่ได้\)
2. เลือก **Image** ที่ต้องการสร้าง โดย image จะประกอบไปด้วย 4 ประภท ดังนี้  **** _Distributions_: image หลักของระบบ เช่น Ubuntu, Windows, Centos เป็นต้น   _Marketplace:  image ที่มี template สำเร็จรูป โดยเมื่อผู้ใช้งานสร้าง จะสร้างมานำไปใช้งานได้เลย ไม่ต้องติดตั้งเพิ่มเติม เช่น Docker, GitLab, Wordpress เป็นต้น_

