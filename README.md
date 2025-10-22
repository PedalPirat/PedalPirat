# PedalPirat
Open Source Bike Plattform with ANT+, CAN, Bluetooth, Power Delivery and more to build the ultimative Smart Bike.


## Goals
- Replace proprietary batteries with a central Powerbank that can optionally be charged by a hub dynamo
- Make stuff work together vendor-independent (Shimano levers with SRAM AXS anyone?)
- Enhance Security with light control, Radars and Cameras using AI
- Integrate E-Bike Technology for Bio-Bikes like the Rohloff E-14
- Automate shifting and reporting cars that park on bike paths
- Fun (Heated Handlebar Tape ftw!)
- Data Fusion and Logging

## Integrations (for now)
- Rohloff E-14 (CAN)
- Shimano GRX Di2 wired Levers (CAN/Contact?)
- ANT+ (Quarq TyreWiz 2.0, Quarq DZero DUB, RockShox Reverb AXS, HR-Belt, maybe more?)

## Custom Hardware


## Don't reinvent the Wheel - Stuff that exists that can be integrated
### Hardware
#### [Mecha Comet](https://mecha.so/comet)
Linux Handheld with Touchscreen
#### [Bikone BB Torque Sensor (BSA)](https://www.bikone.com/bottombracket-torque-sensors/)
  - Power, Crank Position
  - Rohloff Hub gears should be shifted when under low power
  - Sensor would be ideal to determine bottom-out
  - Super hard / impossible to build a better solution DIY
#### [Forumslader Aheadlader V6](https://www.forumslader.de/aheadlader-v6/)
  - Powerbank with Hub Dynamo Charger
  - Delivers 5 and 12V
  - Can be charged externally
  - Power Lights, Phones/Bike Computers and Shifters

### Software
#### [Zephyr Project](https://github.com/zephyrproject-rtos/zephyr)
Real Time Operation System (RTOS) to programm the Microcontroller
#### [Pi Zero Bike Computer](https://github.com/hishizuka/pizero_bikecomputer)
