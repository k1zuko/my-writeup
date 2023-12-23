![[Challenge BabyEncryption.png]]
```bash
unzip BabyEncryption.zip
	Archive:  BabyEncryption.zip
	[BabyEncryption.zip] chall.py password: 
	  inflating: chall.py                
	  inflating: msg.enc 

cat chall.py
	import string
	from secret import MSG
	
	def encryption(msg):
	    ct = []
	    for char in msg:
	        ct.append((123 * char + 18) % 256)
	    return bytes(ct)
	
	ct = encryption(MSG)
	f = open('./msg.enc','w')
	f.write(ct.hex())
	f.close()

cat msg.enc
	6e0a9372ec49a3f6930ed8723f9df6f6720ed8d89dc4937222ec7214d89d1e0e352ce0aa6ec82bf622227bb70e7fb7352249b7d893c493d8539dec8fb7935d490e7f9d22ec89b7a322ec8fd80e7f8921

nano chall.py
	def decryption(msg):
		pt = []
		for char in msg:
			char = char - 18
			char = 179 * char % 256
			pt.append(char)
		return bytes(pt)
	
	with open("msg.enc") as f:
		ct = bytes.fromhex(f.read())
	
	pt = decryption(ct)
	print(pt)

python chall.py
	b'Th3 nucl34r w1ll 4rr1v3 0n fr1d4y.\nHTB{l00k_47_y0u_r3v3rs1ng_3qu4710n5_c0ngr475}'
```