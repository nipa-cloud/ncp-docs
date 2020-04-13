# Cloud Firewall Rules for Ad Server

Firewall Rule ที่ AD Server จำเป็นต้องเปิด เพื่อให้เครื่องอื่นๆสามารถ Connect มาได้ มีดังนี้

```text
TCP port – 88, 135, 139, 389, 445, 49152-65535

UDP port – 53, 123, 137, 138, 389, 49152-65535
```

> Recommend ให้สร้าง cloud firewall ขึ้นมาตัวหนึ่งชื่อ Client Domain เพื่อ Attach ให้กับเครื่องอื่นๆที่จะ Join Domain

สร้าง cloud firewall อีกตัวหนึ่งขึ้นมาชื่อ Domain Controller เพื่อ attach ให้กับ Domain Controller  
โดยใน Domain Controller ให้ Add Ingress ซึ่งมี Port ตามข้างต้น และมี Remote มาจาก Client Domain

