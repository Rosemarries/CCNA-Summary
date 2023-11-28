#CCNA 

## Physical Components
1. HW devices
2. Media
3. other connectors

## Encoding
	![[Screenshot 2566-05-20 at 14.49.18.png]]
### NRZ vs Manchester
| NRZ             | Manchester      |
|-----------------|-----------------|
| 0, 1 ปกติ        | 0 : 0->1        |
|                 | 1 : 1->0        |
| - freq น้อย      | - freq มาก      |
| - bandwidth น้อย | - bandwidth มาก |

## Signaling
![[Screenshot 2566-05-20 at 14.49.50.png]]

### Bandwidth Terminology
- **Latency** : เวลาที่ทำให้ช้า (delays)
- **Throughput** : bits ที่ส่งได้ / เวลาทั้งหมด
- **Goodput** : data ที่ใช้ได้ / เวลาทั้งหมด
	- Goodput = Throughput - traffic overhead

## Copper Cable
- **Unshielded Twisted-Pair Cable** (UTP) : ไม่มีหุ้ม, RJ-45, limited crosstalk(noised)
	- Crossover : สำหรับอุปกรณ์ชนิดเดียวกัน (ex. com-com, hub-hub)
	![[Screenshot 2566-05-20 at 15.12.17.png]]
- **Shielded Twisted-Pair Cable** (STP) : มีหุ้ม, RJ-45, LAN
- **Coaxial Cable** : บิด พัน ม้วน, ต่อหลัง TV

## Fiber-Optic Cable (ชนะ copper ขาด แต่คดแพง)
![[Screenshot 2566-05-20 at 15.16.54.png]]

## Wireless
- WiFi : IEEE 802.11, WLAN (Wireless LAN)
- BlueTooth : IEEE 802.15, WPAN (Wireless Personal Area Network)
- WiMAX : IEEE 802.16, Point-to-Multipoint to boardband wireless access
- Zigbee : IEEE 802.15.4, Low data-rate, Low power-consumption, For IoT
- #### Requirement
	- Access Point(AP)
	- NIC (Network Interface Card) Adapter


