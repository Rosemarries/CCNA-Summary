#CCNA 

ไปดู slide / Module 2 เอา เยอะ

## Interface
```
	Router(config)# interface type-and-number
	Router(config-if)# decription decription-text
	Router(config-if)# ip address ipv4 subnet-mask
	Router(config-if)# ipv6 address ipv6/prefix-length
	
	//very important!
	Router(config-if)# no shutsdown
	
	Router# show running config
	Router# show ip interface brief
	Router# show ipv6 interface brief
	
```
<font style="color : red">no shutdown</font> เพื่อให้ interface มัน UP
<font style="color : red">อย่าลืม ping หากันด้วย!</font> : ping ได้ (router) จะเป็น '!' ต่อ 1 success
![[Screenshot 2566-05-21 at 09.47.29.png]]

### Verify command
| Command | Description |
|-----------|-------------|
| show ip interface brief | Displays all interfaces, their IP addresses, and their current status. |
| show ipv6 interface brief| |
| show ip route | Displays the contents of the IP routing tables stored in RAM. |
| show ipv6 route | |
| show interfaces | Displays statistics for all interfaces on the device. Only displays the IPv4 addressing information. |
| show ip interfaces | Displays the IPv4 statistics for all interfaces on a router. |
| show ipv6 interfaces | Displays the IPv6 statistics for all interfaces on a router. |

![[Screenshot 2566-05-21 at 09.53.13.png]]

- [up/down]
	- ช่องแรก = physical + datalink
	- ช่อง 2 = network layer

## Config Gateway
- มีแค่ Interface เดียวที่ออกข้างนอกได้
- ถ้าเป้น **DCE** ต้อง set clock rate
	```
	Router(config-if)# clock rate 56000 //เลือกมาสัก rate นึง
	Router(config-if)# no shutdown
	```

## Static Route
- <font style="color : red">ต้อง set ทั้ง 2 ฝั่ง!</font>
```
	Router(config)# ip route 10.1.1.0 255.255.255.0
```

