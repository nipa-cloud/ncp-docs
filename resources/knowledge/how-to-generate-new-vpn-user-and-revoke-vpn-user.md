# How To Generate And revoke VPN User

**วิธีการสร้าง VPN User ใหม่** 

1. เข้าไปที่ Path ~/openvpn-ca

```text
cd ~/openvpn-ca
```

2. source เพื่อใช้สิทธิ์ในการใช้คำสั่งสร้าง VPN User

```text
source vars
```

3. สร้าง Key สำหรับผู้ใช้งานใหม่โดยคำสั่ง \(ex. ชื่อผู้ใช้งานใหม่ชื่อ client1\)

```text
./build-key client1
```

หลัง Run คำสั่งข้างต้นจะมีข้อความให้ตั้ง config ต่างๆให้ กด Enter ไปเรื่อยๆจนเจอคำถามที่ให้ตอบเป็น \(yes/no\) และให้ตอบ yes ทั้งหมด

4. โดยจากคำสั่ง ./build-key จะทำการสร้าง Certificate และ Key สำหรับ user นั้นซึ่งต่อไปจะต้องทำการสร้าง Config ให้กับ User ดังกล่าวโดยเข้าไปที่ Path /client-configs และใช้คำสั่งในการ Run Script ชื่อ make\_config.sh ตามด้วยชื่อ User

```text
cd ~/client-configs

./make_config.sh client1
```

5. เข้าไปที่ Path /client-configs/files และจะเห็นชื่อ User ที่เพิ่งสร้างตามด้วยสกุลไฟล์ .ovpn

```text
cd ~/client-configs/files
```

5.1 cat &lt;client1&gt;.ovpn แล้ว copy ข้อความในไฟล์ ovpn ทั้งหมดไป paste ไว้ที่ไฟล์ .txt ธรรมดาในเครื่องที่จะต้องการใช้งาน VPN และเปลี่ยนสกุลไฟล์เป็น .ovpn เพื่อใช้งาน  
Example: client1.txt &gt;&gt; client1.ovpn

```text
cat client1.ovpn
```

โดยการ cat client1.ovpn จะแสดงข้อความในไฟล์ .ovpn ซึ่งมีความยาวพอสมควรและควร Copy ให้ครบถ้วน

หลังจาก Copy ข้อความในไฟล์ .opvn มาที่ไฟล์สกุล .txt และเปลี่ยนสกุลไฟล์เป็น .ovpn จะสามารถใช้งาน VPN user นั้นได้โดยไปที่ folder ที่มีไฟล์ .opvn ของ User นั้นอยู่และตามด้วยคำสั่งใช้งาน VPN ตามด้วยชื่อ User

```text
cd ~/<path-to-openvpn-file>

sudo openvpn <client1>.ovpn
```

**วิธีการถอน Access ของ VPN User**

1. เข้าไปที่ Path ~/openvpn-ca

```text
cd ~/openvpn-ca
```

2. source เพื่อใช้สิทธิ์ในการใช้คำสั่งสร้าง VPN User

```text
source vars
```

3. เรียกใช้คำสั่ง revoke-full และตามด้วยชื่อของ User ที่ต้องการจะถอน Access

```text
./revoke-full client1
```

โดย Output ของคำสั่ง revoke-full จะแสดง error 23 ซึ่งถือว่าปกติโดยคำสั่ง revoke-full จะทำการสร้างข้อมูลการถอน Access ของ User นั้นและเก็บไว้ที่ ไฟล์ชื่อว่า crl.pem ใน Folder ชื่อ Keys

4. Copy ไฟล์ crl.pem ไปที่ Configuration Directory ของ OpenVPN โดยคำสั่ง

```text
sudo cp ~/openvpn-ca/keys/crl.pem /etc/openvpn
```

5. เปิดไฟล์ Config ของ OpenVPN server โดย

```text
sudo nano /etc/openvpn/server.conf
```

6. ใส่ข้อความ crl-verify ไปที่ด้านล่างสุดของไฟล์ server.conf เพื่อที่ OpenVPN Server จะทำการเช็คข้อมูลการถอน Access ของ User ดังกล่าว \( หากพบว่ามีการใส่ข้อความ crl-verify crl.pem อยู่แล้วให้ข้ามไปข้อ 7.\)

```text
crl-verify crl.pem
```

7. ทำการ restart OpenVPN Service เพื่อให้ OpenVPN ดำเนินการ Certificate Revocation

```text
service openvpn restart
```

