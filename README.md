# EMF Detector Project (👻👻👻👻👻 Ghost Hunter 👻👻👻👻👻)

This project involves the design and construction of an Electromagnetic Field (EMF) Detector using various electronic components. The device aims to detect EMF levels and provide both a visual and numerical display of the detected values. It uses an ESP32-C6 microcontroller, a 4-digit 7-segment display, LEDs, and other components to create an affordable, portable EMF detection solution.

## Project Overview

The EMF Detector will:
- Detect electromagnetic fields using an external sensor wand.
- Display EMF readings on a **4-digit 7-segment display**.
- Use **10 LEDs** to provide a bar-graph-style visual indicator of EMF strength.
- Include two **potentiometers** for sensitivity adjustments.
- Be powered by a **5-cell AA NiMH battery pack** for extended battery life and rechargeable convenience.

## Hardware Components

### Main Components
- **Microcontroller:** ESP32-C6
- **EMF Sensor Wand:** Detects electromagnetic fields with adjustable sensitivity.
- **Display:** LTC-4627JR 4-digit 7-segment display for numeric EMF values.
- **LED Bar:** 10 LEDs to indicate EMF intensity visually.
- **Potentiometers:** Dual potentiometers (500kΩ stereo linear) for sensitivity control.
- **Power Source:** 5 AA NiMH batteries in series (6V nominal) with voltage regulation for the ESP32-C6 and display components.

### Other Key Components
- **Right-Angle 3.5mm Stereo Audio Jack:** For external connections.
- **SPDT Toggle Switch (Locking):** Used for turning the device on/off.
- **9V Battery Holder:** Initially considered but replaced with AA NiMH cells.
- **JTAG Header:** For programming and debugging the ESP32-C6.

## Design Notes

- **Power Regulation:** A voltage regulator will step down the 6V from the NiMH battery pack to the required 3.3V for the ESP32-C6 and other components.
- **Mounting:** Components like the potentiometers and 3.5mm audio jack will be mounted on a custom PCB designed in KiCad.
- **Right-Angle Components:** Right-angle potentiometers and audio jacks have been chosen to facilitate easy adjustment and connection within the device’s enclosure.

## Usage

1. **Power On:** Use the locking SPDT toggle switch to power the device.
2. **Adjust Sensitivity:** Use the dual potentiometers to fine-tune the EMF detection sensitivity.
3. **Read EMF Levels:** The 7-segment display shows numerical values, while the LED bar provides a quick visual indication of EMF intensity.
4. **External Connections:** Use the 3.5mm audio jack for external interfaces if needed.

## Project Status

- **Current Stage:** Hardware design and component selection phase.
- **Next Steps:** Complete the KiCad PCB design, assemble components, and begin firmware development for the ESP32-C6.

## License

This project is open-source and licensed under the MIT License.