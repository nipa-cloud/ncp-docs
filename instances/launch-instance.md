# Launch Instance

### ข้อมูลที่ใช้ในการสร้าง Instance

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

> _/ ส่วนที่เป็น optional ผู้ใช้งานสามารถ request ขอทาง Administrator เพื่อใช้งานเพิ่มเติมได้_

### ขั้นตอนการสร้าง Instance

1.กรอก Hostname \(ชื่อ Instance\) ที่ต้องการ \(ภายในช่องกรอกระบบจะมีชื่อ default ให้ โดยทางผู้ใช้งานสามารถตั้งชื่อใหม่ได้\)   

![](../.gitbook/assets/1.png)

2.เลือก **Image** ที่ต้องการสร้าง โดย image จะประกอบไปด้วย 4 ประภท ดังนี้

{% tabs %}
{% tab title="Distributions" %}
> Image พื้นฐานหลักของระบบ เช่น Ubuntu, Windows, Centos เป็นต้น

![](../.gitbook/assets/2.png)
{% endtab %}

{% tab title="Marketplace" %}
> _Image ที่มี template สำเร็จรูป โดยเมื่อผู้ใช้งานสร้างด้วย image ประเภทนี้ จะสามารถนำไปใช้งานได้เลย ไม่ต้องตั้งค่าใดๆเพิ่มเติม เช่น Docker, GitLab, Wordpress เป็นต้น_

![](../.gitbook/assets/3.png)
{% endtab %}

{% tab title="Images" %}
> Image ที่เกิดจากการ snapshot ของ instance ด้วยผู้ใช้งานเอง หรือการทำ auto backup ของระบบ

![](../.gitbook/assets/4.png)
{% endtab %}

{% tab title="Volumes \(Optional\)" %}
> Image ที่เกิดจากการสร้าง volume แบบ boot volume โดยในส่วนนี้ หากผู้ใช้งานต้องใช้ feature นี้  จะต้อง request ขอมายัง Administrator เพิ่มเปิดใช้งาน

![](../.gitbook/assets/5.png)
{% endtab %}
{% endtabs %}



