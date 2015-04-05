# Pineapple II Nitrogen/0.0.0 Tech Doc

## Interface

| Panel/Port      | Pin       | Signal                       | Int. Bus            | Int. Port    | Micro Pin    |
| --------------- | --------  | ---------------------------- | ------------------- | ------------ | ------------ |
| **Power**       | P1        | Power (7V to 12V)            | (VDD)               | F1           |              |
|                 | P2        | GND                          | (GND)               | F2-22        |              |
| **Panel**       | LED       |                              | GEEK19              | F3           | D13~         |
|                 | Reset     |                              | GEEK20              | F5           |              |
| **XMIDI OUT**   | M1        | TX+                          | MIDI1               | B1           |              |
|                 | M2        | GND                          | (GND)               | B2           |              |
|                 | M3        | TX-                          | MIDI3               | B3           |              |
|                 | M4        | MIDI OUT SRC                 | MIDI4               | B4           |              |
|                 | M5        | MIDI OUT SNK                 | MIDI5               | B5           |              |
|                 | --        | TX                           | MIDI6               | B6           | D1           |
| **MIDI OUT 2**  | M6        | NC                           | (NC)                | --           |              |
|                 | M7        | GND                          | (GND)               | B7           |              |
|                 | M8        | NC                           | (NC)                | --           |              |
|                 | M9        | MIDI OUT 2 SRC               | MIDI9               | B9           |              |
|                 | M10       | MIDI OUT 2 SNK               | MIDI10              | B10          |              |
| **XMIDI IN**    | m1        | RX+                          | MIDI11              | B11          |              |
|                 | m2        | NC/GND                       | (GND)               | B12          |              |
|                 | m3        | RX-                          | MIDI13              | B13          |              |
|                 | m4        | MIDI IN SRC                  | MIDI14              | B14          | D12A11pd     |
|                 | m5        | MIDI IN SNK                  | MIDI15              | B15          |              |
|                 | --        | RX                           | MIDI16              | --           | D0           |
| **GeekPort II** | G1        | Power (7V to 12V)            | (VDD)               | F7           |              |
|                 | G2        | GND (1A max)                 | (GND)               | F2-22, U5    |              |
|                 | G3        | USB D+ OR Sensor X           | GEEK3/UNFD3         | F23, U3      | D10~A10      |
|                 | G4        | USB D- OR Sensor Y           | GEEK4/UNFD4         | F24, U2      | D9~A9        |
|                 | G5        | USB Power OR Sensor Z        | GEEK5/GEEK15/UNFD5  | F25, U1      | D4A6pd/D8A8  |
|                 | G6        | Sensor Detector              | GEEK6               | F26          | D6~A7        |
|                 | G7        | Vcc (5V)                     | (VCC)               | F9           |              |
|                 | G8        | Sensor A                     | GEEK8               | F11          | A0           |
|                 | G9        | Sensor B                     | GEEK9               | F13          | A1           |
|                 | G10       | Sensor C                     | GEEK10              | F15          | A2           |
|                 | G11       | Sensor D                     | GEEK11              | F17          | A3           |
|                 | G12       | I2C SDA OR Sensor E          | GEEK12/GEEK22/UNFD12| F19          | D2INT/A4     |
|                 | G13       | I2C SCL OR Sensor F          | GEEK13/GEEK23/UNFD13| F21          | D3~INT/A5    |
|                 | G14       | GND (1A max)                 | (GND)               | F2-22        |              |
| **Internal**    |           | MIDI IN Selector             | MIDI17              |              | D11~         |
|                 |           | I2C/Sensor Selector          | GEEK16              |              | D5~          |
|                 |           | USB Power/Sensor Selector    | GEEK17              |              | D7           |
|                 |           | 3.3V Out                     | GEEK18              |              |              |


analog: 10
pwm: 4



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



