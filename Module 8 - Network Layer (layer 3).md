#CCNA 

## Network layer
- Addressing end devices
- Encapsulation
- Routing
- De-encapsulation
![[Screenshot 2566-05-21 at 08.55.10.png]]

|Function | Description|
|---------|------------|
|Version |This will be for v4, as opposed to v6, a 4 bit field= 0100|
|Differentiated Services |Used for QoS: DiffServ – DS field or the older IntServ – ToS or Type of Service|
|Header Checksum |Detect corruption in the IPv4 header|
|Time to Live (TTL)| Layer 3 hop count. When it becomes zero the router will discard the packet.|
|Protocol |I.D.s next level protocol: ICMP, TCP, UDP, etc.|
|Source IPv4 Address |32 bit source address|
|Destination IPV4 Address |32 bit destination address|

## IP
- Connectionless
- Best Effort
- Media Independent

#### Connectionless
 - เปรียบดั่ง ไปรษณีย์
 - ถึงแน่
#### Best Effort
- เปรียบดั่ง การโทรศัพท์
- บาง packet อาจหายไป

## Host Forwarding Decision
- Packets are always created at the source.
- Each host devices creates their own routing table.
- A host can send packets to the following:
	- Itself – 127.0.0.1 (IPv4), ::1 (IPv6)
	- Local Hosts – destination is on the same LAN
	- Remote Hosts – devices are not on the same LAN
- The Source device determines whether the destination is local or remote
- Method of determination:
	- IPv4 – Source uses its own IP address and Subnet mask, along with the dest IP address
		- ไม่รู้ไปไหน ไป 0.0.0.0 (IPv4 ทั้งหมด)
	- IPv6 – Source uses the network address and prefix advertised by the local router
- Local traffic is dumped out the host interface to be handled by an intermediary device.
- Remote traffic is forwarded directly to the default gateway on the LAN.

## Host Forwarding table
```
	Router# netstat -r
```

## Default Gateway
- คุยออกข้างนอก ส่วนใหญ่เป็น IP router

## Routing
- Router ดูจาก Routing table ของตัวเอง (setup แบบ manual)
![[Screenshot 2566-05-21 at 09.08.53.png]]

### Directly Connect
 - route automatically added by router
### Remote
- Manually - static
- Dynamic - Routing protocol
### Default Route
- forwards all traffic to a specific direction when there is not a match in the routing table
![[Screenshot 2566-05-21 at 09.15.26.png]]

### Static routing
- manually
- small network
- not Up-to-Date
- ![[Screenshot 2566-05-21 at 09.17.11.png]]
### Dynamic routing
- discover remote network
- น้องรู้เอง Up-to-Date
- automatically
- ![[Screenshot 2566-05-21 at 09.18.41.png]]

### Routing Table
```
	Router# show ip route
```

| Source (รู้จากไหน) | Description | Route |
|-------------------|---------------------------|-----|
| L | local | (directly connect) |
| C | connected | (directly connect) |
| S | Static route | (default route)|
| O | OSPF | (remote route) |
| D | EIGRP | (remote route) |

