# How to generate new vpn user and revoke vpn user

**วิธีการสร้าง VPN user ใหม่** 

1. เข้าไปที่ path ~/openvpn-ca

```text
cd ~/openvpn-ca
```

2. source เพื่อใช้สิทธิ์ในการใช้คำสั่งสร้าง vpn user

```text
source vars
```

3. สร้าง key สำหรับผู้ใช้งานใหม่โดยคำสั่ง \(ex. ชื่อผู้ใช้งานใหม่ชื่อ client1\)

```text
./build-key client1
```

หลัง run คำสั่งข้างต้นจะมีข้อความให้ตั้ง config ต่างๆให้ กด Enter ไปเรื่อยๆจนเจอคำถามที่ให้ตอบเป็น \(yes/no\) และให้ตอบ yes ทั้งหมด

4. โดยจากคำสั่ง ./build-key จะทำการสร้าง Certificate และ Key สำหรับ user นั้นซึ่งต่อไปจะต้องทำการสร้าง config ให้กับ user ดังกล่าวโดยเข้าไปที่ path /client-configs และใช้คำสั่งในการ run script ชื่อ make\_config.sh ตามด้วยชื่อ user

```text
cd ~/client-configs

./make_config.sh client1
```

5. เข้าไปที่ path /client-configs/files และจะเห็นชื่อ user ที่เพิ่งสร้างตามด้วยสกุลไฟล์ ovpn

```text
cd ~/client-configs/files
```

5.1 cat &lt;client1&gt;.ovpn แล้ว copy ข้อความในไฟล์ ovpn ทั้งหมดไป paste ไว้ที่ไฟล์ .txt ธรรมดาในเครื่องที่จะต้องการใช้งาน vpn และเปลี่ยนสกุลไฟล์เป็น .ovpn เพื่อใช้งาน  
example: client1.txt &gt;&gt; client1.ovpn

```text
cat client1.ovpn
```

โดยการ cat client1.ovpn จะแสดงข้อความในไฟล์ ovpn ซึ่งมีความยาวพอสมควรและควร copy ให้ครบถ้วน

หลังจาก copy ข้อความในไฟล์ opvn มาที่ไฟล์สกุล .txt และเปลี่ยนสกุลไฟล์เป็น ovpn จะสามารถใช้งาน vpn user นั้นได้โดยไปที่ folder ที่มีไฟล์ opvn ของ user นั้นอยู่และตามด้วยคำสั่งใช้งาน vpn ตามด้วยชื่อ user

```text
cd ~/<path-to-openvpn-file>

sudo openvpn <client1>.ovpn
```

**วิธีการถอน access ของ vpn user**

1. เข้าไปที่ path ~/openvpn-ca

```text
cd ~/openvpn-ca
```

2. source เพื่อใช้สิทธิ์ในการใช้คำสั่งสร้าง vpn user

```text
source vars
```

3. เรียกใช้คำสั่ง revoke-full และตามด้วยชื่อของ user ที่ต้องการจะถอน access

```text
./revoke-full client1
```

โดย output ของคำสั่ง revoke-full จะแสดง error 23 ซึ่งถือว่าปกติโดยคำสั่ง revoke-full จะทำการสร้างข้อมูลการถอน access ของ user นั้นและเก็บไว้ที่ ไฟล์ชื่อว่า crl.pem ใน folder ชื่อ keys

4. Copy ไฟล์ crl.pem ไปที่ configuration directory ของ openvpn โดยคำสั่ง

```text
sudo cp ~/openvpn-ca/keys/crl.pem /etc/openvpn
```

5. เปิดไฟล์ config ของ OpenVPN server โดย

```text
sudo nano /etc/openvpn/server.conf
```

6. ใส่ข้อความ crl-verify ไปที่ด้านล่างสุดของไฟล์ server.conf เพื่อที่ OpenVPN server จะทำการเช็คข้อมูลการถอน access ของ user ดังกล่าว \( หากพบว่ามีการใส่ข้อความ crl-verify crl.pem อยู่แล้วให้ข้ามไปข้อ 7.\)

```text
crl-verify crl.pem
```

7. ทำการ restart OpenVPN Service เพื่อให้ OpenVPN ดำเนินการ certificate revocation

```text
service openvpn restart
```



