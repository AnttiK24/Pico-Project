# Pico Gesture Morse Transceiver

This project turns a Raspberry Pi Pico into a motion-controlled Morse code translator using **FreeRTOS**. It reads accelerometer data to interpret gestures as dots/dashes and translates them to text on an OLED display and is sent to computer.

###  Key Features
* **Motion Input:** Tilt the device to type Morse code.
* **Serial Comms:** Send Morse strings from a PC via USB to receive audio/visual alerts.
* **RTOS Architecture:** Runs 4 concurrent tasks (IMU, State Machine, UI, Serial) using a **Mutex** for thread-safe I2C access.

###  Controls
| Gesture | Action |
| :--- | :--- |
| **Tilt Left** | Dot (`.`) |
| **Tilt Right** | Dash (`-`) |
| **Tilt Forward** | Confirm Character / Space |
| **Button Hold** | Reset / Clear Display |

### Tech 
* **Hardware:** RP2040 (Pico), ICM-42670 (IMU), SSD1306 (OLED), Buzzer.
* **Software:** C, Pico SDK, FreeRTOS Kernel.
