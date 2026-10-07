# Field Interface Module (FIM)

A FIM (Field Interface Module) acts as the hardware backbone that connects the brain of the addressable system to the actual field wiring.

## How a FIM Works

The FIM bridges the gap between the panel's computer processor and the high-voltage/data requirements of the field devices. Here is the step-by-step process of how it functions:
1. **Powers the Loop:** The FIM takes raw power from the panel's power supply and converts it into the exact, stable DC voltage (usually between 15V and 32V) needed to power all the detectors and modules sitting on the parallel loop wires.
2. **Generates the Digital Data (Polling):** The FIM serves as the "translator." The central processor says, "Check device #5." The FIM converts that command into a digital data packet and transmits it down the parallel lines.
3. **Listens for Replies:** The FIM continuously listens to the electrical line for the tiny digital responses coming back from the sensors. If a sensor reports smoke, the FIM instantly decodes that signal and passes it to the main panel CPU to trigger the building-wide alarm.
4. **Self-Monitoring & Troubleshooting (Pseudo Points):** The FIM continuously monitors itself and the loop wiring. If there is an issue, it reports a "Fault" or "Trouble" state back to the panel. It checks for:
	- **Ground Faults:** If a bare wire touches a metal pipe or building structure.
	- **Short Circuits:** If the positive and negative wires accidentally touch each other.
	- **Open Circuits**: If a wire is severed or cut somewhere down the line.

Without the FIM, the fire alarm panel cannot talk to the devices on the wall. If a FIM breaks, an entire loop containing hundreds of detectors will go offline, and the panel will display a critical "FIM Fault" or "Loop Communication Failure"
