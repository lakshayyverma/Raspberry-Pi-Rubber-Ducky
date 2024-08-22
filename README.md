# USB Rubber Ducky using Raspberry Pi Pico

**Author:** Lakshay Verma

## Overview

This project demonstrates how to use a Raspberry Pi Pico to function as a USB Rubber Ducky. The Raspberry Pi Pico is programmed to emulate a Human Interface Device (HID) keyboard and inject keystrokes to automate tasks on a connected Windows system. In this experiment, the primary goal is to turn off Windows Defender using a scripted payload.

## Goals

- **Emulate HID Keyboard**: Make the Raspberry Pi Pico operate as a USB HID device that mimics a keyboard.
- **System Recognition**: Ensure the Raspberry Pi Pico is recognized as a HID device by the connected system.
- **Disable Windows Defender**: Inject a payload to disable Windows Defender on the connected Windows device.

## Requirements

### Hardware
- **Raspberry Pi Pico**: Microcontroller used for the experiment.
- **USB to Micro USB Cable**: For connecting the Raspberry Pi Pico to the system.

### Software
- **[dbisu/pico-ducky GitHub Repository](https://github.com/dbisu/pico-ducky)**: Contains necessary CircuitPython files and additional resources.
- **CircuitPython**: Programming environment required for the Raspberry Pi Pico.

## Procedure

1. **Download CircuitPython**
   - Go to [dbisu/pico-ducky GitHub Repository](https://github.com/dbisu/pico-ducky) and download the latest CircuitPython firmware.

2. **Install CircuitPython on Raspberry Pi Pico**
   - Click on the "DOWNLOAD .UF2 NOW" link to download the CircuitPython firmware.
   - Connect the Raspberry Pi Pico to your system using the USB to Micro USB cable.
   - Drag and drop the downloaded CircuitPython .uf2 file onto the Raspberry Pi Pico, which will appear as `RP1-RP2`.

3. **Prepare CircuitPython Libraries**
   - Download `adafruit-circuitpython-bundle-7.x-mpy-20221113.zip` from the [dbisu/pico-ducky GitHub repository](https://github.com/dbisu/pico-ducky).
   - Extract the zip file and navigate to `adafruit-circuitpython-bundle-7.x-mpy-20221113/lib`.
   - Move the `adafruit_hid` folder to the `CIRCUITPY/lib` directory on the Raspberry Pi Pico.

4. **Prepare Pico-Ducky Payload**
   - Download the Pico-Ducky repository as a zip file from GitHub and extract it.
   - Move `duckyinpython.py` to the root of `CIRCUITPY` and rename it to `code.py`.

5. **Edit Payload Code**
   - Open `code.py` and edit the file to include the desired payload code. 

6. **Final Steps**
   - Save the `code.py` file.
   - Disconnect and reconnect the Raspberry Pi Pico to the system. The payload will be automatically injected.
