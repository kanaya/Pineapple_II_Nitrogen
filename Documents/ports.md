# Pineapple II Ports

## External Ports

### Power Port

#### Type

EIAJ Class-3 (DC 6.3V to 10.5V, 2A)

#### Pinout

| Pin num. | Function |
| -------- | -------- |
| 1        | V+       |
| 2        | GND      |

### GeekPort II

#### Type

Half-pitch 14-pin Amphenol Connector

#### Pinout

| Pin num. | Function (1) | Function (2) |
| -------- | ------------ | ------------ |
| 1        | V+           | V+           |
| 2        | GND          | GND          |
| 3        | USB D+       | USB D+       |
| 4        | USB D-       | USB D-       |
| 5        | USB Power    | USB Power    |
| 6        | Cable detect | Cable detect |
| 7        | Vcc          | Drive 0      |
| 8        | Sensor A     | Drive 1      |
| 9        | Sensor B     | Drive 2      |
| 10       | Sensor C     | Drive 3      |
| 11       | Sensor D     | Drive 4      |
| 12       | I2C SDA      | Drive 5      |
| 13       | I2C SCL      | Drive 6      |
| 14       | GND          | Drive 7      |

### XMIDI OutThru

#### Type

DIN 5-pin

#### Pinout

| Pin num. | Function         |
| -------- | ---------------- |
| 1        | MIDI THRU Send   |
| 2        | GND              |
| 3        | MIDI THRU Return |
| 4        | MIDI OUT Send    |
| 5        | MIDI OUT Return  |

### XMIDI InOut

#### Type

DIN 5-pin

#### Pinout

| Pin num. | Function          |
| -------- | ----------------- |
| 1        | MIDI OUT 2 Send   |
| 2        | GND               |
| 3        | MIDI OUT 2 Return |
| 4        | MIDI IN Anode     |
| 5        | MIDI IN Kathode   |

### HydroPort

#### Type

HR-10A 6p

#### Pinout

| Pin num. | Function     | Corresponding GeekPort II Pin |
| -------- | ------------ | ----------------------------- |
| 1        | Vcc          | Vcc                           |
| 2        | GND          | GND                           |
| 3        | Cable Detect | Cable Detect                  |
| 4        | Sensor A     | Sensor A                      |
| 5        | I2C SDA      | I2S SDA                       |
| 6        | I2C SCL      | I2C SCL                       |

### ZeroVoltagePort

#### Type

HR-10A 4p

#### Pinout

| Pin num. | Function     |
| -------- | ------------ |
| 1        | Vcc R220     |
| 2        | GND          |
| 3        | ZV Contact A |
| 4        | ZV Contact B |

## Internal Ports

### COM

#### Type

JST PH connector (2mm-pitch)

#### Pinout

| Pin num. | Function |
| -------- | -------- |
| 1        | TX+      |
| 2        | TX-      |
| 3        | RX+      |
| 4        | RX-      |

### Actuator Port

#### Type

2x3 Pinheader

#### Pinout

| Pin num. | Function |
| -------- | -------- |
| 1        | GPIO0    |
| 2        | GPIO1    |
| 3        | GPIO2    |
| 4        | SPI MISO |
| 5        | SPI MOSI |
| 6        | SPI SLCK |

### LED Port

#### Type

1x4 Pinheader

#### Pinout

| Pin num. | Function    |
| -------- | ----------- |
| 1        | TXA (GPIO0) |
| 2        | TXK         |
| 3        | RXA (GPIO1) |
| 4        | RXK         |

### Front Port

#### Type

2x4 Pinheader

#### Pinout

| Pin num. | Function |
| -------- | -------- |
| 1        | V+       |
| 2        | GND      |
| 3        | V+       |
| 4        | GND      |
| 5        | RST      |
| 6        | GND      |
| 7        | LEDA     |
| 8        | LEDK     |

### Back Port

#### Type

10-pin Harting (MIL) connector

#### Pinout

| Pin num. | Function                              |
| -------- | ------------------------------------- |
| 1        | XMIDI OutThru RX Send (THRU Send)     |
| 2        | GND                                   |
| 3        | XMIDI OutThru RX Return (THRU Return) |
| 4        | XMIDI OutThru TX Send (OUT Send)      |
| 5        | XMIDI OutThru TX Return (OUT Return)  |
| 6        | XMIDI InOut TX Send (OUT2 Send)       |
| 7        | GND                                   |
| 8        | XMIDI InOut TX Return (OUT2 Return)   |
| 9        | XMIDI InOut RX Anode (IN Anode)       |
| 10       | XMIDI InOut RX Kathode (IN Kathode)   |


