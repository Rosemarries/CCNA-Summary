#CCNA 

#### Hop-to-Hop (Frame)
- error detection & reject corrupt frame
![[Screenshot 2566-05-20 at 15.32.16.png]]

## 2 sublayer of datalink
1. **Logical Link Control (LLC)** : communicate between upper and lower layer
2. **Media Access Control (MAC)** : responsible for encapsulation and MAC

## WAN Topologies
- **Point-to-Point** : permanent link between 2 endpoints
- **Hub(layer 1) & Spoke** : centralized + point-to-point, star
- **Mesh** : ทุกเครื่อง endsystems ต้องต่อกับ ทุกเครื่อง endsystems

## LAN Topologies
- **Star** : เจอบ่อยสุด มี centralized device คอยเป็นศูนย์กลาง
- **Bus** : มี Backbone, T-junction ปกติมีใน Hub
- **Ring** : ปกติจะใช้กับ Token -> เครื่องที่มี token = ส่งได้, ไม่มี token = ส่งไม่ได้ ต้องรอ
![[Screenshot 2566-05-20 at 15.43.34.png]]

### Half and Full Duplex Communication
- **Full-duplex** (default for switch) : ส่งได้ทั้ง 2 ทาง
- **Half-duplex** : ส่งทางนึงก่อน ค่อยส่งอีกทาง

