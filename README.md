# SlimeVr_18650_PCB_Version
This repository contains all the files for the PCB and the case designed with this PCB in mind. It also contains a detailed instructions on the assembly of the PCB and the case.

# Sections
-   Parts and Setup
-   PCB Related Information
- 	Case Related Information
- 	Assembly Information


# Parts and Setup
The parts used for this PCB can be found in the [official Components list](https://docs.slimevr.dev/diy/components-guide.html) and [Schematic](https://docs.slimevr.dev/diy/tracker-schematics.html).
This PCB is compatible with any 3.3V IMU which is smaller than the following maximum dimensions 28mm by 18mm.
The following parts are used in the PCB:
- D1 Mini.
- TP4056 Charge Board (Any connection).
- SPDT Slide Switch (SS12D00G3).
- Any 3.3V IMU under the max dimension 28mm by 18mm.
- 1N5817 Charge Diodes.
	Note for those not using it: Bridge the diode connections from the  positive output to the centre connections.
- (Optional) 180K Ohm resistor for battery sense.
- 3.7V Battery.

For those who who want a case and are using 18650 batteries for the tracker, there are 2 cases using this PCB found in the case files folder. (Additional information below)

# PCB Related Information
The Gerbal file for the PCB can be found in the PCB files folder along with an image of the schematic.
Additionally the project for this PCB can be found at the following links with or without the Aux connector:

PCB with Aux connection: https://easyeda.com/editor#id=22acdfc2081e44a4a4d110a4ab3e7e97

PCB without Aux connection: https://easyeda.com/editor#id=266cc1c912134b10b92cc5d7d849ca76

![Images/SchematicWithAux.png](Images/SchematicWithAux.png)
![Images/SchematicWithoutAux.png](Images/SchematicWithoutAux.png)

## PCB Ordering
The steps for ordering a PCB is very simple and straight forward as seen below.
- Step 1: Download the Gerbal files for the PCB of your choice.
- Step 2: Go to a PCB manufacturing site, for demonstration purposes JLCPCB will be used found here: https://jlcpcb.com/

![Images/JLCPCBSite.png](Images/JLCPCBSite.png)
- Step 3: Upload the Gerbal zip file.
- Step 4: Inspect the following settings are correct (see image) and adjust any of the cosmetic options to your preference.

![Images/JLCPCBSetting.png](Images/JLCPCBSetting.png)
- Step 5: Pay and wait for it to arrive.

# Case Related Information
This section referes to the cases designed for the PCB and found in the Case files folder. Both of the cases have been designed in SolidWorks.

## Case V:
![Images/Vertical18650Case3DRender.JPG](Images/Vertical18650Case3DRender.JPG)
The STL files for 3D printing this case can be found in the "Case Files / Vertical 18650 Battery Mount" folder along with the original files for easy modifications if you choose to do so.

## Case H:
![Images/Horizontal18650Case3DRender.JPG](Images/Horizontal18650Case3DRender.JPG)
The STL files for 3D printing this case can be found in the "Case Files / Horizontal 18650 Battery Mount" folder along with the original files for easy modifications if you choose to do so.

## Extension:
![Images/ExtensionRender.JPG](Images/ExtensionRender.JPG)
The STL files for 3D printing this case can be found in the "Case Files / Extension Case" folder along with the original files for easy modifications if you choose to do so.
Note: This extension case is compatible with all IMUs within 28mm by 18mm dimensions, if there are request for larger IMUs they would be added.

## 3D printing the case
The following demonstration for preparing each STL file will be shown in PrusaSlicer, ensure that the if there is supports used to match the images provided.
All of the case files can be printed at 0.2mm layer height.

- For the vertical battery mount case model use supports where the Aux cables exit the case.
- For the lid model, use supports for all overhanging material.

- For the horizontal battery mount case model use supports where the Aux cables exit the case and where the 18650 battery holder will be held.
- For the horizontal lid model, does not require any support material.

- The Extension models does not require any support material.

PCB Assembly Instructions
For the instructions below MPU6050 will be used, however any IMU using 3.3V input, match the first 4 pins and within 28mm by 18mm. Diodes are not required but the positive output must be bridged with a wire.
The battery sense resistor is optional, within this instructions a higher watt resistor will be used, 1/4 watt also works.

Below are all the electrical parts required to build a tracker, the parts within the marked area are for the extension tracker.
![Images/Build/AllParts.jpg](Images/Build/AllParts.jpg)

Step 1:

Solder the diodes in their spaces as shown in the picture (Grey strip pointing to the centre) and cut off the excess.

![Images/Build/Step1T.jpg](Images/Build/Step1T.jpg)
![Images/Build/Step1U.jpg](Images/Build/Step1U.jpg)

Step 2:

Solder the pins used for the TP4056 in the spaces as shown in the picture.

![Images/Build/Step2T.jpg](Images/Build/Step2T.jpg)
![Images/Build/Step2U.jpg](Images/Build/Step2U.jpg)

Step 3:

Solder the TP4056 on the pins from step 2 as shown in the picture and cut off the excess.

![Images/Build/Step3T.jpg](Images/Build/Step3T.jpg)

Step 4:

Solder the pins used for the D1 Mini in the spaces as shown in the picture.

![Images/Build/Step4T.jpg](Images/Build/Step4T.jpg)
![Images/Build/Step4U.jpg](Images/Build/Step4U.jpg)

Step 5:

Solder the pins used for the IMU in the spaces as shown in the picture only VCC, GND, SCL, SDA are required, the rest are optional.

![Images/Build/Step5T.jpg](Images/Build/Step5T.jpg)
![Images/Build/Step5U.jpg](Images/Build/Step5U.jpg)

Step 6 - OPTIONAL:

Solder the battery sense 180K Ohm resistor in the space shown in the picture and cut off the excess.

![Images/Build/Step6T.jpg](Images/Build/Step6T.jpg)
![Images/Build/Step6U.jpg](Images/Build/Step6U.jpg)

Step 7:

Solder the D1 Mini on the pins from step 4 as shown in the picture and cut off the excess.

![Images/Build/Step7T.jpg](Images/Build/Step7T.jpg)

Step 8:

Solder the IMU on the pins from step 5 as shown in the picture and cut off the excess. Ensure that the IMU remains parallel to the PCB, this could be achieved by using unused pin headers.

![Images/Build/Step8U.jpg](Images/Build/Step8U.jpg)

Step 9:

Cut one of the outside pins of the switch and then bend the remaining two in as shown in the picture.

![Images/Build/Step9U.jpg](Images/Build/Step9.jpg)

Step 10A - Horizontal 18650 case OPTION 1:

Solder a wire onto each the positive and negative terminals, ensure that the wire for the negative terminal is longer as it will be weaved into the case as shown in the picture, recommended length: Positive 40mm and Negative 90mm. You can coil the positive and negative wire after if you wish to do so. Cut off excess, leave enough wire for moving the PCB when it is attached.

![Images/Build/Step10A.jpg](Images/Build/Step10A.jpg)

Step 10B - Vertical 18650 case OPTION 2: 

Solder a wire onto each the positive and negative terminals, ensure that the wire for the positive terminal is longer so it could reach the PCB, recommended length: Positive 90mm and Negative 40mm. You can coil the positive and negative wire after if you wish to do so. Cut off excess, leave enough wire for moving the PCB when it is attached.

![Images/Build/Step10B.jpg](Images/Build/Step10B.jpg)

Step 11 - OPTIONAL EXTENSION:

Solder wires used for the extension tracker as shown in the picture, leave enough wire for movement between trackers. 

Note: Ensure that the ADO is bridged to the 3v3 pin for the extension IMU and ADO bridged to GND for the main IMU the or do so on the IMU side in step 14.

![Images/Build/Step11T.jpg](Images/Build/Step11T.jpg)
![Images/Build/Step11U.jpg](Images/Build/Step11U.jpg)

Step 12:

Note: If there is a extension tracker cables first move them into the slot in the case - the smaller one next to where the switch location.

Insert the PCB into the case, start with the moving TP4056 into its slot and ensure that the batteries wires don't disconnect once the PCB is completely flat inside move on to the next step. This is the same for both cases

![Images/Build/Step12.jpg](Images/Build/Step12.jpg)

Step 13:

Insert the switch prepared in step 9 into the slot in the case and adjust the pins to go into the PCB holes as shown in the picture. Once satisfied, solder the switch. Put on the corresponding tracker position lid to complete the main unit.

![Images/Build/Step13.jpg](Images/Build/Step13.jpg)

Step 14 - OPTIONAL EXTENSION: 

Using the wires from step 11, put it through the slot in the extension and continue to do so leaving enough room to solder the corresponding wires to the pins of the IMU as shown in the picture.

![Images/Build/Step14.jpg](Images/Build/Step14.jpg)

Step 15 - OPTIONAL EXTENSION:

Solder the corresponding wires to the pins of the IMU as shown in the picture - on the underside of the IMU.
Note: Ensure that the ADO is bridge to the 3v3 pin if it has not been done in step 11.

![Images/Build/Step15.jpg](Images/Build/Step15.jpg)

Step 16 - OPTIONAL EXTENSION:

Carefully position the IMU into the extension case, once positioned push it down onto the pins, gently pull cables when required, the IMU should be sitting inside as shown in the picture. Once it is in fully put on the extension lid on to finish the assembly.

![Images/Build/Step16.jpg](Images/Build/Step16.jpg)
