# PedalPirat
Open Source Bike Plattform with ANT+, CAN, Bluetooth, AI Cameras and more to build the ultimative Smart Bike.
![PedalPirat](PedalPiratController.drawio.png)

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


### Main Controller / Extension for [Mecha Comet](https://developers.mecha.so/comet/extensions/io-breakout)
- nRF54H20
  - USB to connect with Comet
  - CAN to connect with Rear MCU, Rohloff
- u-blox MAX-M10S GPS
- Bosch BHI385 IMU

### Rear-Controller
- nRF54H20 with CAN to Front-Controller
- Connect / Control Rohloff E-14
- Connect to Bikone BB Torque Sensor
- Connect to rearlight
- 
### Input
- Brake Sensor Input
- Turn Signals
- Snapshot / Report
- Shift Up/Down
- Bike Computer Control
- Other/Joystick
### Turn Signals
- Models
  - Ergon-Endcap
  - Surly Moloko Extension
  - Rear Light
- LIN-Based

### Light Controller (for [LiteMove RX-E90](https://www.lite-move.com/product/rx-e90-high-low-beam/))
- Lumissil [IS32LT3183A](https://www.lumissil.com/applications/automotive/automotive-lighting/interior-lighting/ambient-lighting-&-footwell/is32lt3183a)
- Control High Beam
- On/Off

## Don't reinvent the Wheel - Stuff that exists that can be integrated
### Hardware
#### [Mecha Comet](https://mecha.so/comet)
Linux Handheld with Touchscreen
#### Bike Components
##### [Bikone BB Torque Sensor (BSA)](https://www.bikone.com/bottombracket-torque-sensors/)
  - Power, Crank Position
  - Rohloff Hub gears should be shifted when under low power
  - Sensor would be ideal to determine bottom-out
  - Super hard / impossible to build a better solution DIY
##### [Forumslader Aheadlader V6](https://www.forumslader.de/aheadlader-v6/)
  - Powerbank with Hub Dynamo Charger
  - Delivers 5 and 12V
  - Can be charged externally
  - Power Lights, Phones/Bike Computers and Shifters

##### [Rohloff E-14](https://www.rohloff.de/en/products/speedhub/e-14)

##### [Quarq TyreWiz 2.0](https://www.sram.com/de/service/models/wh-trwz-e1)

#### Electronic Components
##### ICs
- [Nordic Semi nRF54H20 MCU](https://www.nordicsemi.com/Products/nRF54H20)
- [Melexis LED Controller](https://www.melexis.com/en/products/smart-led-driver-ics)
- [Lumissil LIN Controller](https://www.lumissil.com/applications/automotive/automotive-lighting/interior-lighting/is32cs8978)
- [u-blox MAX-M10S GPS](https://www.u-blox.com/en/product/max-m10-series)
- [Bosch BHI385 Smart Sensor](https://www.bosch-sensortec.com/products/smart-sensor-systems/bhi385/)
- [Ti USB-PD Powerbank Eval Board](https://www.ti.com/tool/USB-PD-CHG-EVM-01)
- [MPS Powerbank Eval Board](https://www.monolithicpower.com/en/mezs7-1s-4spdpowerbank-reference-design)
- Rotary Sensor

##### Other
- [AI Camera](https://www.st.com/content/st_com/en/st-edge-ai-suite/case-studies/smart-rear-view-camera-running-on-batteries.html)

### Software
#### [Zephyr Project](https://github.com/zephyrproject-rtos/zephyr)
Real Time Operation System (RTOS) to programm the Microcontroller
#### [Pi Zero Bike Computer](https://github.com/hishizuka/pizero_bikecomputer)

## Protocols / Knowledge
- [ANT+](http://thisisant.com)
- [CAN](https://www.csselectronics.com/pages/can-bus-simple-intro-tutorial)
- [LIN](https://www.csselectronics.com/pages/lin-bus-protocol-intro-basics)
