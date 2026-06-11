# Clone_of_Juma_PA150D
There are several Ham radio operators use  clone of Juma PA 150D linear amplifier. This repo helps them to upload the latest firmware along with the bootloader

/*** Note - These steps are for Windows 11  ****/

1) Download  MPLAB X IDE setup file ( v6.2.0 worked for me with the pickit I have )

2) Select only MPLAB IPE  and check box option "dsPIC DSC and 16 bit PIC 24"  when the installer asks

3) After installation , connect pickit and install missing dependent libraries  if any.

4) Open up the Amp , and connect a 6 pin JST connector to J19. It is very difficult to remove the LCD screen as it is directly soldered to the board. So I have soldered this pin in a 45 degree angle :-)

<img width="4080" height="3072" alt="IMG_20260608_172037718" src="https://github.com/user-attachments/assets/b8de9f15-7543-4e82-853d-f53c3fffe254" />


5) Before connecting the other end to Pickit , do some settings in MPLAB IPE as shown below
<img width="1431" height="797" alt="Tool_Photo_2" src="https://github.com/user-attachments/assets/0912ef53-0900-4377-8d58-421acc8bc8e8" />

<img width="1692" height="872" alt="Tool_Photo_3" src="https://github.com/user-attachments/assets/86e6faf2-f048-43b5-b780-2756b3cc3519" />

<img width="967" height="472" alt="Tool_Photo_4" src="https://github.com/user-attachments/assets/6b61fcdf-c6ae-4009-9421-df5dc385063f" />





6) Now try to connect other end of 6 pin connector to Pickit ( make sure the pin numbers are properly aligned. )  , and choose the below parameters

<img width="1417" height="637" alt="Tool_Photo_2a" src="https://github.com/user-attachments/assets/7d8795c1-f7f1-405d-b54b-1d1274a71fe6" />


7) Connect to pickit and see if it able to find the pic from the Amp. 

8) Connect 12 v to Amp , switch power ON in the Amp and hold the power button. Now try to click on the "Read" button in MPLAB IPE. If IPE reads the pic , then export the read .hex as a backup 

9) If "Read" is success , then browse and select "Merged_Juma_PA100.hex" ( attached as .hex.txt   , please rename to .hex ) in IPE

10) As we did for "Read" , power on and hold the button.

11) Click on "Program" , make sure that  the power button is pressed till the write completes.

This should show the log as below :

Connecting to MPLAB PICkit 3...

Currently loaded firmware on PICkit 3

Firmware Suite Version.....01.56.09

Firmware type..............dsPIC30F

Target voltage detected

Target device dsPIC30F6014A found.

Device Revision ID = 1041

Device Erased...

Programming...

The following memory area(s) will be programmed:

program memory: start address = 0x0, end address = 0x17fff

configuration memory

EEData memory

Programming/Verify complete

2026-06-08 16:56:51 +0530 - Programming complete

***   Release From Reset mode is enabled   ***

12) Once after successful "Program" , press "Disconnect" in tool and remove the Pickit connections to the 6 pin connector.

13) Power off and on the Amp , that should now be with updated firmware.

<img width="4080" height="3072" alt="IMG_20260608_180521922" src="https://github.com/user-attachments/assets/648fb1a0-544a-4350-ab51-bbe5c45f7f61" />


14) You may do the calibration as per the standard documentation.
