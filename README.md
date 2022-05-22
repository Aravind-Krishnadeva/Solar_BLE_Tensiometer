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
This version of the project uses a fixed resistor of value 7.87K, that is used in series with the watermark sensor, whose resistance is to be measured. The circuit
uses digital power input from an arduino/ or a separate battery can be used. After the resistance is calculated, the the resistance value is calibrated to reflect
the soil water tension in Kilo pascals or centibars. This analog input is read by the arduino, which can be read a suitable display / screen




