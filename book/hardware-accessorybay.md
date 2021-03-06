# Accessory Port

## Mechanical

The *Accessory Bay* is considered to be the area behind the gimbal under the Solo that does not interfere with the 3DR Gimbal. It is roughly 3" wide x 5.25" long x 4" deep. 

Maximum payload of the system is 700g, the 3DR Gimbal + GoPro weigh approximately 390g, leaving 310g for accessories that are meant to be used with the 3DR Gimbal.

The Accessory Bay hole pattern is M2 screws in a 1.655" x 1.15" rectangular pattern. Ensure that the rectangle is not intersected by the path of the gimbal.

![Hole Pattern](https://cloud.githubusercontent.com/assets/2678765/10023369/612fcd74-6117-11e5-961d-6a9d4ffeeb35.png)

## Electrical

The mating connector part number is [JAE SJ038252](https://jae-connectors.com/en/pdf_download_exec.cfm?param=SJ038252.pdf) and can be purchased on [Mouser](http://www.mouser.com/ProductDetail/JAE-Electronics/TX24-30R-6ST-N1E/?qs=%2fha2pyFaduiqgba8kBa6TtehVWNIeLFx3lhQ48lSxiSCqywLxSV2eg%3d%3d).

The pinout of the Accessory Port is:

Pin | Description | Pin | Description
--- | --- | --- | ---
1. | USB D- | 16. | USB GND
2. | USB D+ | 17. | +5V
3. | N/C | 18. | N/C
4. | N/C | 19. | +5V
5. | N/C | 20. | N/C
6. | N/C | 21. | GND
7. | N/C | 22. | N/C
8. | N/C | 23. | BUS ID
9. | SER5 TX (DEBUG) | 24. | SER5 RX (DEBUG)
10. | SER2RT | 25. | SER2CT
11. | SER2Tx | 26. | SER2Rx
12. | CANH1 | 27. | 3DRID (USB ID)
13. | CANL1 | 28. | GND
14. | GND | 29. | GND
15. | BATT (14.0-16.8V, 1.5A max) | 30. | BATT (14.0-16.8V, 1.5A max)

## Communication Protocol

The two primary interfaces to the *Accessory Bay* will be the CAN bus for direct integration with the flight controller and the USB port for higher-level interactions with Smart shots, DroneKit, and interactions with the Controller.

CAN - Uses the [UAVCAN](http://uavcan.org/UAVCAN) protocol and interfaces directly with the Pixhawk. 

USB - USB Host device to the iMX6 co-processor.

## Accessory Breakout Board

An open source reference design for a breakout board can be found [here](https://github.com/3drobotics/Pixhawk_OS_Hardware/tree/master/Accessory_Breakout_X1).
