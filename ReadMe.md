# 1. Visuals (Blueprints & Schematics)

## Understanding ELV Systems: Why They Matter to Modern Facilities
The 5 Core Domains of ELV Systems
In modern commercial construction, ELV is broken down into five primary categories. Almost every cable that is not a heavy mains power line falls into one of these buckets:
- 🚨 1. Life Safety & Environmental Systems
These systems must operate with 99.99% reliability, which is why they use specialized topologies like the SLC loops we discussed.
  - • Fire Alarm Systems (FAS): Detectors, pull stations, strobes, and fault isolators.
  - • Gas Detection Systems: Carbon monoxide and methane monitors for industrial spaces or parking garages.
  - • Emergency Voice Communication: Warden interphones and fireman intercoms.
- 🔒 2. Security & Surveillance Systems
These systems focus on property protection and tracking data, heavily utilizing digital networking and differential communication.
  - • CCTV (Closed-Circuit Television): IP cameras powered via PoE (Power over Ethernet).
  - • Access Control Systems (ACS): Card readers, biometric scanners, electromagnetic door locks, and break-glass units.
  - • Intrusion Detection Systems (IDS): Motion sensors, glass-break detectors, and magnetic door contacts connected to a security panel.
- 🏢 3. Building Automation & Smart Controls (BMS)
The "brain" of the building, which regulates energy usage and mechanical operations.
  - • Building Management Systems (BMS): Uses protocols like BACnet or Modbus to let chillers, pumps, and fans talk to a central station.
  - • Smart Lighting Controls: Uses DALI loops or KNX buses to automate building lighting schedules and dimming.
- 🛜 4. Telecommunications & Information Technology (ICT)
The backbone data highways that all other ELV systems increasingly rely on.
  - • Structured Cabling Systems (SCS): The physical infrastructure of Cat6 copper cables, patch panels, and fiber optics running through a building.
  - • Public Address & Voice Alarm (PAVA): High-voltage audio lines (70V/100V distributed audio) used for background music and emergency announcements.
  - • SMATV/MATV: Satellite and master antenna television distribution networks.
- 🚗 5. Specialized Extra-Low Voltage Systems
Niche operational architectures built for specific facility needs.
  - • Car Park Management Systems (CPMS): Automatic license plate recognition (ALPR), boom gates, and ticketing kiosks.
  - • Nurse Call Systems: Pull cords, bed head units, and dome lights used in healthcare facilities.

## The 3 Core Communication Patterns in ELV
As an embedded electronics enthusiast, you will notice that no matter what the system is called, it will almost always use one of three distinct hardware communication methods to move data across a building:
|Communication Type	|How It Works	|Where You See It|
| :--- | :--- | :--- |
|Power + Data Combined (2-Wire)	|Blends power and data on a single pair using voltage dips and current spikes.	|Fire Alarm SLC, DALI Lighting, Gas Detection arrays.|
Differential Digital (Data Only)	Uses two dedicated wires (RS-485 / CAN Bus) to transmit complementary square waves. immune to noise, but requires separate power wires.	BACnet MS/TP, Modbus HVAC networks, Access Control readers.
IP Networking (Ethernet)	High-speed data packets over twisted pairs. Can use PoE (Power over Ethernet) to inject 48VDC directly onto the data lines.	Modern IP CCTV cameras, BACnet/IP automation, Wi-Fi Access Points.

## Fire Alarm Systems
### CoreTypes of Fire Alarms Panle
- Conventional Panels: divide into several zones; ideal for smaller site
- Addressable Panel: unique ID to device(sensor) and pinpoint the precise location.
- Intelligent Panels: Addresable system to cloud system

### Local Compliance & Standard
- Placement Requirement: Ready accessible zone (Fire Command Centre, guardhouse, main lobby, security room approved by BOMBA)
- Mandatory Approvals: System must pass local inspection to secure or renew Fire Certificate (FC)
- Local Manufacturers & Brands: Program Electronic Sdn Bhd, Demco Industries Sdn Bhd, and global brands Notifier & Hochiki

![Program Electronic Fire Alarm Panel](https://programelectronic.my/wp-content/uploads/2022/03/FAP-a-01.jpg)

- Every component must comply with MS-1745(Malaysia Standard adapt from BS-5839)

### 3 Pillars of Fire Systems
- Input device
    - Smoke detector
    - Heat detector
    - Manual Call Points (MCP)

- Output Devices (Notification & Interfacing)
    - Siren & Flasher
    - BMS/Scada Interfacing
    - Auxiliary Controls

- Wiring Topologies
    - Conventional (Zone-based) : Uses 2-core fire-rated cables (like FP200 or PVC/Conduit) arranged in a radial circuit. If a detector fires, you only know the zone (e.g., Level 2, Zone A), not the exact room.
    - Addressable (Loop-based) : • Uses a continuous loop starting and returning to the panel. It uses a digital protocol to talk to each device individually. If a detector triggers, the panel screen tells you exactly: "Device 045 - Level 3 Room 302".

## ELV installer accountable to standard MEP specifications:

### 1. Review the Material Approval (MAS)
Before they pull a single wire, ask the contractor for the approved Material Approval Submission (MAS) or Technical Data Sheets for the cables and containment.
- Fire Alarm Cables: Ensure they are using the exact approved fire-rated brand specified (e.g., FP200 Gold, Prysmian, or equivalent depending on regional specs). Look for third-party certifications like LPCB (Loss Prevention Certification Board) or UL listing printed directly on the cable insulation jacket.
- Conduits: Check if the specification requires Galvanized Iron (GI) steel conduits or heavy-duty High-Impact PVC. In many commercial specs, fire alarm lines must run strictly in red-painted GI conduits for maximum physical protection.
### 2. Check the "Shop Drawings" vs. Site Reality
The installer must follow the approved ELV Shop Drawings.
- Containment Routing: Walk the corridors. Make sure the ELV cable trays are installed exactly where shown on the drawings and are not clashing with mechanical ductwork or plumbing pipes.
- Clearance: Verify that the physical spacing between the ELV tray and the electrical LV power tray matches the specified distance (typically a minimum of 300mm for unshielded power distribution).
### 3. Inspect Cable Pulling & Termination Quality
- No Splices/Joints: Fire alarm and critical ELV loops must be pulled in one continuous length from the panel to the device or junction box. Under standard specs, straight through through-wire cable joints/splices hidden inside conduits are strictly forbidden because they create failure points.
- Bending Radius: Ensure the cables aren't bent sharply around tight corners. Fire-rated and data cables have a mandatory minimum bending radius (usually 6x to 8x the outer diameter of the cable). Bending them too tightly damages the internal insulation and shields.
- Identification & Tagging: Every cable must have a durable, printed cable tag/ferrule at both ends and inside junction boxes matching the asset tags on the schematics (e.g., L1-D01 for Loop 1, Device 1). Hand-written masking tape is usually a violation of spec.
### 4. Witness the Testing & Commissioning (T&C)
Do not take the installer's word that it works. You should formally witness their T&C stage:
- Insulation Resistance (Megger Test): Before connecting devices, they must test the ELV cables with a Megger tester (typically at 250V or 500V DC for ELV) to prove there are no nicks or shorts in the insulation inside the conduits.
- Loop Continuity Test: They must measure and log the resistance of the copper loops to ensure the wire lengths don't exceed the panel manufacturer’s maximum allowable limits.


