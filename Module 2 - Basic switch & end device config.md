#CCNA 

## OS : Cisco IOS Access
- **Shell** : CLI (Command Line Interface) and GUI (Graphic User Interface)
- **Kernel** : Communicate between HW and SW
- **Hardware** : Physical parts

## Access Methods
- **Console** : Physical management port (สาย LAN, VGA) -> provide maintenance : init config
- **Secure Shell (SSH)** : secure remote CLI connection
- **Telnet** : insecure remote CLI connection

## IOS Navigation
- ### EXEC Mode
	- <font style="color : skyblue">User EXEC Mode</font> : User
	```bash
	[Hostname]>
	
	Router>
	Switch>
	```

	- <font style="color : skyblue">Privileged EXEC Mode</font> : Admin
	```bash
	[Hostname]#
	
	Router#
	Switch#
	```

- ### Configuration & Subconfiguration Mode
	- <font style="color : lime">Global Configuration Mode</font> : used to access config obtions on the device
	```bash
	[Hostname](config)#
	
	Router(config)#
	Switch(config)#
	```
	
	 - <font style="color : lime">Line Configuration Mode</font> : used to config *Console, SSH, Telnet, AUX* access
	 ```bash
	[Hostname](config-line)#
	
	Router(config-line)#
	Switch(config-line)#
	```
	
	 - <font style="color : lime">Interface Configuration Mode</font> : used to config a *switch port, router interface*
	 ```bash
	[Hostname](config-if)#
	
	Router(config-if)#
	Switch(config-if)#
	```

## Navigation Between IOS Modes
- <font style="color : skyblue">User EXEC Mode</font> <-> <font style="color : skyblue">Privileged EXEC Mode</font> <-> <font style="color : lime">Global Configuration Mode</font> <-> <font style="color : lime">Line Configuration Mode</font> <-> <font style="color : lime">Interface Configuration Mode</font>
	```
	Switch> enable
	Switch# configure terminal
	Switch(config)# line console 0
	Switch(config-line)# interface FastEthernet 0/1
	Switch(config-if)# 

	Switch(config-if)# exit
	Switch(config-line)# exit
	Switch(config)# exit
	Switch# exit
	Switch> 
	```

## IOS command syntax
| Convention    | Description |
|---------------|----------------------------------|
| bold          | command / keyword |
| italic        | arguments |
| [x]           | optional elements |
| {x}           | required elements |
| [x { y \| z }] | required choice with optional elements |
<font style="color : red">*ถ้าไม่รู้ command หรือ argument ให้ใช้ "?" ต่อท้าย</font>
<font style="color : red">กด "TAB"</font> เพื่อ autocomplete
<font style="color : red">กด "SPACEBAR"</font> เพื่อ goto next page ตอน --More--

<font style="color : pink">Ctrl-C, Ctrl-Z</font> : end config mode -> return to EXEC mode
<font style="color : pink">Ctrl-Shift-6</font> : kill -9

## Basic Device Config
```
	//change Hostname
	Switch# configure terminal
	Switch(config)# hostname SW1
	SW1(config)#

	//change password for login in 'SW1>'
	// console = setup
	// vty = remote, plz setup port to connect
	// ex. line vty 0 4 //port 0-4
	SW1(config)# line console 0
	SW1(config-line)# password cisco
	SW1(config-line)# login

	//change password for login in privileged mode 'SW1#'
	SW1(config-line)# enable password c1$c0

	//set secret a encrypted password
	SW1(config-line)# enable secret itsasecret

	//change all plain text password into encrypted one
	SW1(config-line)# enable password-encryption

	//set warning message when not login
	SW1(config-line)# banner motd "Authorized User ONLY!!!"
	SW1(config-line)# exit
	SW1(config)#

	//show config that done above
	SW1# show running-config

	//save running-config(may lost config if no electricity) to 
	//startup-config(NVRAM [non-validate (ไม่ต้องใช้ไฟ ก็ save ได้)])
	SW1# copy running-config startup-config


	//use 'erase' to reset config
	SW1# erase startup-config

	//use 'no' to reset what we have config
	SW1# conf t
	SW1(config)# line console 0
	SW1(config-line)# no enable password

	//switch to interface
	SW1# conf t
	SW1(config)# interface vlan 1
	SW1(config-if)# ip address 192.168.1.20 255.255.255.0
	SW1(config-if)# no shutdown
```

