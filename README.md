## Introduction
The aim of the project was to create a device for audiovisual shows using lasers. The devices, held in both hands of the showman, generate laser beams from both ends. By turning the beam on and off using the buttons on the housing, you can create the illusion of beam control. As picture below.
<img width="1000" height="666" alt="image" src="https://github.com/user-attachments/assets/0028cb9a-6fd3-4958-909a-810c31c1a1aa" />

## Description of operation
The device consists of two 200mW green laser modules. The modules are attached to the 3D printed base using cable ties. The entire assembly is screwed with thermoplastic screws. For the printed circuit board. The connection between the modules is made of wire. To prevent the lasers from sliding inside, the space between them is secured with hot glue.
The entire device is powered by a single Li-ion cell, size 18650. For assembly, use the version with attached plates. The plates should be soldered to the PCB after mounting it in the lower part of the housing.
The IP5306 system was used to charge the battery, the battery is charged via the USB C port. Resistors R12, R13 force a higher current on the charger (up to 1.5A). D1 protects against overvoltages on the USB port. Basically, a unidirectional diode should be used here. 
The application of the IP5306 system is typical and taken from the catalog note. 
In order to protect the cells against excessive discharge, U1 and U5 systems were used. They are needed because the laser drivers are powered directly from the battery. 
Two linear current sources, CN5711 LED drivers, were used to control the lasers, mainly due to the large size of the housing, easy accessibility, and a small number of external components. The current is regulated using mounting potentiometers in the range of 100-225mA

The button control logic was made on semiconductor diodes. Pressing the middle button turns on both lasers at once, while the outermost buttons turn on the corresponding lasers.
The SW1 button allows you to display the battery charge status. The device does not have an additional switch, which is a big disadvantage. Because this may result in the lasers being accidentally turned on.
The entire diagram can be seen in the image below.

<img width="1121" height="791" alt="image" src="https://github.com/user-attachments/assets/62caba90-e972-47fd-9d08-13a62bda25ad" />



## Mechanical Info

The device housing consists of two halves, fastened with M3x22mm screws. The length of the screws is slightly unusual, but they are available, e.g. 1570366 BOSSARD
In the lower part of the housing there are places for M3 flat nuts, for example 1088998 BOSSARD
the printed circuit board is screwed to the lower part using screws 3205122 BOSSARD

The disadvantage of this solution is the lack of elements that hold both shelves relative to each other, which may cause them to move and block the button levers.

The buttons are placed on the button levers and secured with glue. Openings in the housing allow access to the potentiators to regulate the laser current. The gap at the bottom allows you to display the battery charge status
## Design flaws


Things that didn't work very well. 

1. The 18650 battery is way too big. 
2. The buttons used in the project work very poorly and have low durability, so they are not suitable for such an application.
3. The mounting of the laser diodes does not allow for their easy adjustment, there will be problems with aligning both laser beams.
4. The casing can tilt and block the buttons.
5. A large number of elements needed for assembly.
6. The shape of the housing is not optimized for 3D printing
7. Inability to turn off the device.
