# ESPHome-modbus-solar-inverter-Sunways-2

## Description:
This manual describes how to connect the device to Home Assistant via Modbus protocol using ESP8266 and RS485/TTL converter.
In this case it is about connecting a Solar Inverter Sunways.

This is a fork of repo: [Source ropository](https://github.com/budisek/ESPHome-modbus-solar-inverter-Sunways)

## Info:
- shielded cable recommended, otherwise the error "Modbus CRC Check Failed!" may appear in the log.
- Sunways modbus datasheet: [Interter Sunways](https://github.com/budisek/ESPHome-modbus-solar-inverter-Sunways/files/11507484/hybrid_inverter_modbus_rtu_protocol_en0332.pdf)
- Sunways User manual: [User Manual EN.pdf](https://github.com/budisek/ESPHome-modbus-solar-inverter-Sunways/files/11507661/STH.4.12KTL-HT.User.Manual.EN.pdf)
- you need to find out what the Inverter modbus address is - default is 247
- you also need to find out the serial port speed - default 9600
- in ESPHome use the sensor class only for addresses that are read-only
- for addresses that are read/write use the "number" class (you can then change their values in lovelace)
- for each register you want to have in HA you have to create a separate sensor in ESPHome
- you can write the address to the sensor in decimal or hex

## Components:
- ESP8266 (NodeMCU, Wemos D1...)
- RS485/TTL converter: [SHOP](https://www.laskakit.cz/prevodnik-uart-na-rs-485--max485/) 

## Lovelace:
<img width="375" alt="image" src="https://github.com/budisek/ESPHome-modbus-solar-inverter-Sunways/assets/35574450/77d7a180-340d-4570-b3bd-0cc1a9412778">

<img width="375" alt="image" src="https://github.com/budisek/ESPHome-modbus-solar-inverter-Sunways/assets/35574450/7fc45319-5bcd-4c9d-bfd0-57bfbc785f15">

