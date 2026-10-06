# Signaling Line Circuit (SLC)

A SLC is a 2-wire loop connecting a fire alarm control panel FACP to addressable device. 
- High voltage/Industrial:
    - Designed to handle heavy environmental noise.
- Power and data combined:
    - The data packets right on top of the 24V power line
- Speed:
    - Deliberately slow, often under 10k bps
- Core functions
    - Two-way communication, constant device polling, power delivery and exact-location ID.
- Common Protocols:
    - CLIP : Serial polling, support up to 99 detectors and 99 modules(legacy)
    - FlashScan: Group polling(blocks of 10), faster response, support up to 159 detector and 159 modules per loop.
- Wiring Classes:
    - Class A, B or X (includes isolators before/after devices)
- Electrical Limits:
    - Typically max 40~50 ohms loop resistance and 0.5 uF capacitance
- Troubleshooting:
    - Check for open, shorts, ground faults, double/duplicate addresses and loop resistance limits.

- Example DIY:
    - ![Example](assets/graph.png)

