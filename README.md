# Dual_WBO

## Development status: ##
- Hardware: working in progress, check hardware/V0.0.1 for actual status
- Software: not started yet

### Dual WBO controller based on: ### 
- Microchip AT90CAN128
- 2x Bosch CJ125 wideband lambda controller
- NXP TJA1051T high speed can transceiver (Rohm BD41041FJ-CE2 can be used instead)
- Analog Devices LTC2633 dual channel 10-bit I²C DAC
- Infineon TLE42754D LDO 5v and 450mA
- TI REF5050-Q1 5v and 10mA precision reference (0.05%) for TLS115
- Infineon TLS115B0EJ voltage tracker for analog part, provides 5v and 150mA
- ...

### Features: ### 
- supports **LSU4.9** probes only
- Automotive grade components
- Molex MX150 20-pin automotive sealed connector (348302001)
- 2x LSU 4.9 connector (TE 1813139-1)
- 4 layer PCB

### Inputs: ### 
- 2x LSU4.9 probes
- CAN high speed with 500kbit/s and extended IDs
- TTL input for activation the controller

### Outputs: ### 
- dual analog output, either as 0..4.096V for AFR 10..20 **OR** narrow band emulation
- CAN output (AEM X-Series protocol) for both channels
- CAN debug / diagnostic messages (pump current, battery voltage, heater power, ....)

### Suitable Bosch lambda probes: ###
|Bosch number  |Length overall|Comment|
|--------------|--------------|-------|
|0 258 017 025 |1000mm|Bosch motorsport part|
|0 258 017 012 |1060mm||
|0 281 004 184 |1000mm||
|0 281 004 150 |1215mm||
|0 258 017 126 |680mm|black, used by BMW after 09/2006 (1178 7561410)|
|0 258 017 029 |620mm|grey, used by BMW after 09/2006 (1178 7539124)|
|0 258 017 092 |950mm|black, used by BMW (1178 7540167)|
|0 258 017 038 |340mm|grey, used by BMW (11787537984)|
|...|||

### LSU4.9 probe pinout: ###
|Pin#|Color|Description|Symbol|
|----|-----|--------|-----------|
|1|red|Pump current APE|IP|
|2|yellow|Virtual ground IPN|VM|
|3|white|Heater voltage H-|Uh-|
|4|grey|Heater voltaget H+|Uh+|
|5|green|Trim Resistor RT|IA|
|6|black|Nernst voltage UN|RE|
