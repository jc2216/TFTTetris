# TFTTetris
A 1.8" TFT powered by a Raspberry Pi Pico that can play the hit game Tetris. Control the position of the block by rotating the device, and rotate the block by pressing a button.

## Features
- 1.8" TFT display
- Raspberry Pi Pico
- MPU-6050 IMU
- Push Button
- Active Buzzer
- 3.7V LiPo Battery
- TP4056 USB-C Charger

## Schematic
<img width="731" height="524" alt="Screenshot 2026-11-01 at 3 23 28 PM" src="https://github.com/user-attachments/assets/0cbd2108-b2b6-49d4-9284-2dfb2b4a4425" />

- TFT is connected to Raspberry Pi Pico through a few pins. Capacitors are also connected to soak up current spikes when the screen redraws.
- Transistors + Resistors to safely power backlight, while also allowing firmware to turn it on/off.
- MPU-6050 connected to Raspberry Pi Pico to detect rotational motion. Push button also connected to the Pi.
- Buzzer requires transistor to get more current than what the Pi can supply. Resistor limits current to transistor to be safe.
- TPU-4056 Battery Pads are connected to the Battery Socket. TP4056 Output pads are connected to Slide Switch, which can turn on and off the system. Diode prevents power from flowing backwards.

## PCB

<img width="398" height="425" alt="Screenshot 2026-11-01 at 7 22 19 PM" src="https://github.com/user-attachments/assets/c71eee63-97fd-49b8-b21c-72902ded3fac" />

<img width="575" height="584" alt="Screenshot 2026-11-01 at 7 21 39 PM" src="https://github.com/user-attachments/assets/43fe494b-5db0-4aca-9220-514f1573d130" />

- Ground fill added, routed the PCB.
- Added neat little drawings for fun.
- Had to create space for the TFT screen at the end (because it can't go over the buzzer + switch), led to more pain.
- The battery, TPU-4056, MPU-6050, and TFT board will hang off of the PCB.

## Firmware
- Currently in progress
- Will be added soon

## BOM
| Item | Qty | Supplier | Cost/item | Total | Link |
|---|---|---|---|---|---|
| Tact push button | 1 | AliExpress | $0.96 | $0.96 | [Link](https://www.aliexpress.us/item/3256805859865632.html) |
| MPU6050 | 1 | AliExpress | $3.89 | $3.89 | [Link](https://www.aliexpress.us/item/3256812536361672.html) |
| Raspberry Pi Pico | 1 | AliExpress | $2.63 | $2.63 | [Link](https://www.aliexpress.us/item/3256805430865417.html) |
| 1.8" TFT | 1 | AliExpress | $2.97 | $2.97 | [Link](https://www.aliexpress.us/item/3256805953674718.html) |
| 3.7V 800 mAh LiPo | 1 | AliExpress | $1.09 | $1.09 | [Link](https://www.aliexpress.us/item/3256808535461122.html) |
| S8050 transistors | 1 | AliExpress | $2.64 | $2.64 | [Link](https://www.aliexpress.us/item/3256806624734473.html) |
| Slide switch | 1 | AliExpress | $1.11 | $1.11 | [Link](https://www.aliexpress.us/item/3256804214993913.html) |
| TP4056 | 1 | AliExpress | $1.10 | $1.10 | [Link](https://www.aliexpress.us/item/3256808491871337.html) |
| SS14 Schottky diode | 1 | AliExpress | $2.18 | $2.18 | [Link](https://www.aliexpress.us/w/wholesale-ss14-Schottky-diode.html) |
| AO3401A transistor | 1 | AliExpress | $2.10 | $2.10 | [Link](https://www.aliexpress.us/item/3256811832598213.html) |
| Molex PicoBlade | 1 | AliExpress | $2.25 | $2.25 | [Link](https://www.aliexpress.us/item/3256809135240230.html) |
| R1, 100 Ω resistor, 0805 | 1 | | | | |
| R2, 10 kΩ resistor, 0805 | 1 | | | | |
| R3, 1 kΩ resistor, 0805 | 1 | | | | |
| C1, 10 µF ceramic capacitor, 0805 | 1 | | | | |
| C2, 100 nF ceramic capacitor, 0805 | 1 | | | | |
| Active buzzer, 3 to 3.3 V | 1 | | | | |
| PCB | 1 | JLCPCB | $4.00 | $4.00 | [Link](https://jlcpcb.com) |
| Estimated shipping | 1 | | | $15.63 | |
| **Total** | | | | **$42.55** | |




