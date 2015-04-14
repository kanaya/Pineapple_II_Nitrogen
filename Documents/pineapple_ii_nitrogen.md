# Pineapple II Nitrogen/0.0.0 Tech Doc

## Interface

| Panel/Port      | Pin | Signal              | Int. Port | Micro Pin        |
| --------------- | --- | ------------------- | --------- | ---------------- |
| **Power**       | P1  | Power (7V to 12V)   | F01, F03  | Vin              |
|                 | P2  | GND                 | F02, F04  | GND              |
| **Panel**       | LED | Main LED            | F07-F08   | D13PWM-(R-GND)   |
|                 | RST | Reset               | F05-F06   | RST-GND          |
| **GeekPort II** | G01 | Vin                 |           | Vin              |
|                 | G02 | GND                 | U5        | GND              |
|                 | G03 | USB D+ or Sensor X  | U3        | U3 or D10PWM/A10 |
|                 | G04 | USB D- or Sensor Y  | U2        | U2 or D9PWM/A9   |
|                 | G05 | USB Power           | U1        | U1 and D8/A8     |
|                 | G06 | Cable detector      |           | D6PWM/A7         |
|                 | G07 | Vcc                 |           | Vcc              |
|                 | G08 | Sensor A            |           | A0               |
|                 | G09 | Sensor B            |           | A1               |
|                 | G10 | Sensor C            |           | A2               |
|                 | G11 | Sensor D            |           | A3               |
|                 | G12 | I2C SDA or Sensor E |           | D2INT or A4      |
|                 | G13 | I2C SCL or Sensor F |           | D3INTPWM or A5   |
|                 | G14 | GND                 |           | GND              |
| **MIDI OUT+**   | X1  | MIDI OUT+ Power     | B01       | Vcc              |
|                 | X2  | MIDI OUT+ GND       | B02       | GND              |
|                 | X3  | MIDI OUT+ Raw TX    | B03       | TX + Buffer      |
|                 | X4  | MIDI OUT+ Send      | B04       | Vcc + R          |
|                 | X5  | MIDI OUT+ Return    | B05       | TX + Buffer + R  |
| **MIDI IN+**    | M1  | MIDI IN+ Contact A  | B06       | D12/A11 + Relay  |
|                 | M2  | NC                  | B07       | NC               |
|                 | M3  | MIDI IN+ Contact B  | B08       | --               |
|                 | M4  | MIDI IN+ Anode      | B09       | --               |
|                 | M5  | MIDI IN+ Kathode    | B10       | Optocoupler + RX |

Obsolete

| Panel/Port      | Pin      | Cable  | Signal                       | Int. Bus      | Int. Port    | Pro Mini Pin |
| --------------- | -------- | ------ | ---------------------------- | ------------- | ------------ | ------------ |
| **GeekPort D**  | G1       |        | USB Power                    |               |              |              |
|                 | G2       |        | USB D+                       |               |              |              |
|                 | G3       |        | USB D-                       |               |              |              |
|                 | G4       |        | USB GND (?)                  |               |              |              |
|                 | G5       |        | I2C SDA                      |               |              |              |
|                 | G6       |        | I2C SCL                      |               |              |              |
|                 | G7       |        | Vcc                          |               |              |              |
|                 | G8       |        | Sensor A                     |               |              |              |
|                 | G9       |        | Sensor B                     |               |              |              |
|                 | G10      |        | Sensor C                     |               |              |              |
|                 | G11      |        | Sensor X                     |               |              |              |
|                 | G12      |        | Sensor Y                     |               |              |              |
|                 | G13      |        | Sensor Z                     |               |              |              |
|                 | G14      |        | GND                          |               |              |              |


## Parts

* Logic board
* U1: Arduino Pro Mini 328 5V [SparkFun](https://www.sparkfun.com/products/11113) [Switch-Science](https://www.switch-science.com/catalog/946/)
* U2: MAX7219CNG [SparkFun](https://www.sparkfun.com/products/9622) [Marutsu](http://www.marutsu.co.jp/pc/i/60116/)
* IC1: 74HC4051 [Kyohritsu](http://eleshop.jp/shop/g/gT11593/)
* IC2 and IC4: LTC1485CN8 x2 [Akizuki](http://akizukidenshi.com/catalog/g/gI-01869/)
* IC3: 74LS07N [Kyohritsu](http://eleshop.jp/shop/g/gT11678/)
* OK1: TLP552 or TLP2962 [Kyohritsu](http://eleshop.jp/shop/g/g44R13L/)
* T1: 2SC1815Y [Kyohritsu](http://eleshop.jp/shop/g/gA4B135/)
* D1 to D3: 1S1588 or similar [Kyohritsu](http://eleshop.jp/shop/g/g1CS13I/)
* LED1 and LED2: Green and Red LEDs
* C1: 0.1u
* C2 to C7: 0.01u x6
* R1: 22k
* R2: 10k
* R3: 3.3k
* R4, R8, and R9: 220
* R5 and R6: 330 x2
* R7 and R10: 120
* K1 and K2: G5V-2 DC5V [Kyohritsu](http://eleshop.jp/shop/g/g41713R/)
* CN1: JST PH 16p side [Kyohritsu](http://eleshop.jp/shop/g/g61L15C/)
* CN2: JST PH 10p side [Kyohritsu](http://eleshop.jp/shop/g/g61L146/)
* JP1: Pinheader 5p [Kyohritsu](http://eleshop.jp/shop/g/gEAT417/)
* JP2: Pinheader 2p [Kyohritsu](http://eleshop.jp/shop/g/gEAT417/)
* SV1: Harting 26p side [Kyohritsu](http://eleshop.jp/shop/g/g4A114X/)
* Case Takachi MX2-8-13BB [Kyohritsu](http://eleshop.jp/shop/g/g82731D/)
* SW: Nidech Copal-8A [Kyohritsu](http://eleshop.jp/shop/g/gD1G362/)
* SW: Miyama MS-402 [Kyohritsu](http://eleshop.jp/shop/g/g41W131/)
* VR: B 10k Supertech VR [Kyohritsu](http://eleshop.jp/shop/g/g4BP13G/)
* Knob
* LED: Kathode-common matrix LED LTP-305G [Akizuki](http://akizukidenshi.com/catalog/g/gI-07441/)
* LED: 3mm Green LED PY3407S [Akizuki](http://akizukidenshi.com/catalog/g/gI-03461/)
* Con: HR10A-7R-6S [Marutsu](http://www.marutsu.co.jp/pc/i/37647/)
* Con: HR10A-10R-12S [Marutsu](http://www.marutsu.co.jp/pc/i/37640/)
* Con: 4p mini pin jack Marushin MJ-079 x2 [Kyohritsu](http://eleshop.jp/shop/g/g6AR144/)
* Con: DC jack Marushin MJ-17 [Kyohritsu](http://eleshop.jp/shop/g/g3CU147/)
* Con: Harting 26p plug [Kyohritsu](http://eleshop.jp/shop/g/gC32361/) + [Kyohritsu](http://eleshop.jp/shop/g/gC32368/)
* Con: JST PH 16p plug [Kyohritsu](http://eleshop.jp/shop/g/g61K14H/)
* Con: JST PH 10p plug [Kyohritsu](http://eleshop.jp/shop/g/g61K14B/) 
* PH harness [Kyohritsu](http://eleshop.jp/shop/g/gEAO313/)
* Flat cable [Kyohritsu](http://eleshop.jp/shop/g/gA5G149/)



