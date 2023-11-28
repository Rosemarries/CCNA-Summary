#CCNA 

## Transport between Hosts (segments)

## Protocol

![[Screenshot 2566-05-21 at 14.42.52.png]]

## UDP (User Datagram Protocol)
- Connectionless
- ส่งไปเลย ไม่มี handshake อะไรทั้งนั้น กุนักเลงพอ
- best-effort

## TCP
- 3-way handshake
- congestion control
- flow control
- retransmission
- reliable
### netstat -> test TCP connection

### Header
![[Screenshot 2566-05-21 at 14.46.04.png]]
 - **Socket Pairs**
 - ![[Screenshot 2566-05-21 at 14.47.35.png]]


## Well-known Ports
- 3389 -> Remote Desktop for Windows
- Well-known ports – numbers 0 to 1023  
- Registered ports – numbers 1024 to 49151  
- Dynamic or private ports – numbers 49152 to 65535
![[Screenshot 2566-05-21 at 14.48.56.png]]

### TCP Connection Establishment 
![[Screenshot 2566-05-21 at 14.56.06.png]]
### TCP Session Termination
![[Screenshot 2566-05-21 at 14.56.20.png]]

### Data lost & Retransmission
1. **Go-Back-N** = ส่งใหม่หมด
	![[Screenshot 2566-05-21 at 14.57.53.png]]
2. **Selective Repeat** = ส่งแค่ที่ยังไม่ได้
	![[Screenshot 2566-05-21 at 14.58.11.png]]

### Flow Control
- MSS MTU ทำมาแล้ว อย่าโง่!!!
![[Screenshot 2566-05-21 at 15.00.29.png]]

