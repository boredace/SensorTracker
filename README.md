# SensorTracker

## Overview
SensorTracker is a simple C program used to track inventory of the sensors and their capabilities. The core of the program are three files storing information about sensor models, what they measure and the inventory at hand. 

The program is useful for hardware engineers working on various microcontroller projects in their lab to keep track of the sensors they have in their posession. In the future the program can be enhanced to include additional information such as which project / prototype device each sensor is located in.

## Data files
There are three data files used to store sensor information. They are located in the ```/datafiles``` folder.

### sensorts.txt

This files is a csv format file storing all the types of sensors we can possibly have in our inventory and the types of measurements they are capable of collecting. The list of measurement types is in the third column and contacts "id" pointers to entries in the ```measurements.txt``` file.

### measurements.txt

This file is also csv formatted file which stores all the types of possible measurements a sensor is capable of measuring. The Ids are references from the ```sensors.txt``` file

### inventory.txt

This file in a csv format is used to store all individual sensors in our posession and some basic information about them (when it was acquired and how much we paid for it).


## Program Functionality Overview

The program is a Windows executable file launched from a Command Line. 

### Main Menu

Upon start the program displays menu of commands.

```
SensorTracked v0.1

There are 362 sensors of 29 types in the inventory out of 45 types defined.

MAIN MENU:
1. Display inventory of all sensors
2. Display inventory of sensors by type
3. Add sensor
4. Manage Sensor and Measurement Types
0. Exit

Enter Command: _
```

### Display all sensors

Selectng this option will display all sensors defined in the ```inventory.txt``` file along with some basic information. The screen will display 20 sensors at a time and allow to go to previous/next screen as needed.

```
SensorTracker 0.1

SENSOR INVENTORY (All Senspors):

ID  TYPE          ACQUIRED ON     PRICE
1   PMS7003       2023-11-03      $14.99
2   ADC Voltage   2023-12-15      $5.75
3   PMS7003       2023-11-03      $14.99
4   TMP100        2024-07-24      $29.99
5   SCD40         2024-10-22      $13.888

Total of 5 sensors of 4 types.

Enter sensor ID for more details or (P)revious, (N)ext, E(x)it

Enter Command: _
```

To be continued....



# Assignment 1 (2024-10-22)

Create overall project structure with main menu and watch this video how to read data from a file in c (https://www.youtube.com/watch?v=X1Fq59EQaXo). Try to read values from the sensors.txt file (dont worry about formatting for now)
