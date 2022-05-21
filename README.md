# Solar_BLE_Tensiometer

A Tensiometer is a device which measures soil water tension, unlike many soil sensors that only measures amount of water content in the soil. They measure soil water tension in units of negitive pressure, also known as 'tension', measured in terms of Kpas ( Kilo Pascals) or cbars (Centibars). As plants extract moisture from the soil pores, water content starts getting dried up, which increases the soil tension. Soil tension is measured by a hand held data logger that can be connected to tensiometer.

This project is a low cost implementation of a datalogger that is used to measure soil moisture in terms of SWT (Soil water tension). The project is planned in terms of 4 different versions. Even though the circuit can be used for different soil sensors in general, it is more targeted towards Granular Watermark Sensors 200L

# Version 1
Simple Soil moisture Datalogger using a simple resistive divider arrangement

# Version 2
Single Soil moisture Datalogger using 555 Timer circuit

# Version 3
Multiple Soil moisture Datalogger using 555 timers and Multiplexers

# Version 4
BLE Soil moisture Datalogger

# Version 5
Solar powered BLE Soil moisture sensor

------------------------------------------------------------------------------------------------------------------------------------------------------------

## Simple Soil Datalogger using resistive divider
### Objective: Design a soil moisture datalogger for measuring a watermark granular sensor using a simple resistive divider 

#### What is a watermark sensor??
Understanding GMS (Granular Matrix sensors)
A Granular matrix sensor is a type of sensor that contains a pair of corrison resistant electrodes that are embedded in an granular matrix. Current is applied to 
the sensors to obtain the resistance value. This resistance is co-related to centibars / Kilopascals of the soil water tension.
![download](https://user-images.githubusercontent.com/26503600/169240719-eefdddde-653b-4b35-84c0-3f19a839385d.jpg)
#### Watermark sensor 200ss

## Devices used in the project
1. Watermark sensor
2. 7.87K fixed resistor
3. Arduino
4. Connecting wires

## Background / Theory 
This version of the project uses a fixed resistor of value 7.87K, that is used in series with the watermark sensor, whose resistance is to be measured. The circuit
uses digital power input from an arduino/ or a separate battery can be used. After the resistance is calculated, the the resistance value is calibrated to reflect
the soil water tension in Kilo pascals or centibars. This analog input is read by the arduino, which can be read a suitable display / screen


![Resistive_divider](https://user-images.githubusercontent.com/26503600/169237215-787583b4-245c-4cd4-b6ff-db79e823348d.png)




