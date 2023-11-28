#CCNA 

# <font style="color:red">ข้อสอบ Lab ออก Config IPv6 12.6.6</font>

## IPv6 - 128 bits
- Prefix : 64 bits หน้า
- Interface ID : 64 bits หลัง

## IPv4 & IPv6
- **Dual Stack** : ทำแยก v4 v6
- **Tunneling** : v4 แปะหน้า v6
- **Translating** : แปลง ip

## IPv6 Representation
| Mode | IPv6 |
|------|-------|
|Preferred | 2001 : 0db8 : 0000 : 1111 : 0000 : 0000 : 0000 : 0200 |
|No leading zeros| 2001 : db8 : 0 : 1111 : 0 : 0 : 0 : 200|
|Compressed |2001:db8:0:1111::200|

### Unicast
1. Global Unicast Address (GUA) - เบื้องบน fixed มา
2. Link-local Address (LLA) - เฉพาะ link นี้นะไรงี้ = Default Gateway
![[Screenshot 2566-05-21 at 13.20.06.png]]
```
	//GUA
	R1(config)# interface gigabitethernet 0/0/0
	R1(config-if)# ipv6 address 2001:db8:acad:1::1/64
	R1(config-if)# no shutdown
	R1(config-if)# exit

	//LLA
	R1(config)# interface gigabitethernet 0/0/0
	R1(config-if)# ipv6 address fe80::1:1 link-local
	R1(config-if)# no shutdown
	R1(config-if)# exit
```

### Multicast
### Anycast - ตัวใกล้สุด

## RS & RA messages
The RA can provide three methods for configuring an IPv6 GUA :
- SLAAC (Stateless Address Auto-Configuration)
- SLAAC with stateless DHCPv6 server
- Stateful DHCPv6

## Interface ID
1. สร้างแบบ Random
2. เอา MAC address + data บางอย่าง แล้วเติมจนครบ 64 bits
	- **EUI-64**

|48-bit MAC |fc:99:47:75:ce:e0|
|------|-------|
|EUI-64 Interface ID |fe:99:47:ff:fe:75:ce:e0|

## Dynamic LLAs
![[Screenshot 2566-05-21 at 13.29.34.png]]
![[Screenshot 2566-05-21 at 13.30.57.png]]

## Well-known Multicast (ff00::/8)
- ff02::1 All-nodes multicast group
- ff02::2 All-routers multicast group (enable unicast routing)

## Subnet
![[Screenshot 2566-05-21 at 14.15.48.png]]

