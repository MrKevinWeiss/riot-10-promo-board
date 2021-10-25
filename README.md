# RIOT's 10th year anniversary board and firmware

To celebrate the 10 year anniversary of RIOT OS, this open-source, open-hardware board will be published for all to enjoy.

## The Application

This board will act as a digital geocache to show off RIOT's low power and networking capabilities.
After some initial non-volatile configuration via the shell interface the digital cache can be placed in a hidden area, ideally bolted down.
People can search for them and upon locating them, press the button to display a time-sensitive web-link to show some funny message (Red-Green quote?).
The button presses will be logged via LoRaWAN messages to count how many people interacted with the geocache.
Messages will also be periodically sent to sync the RTC based geocache with the website display slots and well as monitor battery life.

## RIOT Modules

```
- gnrc_lorawan
- periph_eeprom
- periph_rtc
- periph_gpio
- shell
```

## Tools

- For PCB designed: KiCAD v5.1.10
- For enclosure and 3d design: FreeCAD
