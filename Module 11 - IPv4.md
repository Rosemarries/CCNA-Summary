#CCNA 

### IPv4 - 32 bits
- 0-255 อย่าโง่มา 256 นะ
- Network + Host portion
	- Host = 2^n - 2
- Overhead
	- **Boardcast** : ตัวสุดท้าย
	- **Network** : วงเน็ต
	- **Gateway** : มักเป็นตัวแรก
	- ยิ่งซอยย่อย ยิ่งเสีย IP มาก = 2^n  IP ที่เสียไป

## Prefix Length
- จับตัว (bits) ยาวสุด

#### IP and Subnet = Network ID

#### Unicast (1-1)
#### Boardcast (1-all)
#### Multicast (1-many) [class D]

## NAT (Network @ Translation)
- Map Private and Public

#### Loopback (127.0.0.0/8)
#### Link-Local (169.254.0.0/16) -> for DHCP

| Class | IP |
|--------|--------------------------|
| Class A | (0.0.0.0/8 to 127.0.0.0/8) |
| Class B | (128.0.0.0 /16 – 191.255.0.0 /16) |
| Class C | (192.0.0.0 /24 – 223.255.255.0 /24) |
| Class D | (224.0.0.0 to 239.0.0.0) | 
| Class E | (240.0.0.0 – 255.0.0.0) |

### Boardcast Domain
- กลุ่มที่ได้รับ Boardcast
- 1 Network = 1 Boardcast Domain
- <font style="color:red">Router = segment boardcast</font> -> ไม่ส่ง boardcast ต่อ
- <font style="color:red">Switch = Flood</font>
### Collision Domain
- วงที่เวลาส่ง packet พร้อมกันแล้ว ชนกันเอง
- 1 Switch = 1 Collision Domain

#### DMZ (demilitarized zone) = public เข้าได้

#### VLSM (Variable Length Subnet Mask) = แบ่ง subnet แบบไม่ fixed length
- Network 161.246.6.0/23
- IP = 512 address

| Network           | Subnet          | IP                            |
|-------------------|-----------------|-------------------------------|
| 161.246.6.0/25    | 255.255.255.128 | 161.246.6.1 - 161.246.6.126   |
| 161.246.6.128/26  | 255.255.255.192 | 161.246.6.129 - 161.246.6.190 |
| 161.246.6.192/26  | 255.255.255.192 | 161.246.6.193 - 161.246.6.254 |
| 161.246.7.0/27    | 255.255.255.224 | 161.246.7.1 - 161.246.7.30    |
| 161.246.7.32/27   | 255.255.255.224 | 161.246.7.33 - 161.246.7.62   |

### DHCP -> สะดวกใช้งาน

