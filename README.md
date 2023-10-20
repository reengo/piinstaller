# piinstaller
configurable installer for Microcomputer

### Basic Installation:

1. Download [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
2. Install Raspberry Pi Imager
3. Insert a 128gb Micro SD Card on your computer and take note of the volume
4. Create and install a Raspberry Pi Instance on the volume
   - choose the latest OS version
   - choose the volume for the 128GB Micro SD Card to install to
   - write and remove from slot when finished
5. Attach the SD Card to Raspberry Pi and power it using a 15W USB-C power supply.
6. Complete installation wizard

### LCD Attachment

1. Connect the Micro SD Card on a computer and edit config.txt
2. Add the following values

hdmi_group=2
hdmi_mode=87
hdmi_cvt 800 480 60 6 0 0 0
hdmi_drive=1

#write the following on 1 line
dtoverlay=ads7846,cs=1,penirq=25,penirq_pull=2,speed=50000,keep_vref_on=0,swapxy=0,pmax=255,xohms=150,xmin=200,xmax=3900,ymin=200,ymax=3900

3. Save file and eject Micro SD Card
4. insert the micro sd card to raspberry pi

### Webservice Installation

--Instructions for nodejs express installation over raspberry pi apache--

### MicroService installation

--Instructions for pulling sub module api--

### Arduino Interface Installation

--Instructions for establishing serial connection to arduino board--

### GUI Installation

--Instructions Keypad and notification GUI--

