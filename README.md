# Solar_BLE_Tensiometer

A Tensiometer is a device which measures soil water tension, unlike many soil sensors that only measures amount of water content in the soil. They measure soil water tension in units of negitive pressure, also known as 'tension', measured in terms of Kpas ( Kilo Pascals) or cbars (Centibars). As plants extract moisture from the soil pores, water content starts getting dried up, which increases the soil tension. Soil tension is measured by a hand held data logger that can be connected to tensiometer.

This project is a low cost implementation of a datalogger that is used to measure soil moisture in terms of SWT (Soil water tension). The project is planned in terms of 4 different versions. Even though the circuit can be used for different soil sensors in general, it is more targeted towards Granular Watermark Sensors 200L

# Version 1
Single Soil moisture Datalogger using 555 Timer circuit

# Version 2
Multiple Soil moisture Datalogger using 555 timers and Multiplexers

# Version 3
Wireless sensing using BLE (BLE Soil moisture sensor)

# Version 4
Solar powered BLE Soil moisture sensor

------------------------------------------------------------------------------------------------------------------------------------------------------------

### Objective: Design a soil moisture datalogger for measuring a watermark granular sensor / Tensiometer

## Development flow of the project
1. Getting the background of the project
2. Project requirements
3. Knowing the sensor
4. Bill of materials (BOM) for the project
5. Preparation of hardware prototype
6. Condition the sensor for testing
7. Test results
8. Designing the hardware layouts / board
9. Future works

## Background / Theory 
Granular matrix sensor is a type of resistive soil moisture sensor, that uses a granular matrix, embedded within the sensor, which is used for precision farming and irrigation scheduling. One such GMS (Granular matrix sensor) sensor is the watermark sensor, that is manufactured by Irrometer. The watermark soil sensor measures the electrical resistance, inside of a granular matrix to determine soil water tension. Once the resistance is known, the value is calibrated to soil water tension via a series of equations or referencing look-up tables. 
In this regard, we need to design a reader module, that can read the sensor data (resistance) and can log the data onto a display screen /serial monitar of a MCU.

![watermark-sensor-500x500](https://user-images.githubusercontent.com/26503600/169804278-26a79443-f2f1-4aa2-b1e7-c592f000f05c.jpg)


### Features of the Watermark sensor

1. 0-200 Centibar range
2. Stainless steel enclosure
3. Fully solid state
4. Will not dissolve in soil
5. Not affected by freezing temperatures
6. Internal compensation for commonly found salinity levels
7. Inexpensive
8. Easy to use
9. No maintenance

For additional details on the sensor, navigate on the given link, https://www.irrometer.com/pdf/sensors/403%20WATERMARK%20Sensor-WEB.pdf





