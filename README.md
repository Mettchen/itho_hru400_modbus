# itho_hru400_modbus
For controlling the Itho Daalderop HRU 400 through modbus

This project is based on two solutions of getting the data through the modbus connection on the Itho Daalderop HRU 400.

Prerequisites:
- MAX485 or MAX3485. The MAX485 requires 5V, while the MAX3485 requires 3.3V.
- ESP32 or ESP8266
- Connector cables
- Powersupply for the ESP

# Solution 1 - ESP8266
Wire up the MAX with the ESP8266 in the way shown in this image: https://www.mischianti.org/wp-content/uploads/2022/09/esp8266-nodemcu-rs458-max3485-module-connection_bb.jpg
With these modifications: 
- R0 (red) -> RX
- DI (yellow) -> TX
- DE/RE (blue) -> G5 
NB! VCC should with MAX485 be connected to 5V externally.


# Solution 2 - ESP32
Same configuration as above, but with the 5V pin for VCC if using MAX485.
