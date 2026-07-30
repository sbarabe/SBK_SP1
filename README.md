# SBK_SP1

**Open-source soft power switch module for learning and embedded electronics projects.**

SBK_SP1 is a compact, reusable soft power switch module for battery-powered embedded systems. It allows a momentary push button and a microcontroller GPIO to control system power while consuming only a few microamps when turned off.

Designed for breadboards, prototypes, and educational projects, SBK_SP1 provides an easy way to add professional soft power management to Arduino, ESP32, RP2040, ATtiny, STM32, and similar microcontroller-based systems.

---

## Features

- Input voltage: **2–12 VDC**
- Load current: **up to 2 A**
- High-side **P-channel MOSFET** switching
- Microcontroller-controlled soft power latching
- Ultra-low off-state current
- Power input and output status LEDs
- Breadboard-friendly 2.54 mm pin header
- Fully assembled with JLCPCB Basic components

---

## Pinout

| Pin | Description |
|------|-------------|
| **VIN** | Power input (2–12 VDC) |
| **GND** | Ground |
| **VOUT** | Switched power output |
| **CTRL** | Control input (0–VIN). Drive HIGH to enable the output. |

---

## Typical Application

```text
Battery
   │
SBK_RP1 (optional)
   │
SBK_SP1
   │
Microcontroller
```

A momentary push button is connected to the **CTRL** input to power the system. Once the microcontroller has started, it drives **CTRL** HIGH to keep the module enabled. When the application is ready to shut down, the microcontroller releases the **CTRL** pin, automatically removing power from the system.

---

## Operation

1. The user presses the push button.
2. The **CTRL** input goes HIGH.
3. SBK_SP1 enables the power output (**VOUT**).
4. The microcontroller boots.
5. The microcontroller drives **CTRL** HIGH to maintain power after the button is released.
6. When shutdown is requested, the microcontroller releases **CTRL**.
7. SBK_SP1 disconnects power from the load.

---

## Applications

SBK_SP1 is suitable for a wide variety of battery-powered embedded projects, including:

- Arduino
- ESP32
- RP2040
- ATtiny
- STM32
- Portable instruments
- Battery-powered sensors
- Educational electronics projects
- Custom embedded devices

---

## Related Projects

- [**SBK_RP1**](https://github.com/sbarabe/SBK_RP1) – Reverse Polarity Protection Module
- [**MémoBot**](https://github.com/sbarabe/MemoBot) – Educational memory game built using SBK_SP1 and SBK_RP1

---

## License

This project is released as open-source hardware under the **CERN Open Hardware Licence Version 2 - Permissive (CERN-OHL-P v2)**.

You are free to study, modify, manufacture, and distribute this design, provided the terms of the license are respected.

See the [LICENSE](LICENSE) file for the full license text.

## Design with KiCad 10
