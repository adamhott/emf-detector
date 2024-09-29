# EMF Detector Project (👻👻👻 Ghost Hunter 👻👻👻)

This project involves the design and construction of an Electromagnetic Field (EMF) Detector using various electronic components. The device aims to detect EMF levels and provide both a visual and numerical display of the detected values. It uses an ESP32-C6 microcontroller, a 4-digit 7-segment display, LEDs, and other components to create an affordable, portable EMF detection solution.

## Project Overview

The EMF Detector will:
- Detect electromagnetic fields using a **Hall effect sensor** mounted directly on the PCB.
- Display EMF readings on a **4-digit 7-segment display** controlled by the MAX7219 display driver.
- Use **10 LEDs** to provide a bar-graph-style visual indicator of EMF strength.
- Include two **potentiometers** for sensitivity adjustments.
- Be powered by a **5-cell AA NiMH battery pack** for extended battery life and rechargeable convenience.
- Incorporate a **3.5mm stereo audio jack** to listen to EMF level changes in real-time.

## Hardware Components

### Main Components
- **Microcontroller:** ESP32-C6 WiFi 6 + BLE 5.3 Module.
- **EMF Sensor:** DRV5053RAQLPG Hall Effect Sensor for detecting electromagnetic fields, mounted on the PCB.
- **Display:** **TDCR1060M** 4-digit 7-segment display, driven by the MAX7219CWG+T for numeric EMF values.
- **LED Bar:** 10 LEDs to indicate EMF intensity visually, connected to the ESP32-C6 GPIO pins.
- **Potentiometers:** Dual potentiometers (500kΩ stereo linear) for sensitivity control.
- **Power Source:** 5 AA NiMH batteries in series (6V nominal) with a low-dropout voltage regulator (LDLN050) to step down to 3.3V for the ESP32-C6 and display components.
- **USB-C Port:** Allows for an external power supply and potential data communication.
- **Stereo Audio Jack (3.5mm):** Enables audio output to listen to EMF levels, providing an auditory indication of electromagnetic field strength.

### Other Key Components
- **SPDT Toggle Switch (Locking):** Used for turning the device on/off.
- **JTAG Pads (TC2030-MCP):** For programming and debugging the ESP32-C6.
- **Inductors:** 100mH radial inductor for filtering and noise suppression.
- **Capacitors:** Various capacitors (e.g., 2.2µF, 1µF, 22µF) for noise filtering and stability in the power supply.
- **Diodes:** Includes ESD protection diodes (e.g., SD03) for USB-C and other sensitive components.

## Design Notes

- **Power Regulation:** The 6V from the NiMH battery pack is regulated to 3.3V using an LDO regulator (LDLN050) to power the ESP32-C6, display, and other components.
- **EMF Sensor:** The DRV5053RAQLPG Hall Effect Sensor, mounted on the PCB, provides an analog output, which is read by the ESP32-C6's ADC pin to measure electromagnetic fields.
- **Display Driver:** The MAX7219CWG+T drives the **TDCR1060M** 4-digit 7-segment display to show numeric values of detected EMF strength.
- **LED Indicators:** The 10 LEDs connected to GPIO pins on the ESP32-C6 act as a visual bar-graph, indicating the intensity of the detected electromagnetic field.
- **Audio Output:** The 3.5mm stereo audio jack provides an auditory signal to monitor EMF changes, with the output modulated according to the detected EMF levels.
- **Mounting:** Right-angle components (e.g., potentiometers and audio jacks) facilitate easy adjustment and connection within the device’s enclosure.

## Connections Overview

### Key Connections to the ESP32-C6
- **EMF Sensor:** The output of the DRV5053RAQLPG is connected to an ADC pin (ADC1_CH0) on the ESP32-C6.
- **7-Segment Display:** Controlled by the MAX7219 using DIN, LOAD, and CLK pins.
- **LEDs:** Connected to various GPIOs (GPIO3 - GPIO16) for individual control.
- **Stereo Audio Jack:** Connected to an appropriate GPIO pin and configured to output PWM or digital signal to modulate the audio based on EMF levels.
- **JTAG Header:** For programming and debugging, using the TXD0 and RXD0 pins.
- **USB-C Port:** Provides power to the circuit and ESD protection for the input.

## Usage

1. **Power On:** Use the locking SPDT toggle switch to power the device.
2. **Adjust Sensitivity:** Use the dual potentiometers to fine-tune the EMF detection sensitivity.
3. **Read EMF Levels:** The **TDCR1060M** 7-segment display shows numerical values, while the LED bar provides a quick visual indication of EMF intensity.
4. **Listen to EMF Levels:** Use the 3.5mm stereo audio jack to listen to the variations in EMF strength.

## Project Status

- **Current Stage:** Hardware design phase is nearing completion, with all main components selected and integrated into the KiCad schematic.
- **Next Steps:** Complete PCB layout in KiCad, order components, assemble the PCB, and begin firmware development for the ESP32-C6 to handle EMF detection, display updates, and audio output.

## License

This project is open-source and licensed under the MIT License.