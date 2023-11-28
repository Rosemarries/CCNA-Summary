#CCNA 

### ICMPv4 -> check เฉยๆว่าเชื่อม host ได้ไหม
### ICMPv6 = ICMPv4 + ARP + IPv6

### TTL (Time to live)
- TTL -= 1 every hop
- if (TTL == 0) { "TTL expired in transit." => use **traceroute** }

## Test Connectivity (Ping/Traceroute)
- ping IP
- ping loopback (127.0.0.1)
- ping default-gateway
- ping remote-host
- traceroute IP (test path)