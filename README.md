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
5. configure pi to run on cli on boot.
6. set time and date

sudo timedatectl status
sudo timedatectl set-time “2023-10-20 16:33:56” 


### Webservice Installation

1. update apt-get

sudo apt-get update

4. install apache

sudo apt-get install apache2 -y

5. check IP

hostname -I

6. take note of IP and run on a different computer on a browser and confirm apache installation


### MicroService installation

1. clone api

mkdir /var/www/dspencer
cd /var/www/dspencer
git clone http://<pat>@github.com/pragmanila/papi.git .

2. configure api

cp .env.example .env
yarn

3. install forever

yarn add forever -g

4. run api using forever

forever --uid dspencer-api start server.js 

### Arduino Interface Installation

--Instructions for establishing serial connection to arduino board--

### GUI Installation

--Instructions Keypad and notification GUI--

