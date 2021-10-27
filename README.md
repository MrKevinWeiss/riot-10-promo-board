# `r10t-gc`, RIOT's 10th year anniversary board

To celebrate the 10 year anniversary of RIOT OS, this open-source, open-hardware board will be published for all to enjoy.

## The Application

`r10t-gc` (`r10t` indicates RIOT's 10th anniversary and `gc` indicates geocache) will act as a digital geocache to show off RIOT's low power and networking capabilities.
After some initial non-volatile configuration via the shell interface the digital cache can be placed in a hidden area, ideally bolted down.
A tamper sensor can detect if `r10t-gc` is removed and notify the device monitoring software.
People can search for them and upon locating them, press the button to display a time-sensitive (or one-time-password) QR code pointing to a hint to the next node and a culturally specific meme.
Periodic LoRaWAN messages will be used to sync the time, report logged button presses (how many people found the device), report battery life, and tampering (either by lack of keep-alive or async tamper message).
As time between the hint server and `r10t-gc` will be synced, constant LoRa connection is not required in order to produce the QR code.

## Hardware Design

As this is a community project, the design will be highly modular.
This will allow each person to work on components such as MCU, LCD, power, have one board that brings each component together.
Modularity is also required in this day and age to handle the crazy chip shortages.

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
- For enclosure and 3d design: FreeCAD 0.19.2
