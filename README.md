# STM32 SOLAR GRANULAR MATRIX SOIL SENSOR

A Tensiometer is a device which measures soil water tension, unlike many soil sensors that only measures amount of water content in the soil. They measure soil water tension in units of negitive pressure, also known as 'tension', measured in terms of Kpas ( Kilo Pascals) or cbars (Centibars). As plants extract moisture from the soil pores, water content starts getting dried up, which increases the soil tension. Soil tension is measured by a hand held data logger that can be connected to tensiometer. 

In this project, a solar powered soil sensor is developed, which is used to power our system. The solar module is used to drive an ultra low power PMIC, which charges a Li Po battery. The system is powered by the Li Po battery, which provides uninterrupted power to the system, even during night time.


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

## Bill of materials (BOM) for the Irrometer reader
1. STM32L476 Nucleo board ( Controller )
2. Li Po battery 3.7 Volts
3. Watermark soil sensor
4. DS18B20 soil temperature sensor
5. LMC 555 (CMOS version of 555 IC)
6. Fixed resistor dividers: 390E and 150K
7. Pull up resistor across Discharge Output: 1K
8. Timing Capacitor: 100nF
9. Filter Capacitors across Sensor lines: 4.7u 16V - 2 numbers
10. Optional Protection diodes across sensor lines, against earth faults

## Hardware sections

The hardware consists of three major blocks

1. Power supply section
2. Controller section
3. Signal conditioning section

## Step 1: Design of the signal conditioning system

We need an interface for measuring the soil moisture sensor. The moisture content is measured by determining resistance of the soil sensor electrodes. The signal conditioner uses a LMC555 timer in relaxation oscillator mode to send an AC pulse signal to the electrodes. The AC resistance is suitably converted to a frequency output, that can be read by our STM32 data logger, which converts our resistance to Kilo pascals or centibars that can be displayed on a suitable display. 

