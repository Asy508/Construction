
# The 4 Biggest Conceptual Gaps You Need to Learn

To transition smoothly, you need to shift your mindset from a circuit board level to a facility infrastructure level. Focus your learning on these four pillars:

## 1. Industrial Networking Protocols

In embedded systems, you deal with short-distance chip communication. In ELV, you deal with building-wide communication. You must learn:
- [BACnet](/Notebook/bacnet.md) (IP and MS/TP): The undisputed king of Building Automation. It allows different vendors' HVAC and control systems to talk to each other.
- Modbus (RTU and TCP): Heavily used to read data from electrical meters, VFDs (Variable Frequency Drives), and generators.
- ONVIF: The global standard protocol for IP cameras (CCTV) to communicate with Network Video Recorders (NVRs).

## 2. IT Networking & Structured Cabling

Modern ELV is almost entirely IP-based. You need to understand:
- Subnetting, VLANs, and IP addressing: ELV systems usually run on a dedicated corporate virtual network (VLAN) to separate security/BMS data from regular office internet.
- PoE (Power over Ethernet): How switches deliver both power and data to IP cameras, access control readers, and VoIP phones.

## 3. Standard ELV Hardware Form Factors

Instead of soldering components onto a PCB, ELV engineering is about "system integration." You buy off-the-shelf industrial modules and wire them together inside a wall-mounted panel.
- Relays and Contactors: You will use small 24V DC control signals from a DDC to switch heavy 230V/400V AC hardware.
- Standard Signals: Master how 0-10V DC voltage loops and 4-20mA current loops are used to transmit analog sensor readings over hundreds of meters without signal degradation.

## 4. Reading Construction Drawings

You need to learn how to read building layouts instead of circuit schematics.
- Shop Drawings: Floor plans showing where cameras, card readers, and smoke detectors are physically installed.
- Schematic Matrix / Single Line Diagrams (SLD): Block diagrams showing how the DDC panel connects to the sensors in the field.

# Where to Start Learning (Proactive Steps)

If you want to start building your knowledge base immediately, I recommend looking into these specific areas:
- Look up BACnet: Download a free tool like YABE (Yet Another BACnet Explorer) on your PC. It will give you a visual idea of how data points are exposed over a building network.
- Study standard BMS logic: Look up "Function Block Programming for BMS". It is very similar to visual programming or state-machine logic you might have seen in embedded software development.
- Explore major manufacturers: Go to the documentation sections of brands like Honeywell (Trend/Alerton), Schneider Electric (EcoStruxure), Siemens (Desigo), or Johnson Controls. Read their product data sheets for DDC controllers to see how they layout their I/O terminals.
To help narrow down your first study topic, which branch of ELV excites you the most?
- The Automation side (BMS, DDC, energy efficiency, HVAC control)
- The Security/Safety side (CCTV, Access Control, Fire Alarms)
- The Network Infrastructure side (ICT, Fiber optics, Structured cabling)
