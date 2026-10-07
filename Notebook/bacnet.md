# BACnet introduction

BACnet (Building Automation and Control Networks) is an open international standard communication protocol that allows building management systems and automation devices from different manufacturers to talk to each other

The official BACnet standard (ASHRAE 135) defines several ways to transport data across physical networks. These are officially known as BACnet Data Link Options.
They are categorized below into modern standards, wireless technologies, and legacy systems:

## Type of transportation
### 1. Modern & Mainstream Transports (Active)

These options represent the vast majority of all building automation systems installed today.
- • BACnet/IP (Internet Protocol):
  - • How it connects: Standard Ethernet cables (Cat5e/Cat6) or Wi-Fi.
	- • Mechanism: Wraps BACnet data inside standard IPv4 or IPv6 network packets using UDP (and occasionally TCP). It allows building data to travel across corporate IT networks, routers, and the internet.
- • BACnet MS/TP (Master-Slave/Token-Passing):
	- • How it connects: Shielded twisted-pair copper wire using the RS-485 serial standard.
	- • Mechanism: Completely bypasses the internet layer. Devices pass a digital "token" down the line to take turns speaking, preventing data packets from colliding. It is highly cost-effective and used for field-level controllers (like VAV boxes and thermostats).
- • BACnet/SC (Secure Connect):
	- • How it connects: Standard IT networks (Ethernet, Wi-Fi, Fiber).
	- • Mechanism: The newest standard designed for cybersecurity. It encapsulates traditional BACnet binary data inside encrypted WebSockets over TLS (HTTPS/TCP), allowing it to easily pass through strict corporate network firewalls without needing special UDP configurations.

### 2. Wireless Transports

These choices eliminate the need for running physical data cables through walls.
- • BACnet over Zigbee:
	- • How it connects: Low-power, short-range mesh radio waves (IEEE 802.15.4 standard).
	- • Mechanism: Adapts the BACnet protocol to run natively over wireless mesh networks, frequently used for wireless room sensors or lighting controls.

### 3. Specialty & Legacy Transports (Rarely Used Today)

These methods are either legacy systems from the 1990s/2000s or built to bridge other automation technologies.
• BACnet over Ethernet (ISO 8802-3):
	• How it connects: Standard Ethernet cables.
	• Mechanism: Sends data directly to a hardware MAC address, entirely skipping the IP routing layer. Because it cannot pass through IT network routers, it is restricted to a single local network segment.
• BACnet over LonTalk:
	• How it connects: LonWorks twisted-pair network wiring.
	• Mechanism: Maps BACnet protocol formatting onto a rival physical network technology (LonWorks) to allow cross-system communication.
• BACnet PTP (Point-to-Point):
	• How it connects: RS-232 serial cables or dial-up telephone modems.
	• Mechanism: A legacy dial-up connection layout used before broadband internet to allow a remote engineer to dial into a building's computer system.
• BACnet over ARCNET:
	• How it connects: Coaxial or twisted-pair cabling.
	• Mechanism: A 2.5 Mbps token-bus network type popular when BACnet was first released in 1995, now effectively obsolete.

