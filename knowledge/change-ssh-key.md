# Change old SSH KEY

## Change old SSH KEY

วิธีการเปลี่ยน SSH key ที่ใช้ในการ login โดยที่ SSH key เดิมยังใช้งานได้

Use case: ต้องการเปลี่ยน ssh key เนื่องจาก เปลี่ยนผู้ดูแลระบบ key file เดิมยังสามารถใช้งาน login เข้าระบบได้ ไม่ต้องการทำ snapshot และ restore ใหม่

1.Generate ssh key file ใหม่ ด้วย command ssh-keygen หรือ ทำการสร้าง key ใหม่จากหน้า NIPA Cloud Portal หมวด keypair ![](../.gitbook/assets/k_replace_ssh_key_001.png) หากใช้การสร้าง key จาก ssh-keygen ควรนำ public key ที่ได้มา import เข้าระบบด้วย เพื่อใช้ในกับเครื่องที่จะสร้างใหม่หลังจากนี้

2.หากทำการสร้าง keypair จากหน้า portal จะต้องทำการ extract public key ออกมาจาก private key ที่ได้ ด้วย command ดังนี้  
`ssh-keygen -y -f newkey.pem > /tmp/newkey.pub`

3.ทำการ Replace authorized\_keys ด้วย command ดังนี้  
`cat newkey.pub |ssh -i oldkey.pem nc-user@<server ip address> “cat > ~/.ssh/authorized_keys”`

4.ทดสอบ ssh ด้วย key ใหม่  
`ssh -i newkey.pub nc-user@<server ip address>`

