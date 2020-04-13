# RULE CLOUD FIREWALL FOR AD SERVER

## RULE CLOUD FIREWALL FOR AD SERVER

Rule firewall ที่ AD Server จำเป็นต้องเปิด เพื่อให้เครื่องอื่นๆสามารถ connect มาได้ มีดังนี้

```text
TCP port – 88, 135, 139, 389, 445, 49152-65535

UDP port – 53, 123, 137, 138, 389, 49152-65535
```

> Recommend ให้สร้าง cloud firewall ขึ้นมาตัวหนึ่งชื่อ clientdomain เพื่อ attach ให้กับเครื่องอื่นๆที่จะ join domain

สร้าง cloud firewall อีกตัวหนึ่งขึ้นมาชื่อ domaincontroller เพื่อ attach ให้กับ domain controller  
โดยใน domain controller ให้ add Ingress ซึ่งมี port ตามข้างต้น และมี remote มาจาก clientdomain

