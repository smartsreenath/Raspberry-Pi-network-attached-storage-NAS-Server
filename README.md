<p align="center">
  <img 
    width=50%
    height=50%
    src="https://i.imgur.com/b04QAsB.png"
  >
</p>

# Raspberry Pi network-attached storage (NAS) Server—1st  Part
### Raspberry Pi VNC (Remote Access Software)



![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)![Raspberry Pi](https://img.shields.io/badge/-RaspberryPi-C51A4A?style=for-the-badge&logo=Raspberry-Pi)![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)![Mac OS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)![IOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=ios&logoColor=white)![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)

This Tutorial is a Part of RPI NAS Server. If you have external monitor skip the 1st part

What is the use of VNC?
VNC stands for Virtual Network Computing. It is a cross-platform screen sharing system that was created to remotely control another computer. This means that a computer's screen, keyboard, and mouse can be used from a distance by a remote user from a secondary device as though they were sitting right in front of it.

If you do not have external display this will help you remotely view the pi screen in pc or phone. 

###  If you have already running pi with new OS and SSh enabled, Then skip to 14th step.
1. 	Preparing Your SD Card
    -  Format Sd card using [SD Card Formatter](https://www.sdcard.org/downloads/formatter/) (click for Link)
2.	Flash the Raspberry Pi OS image to our SD card using Raspberry pi imager
3.	Click advance settings in Raspberry pi Imager and select ssh. You can also add new ssh password (default is raspberry)
    - If you do not have external display this will help you to install VNC and there by remotely control raspberry pi

![This is an image](https://i.imgur.com/PbAb9RH.jpg)
![This is an image](https://i.imgur.com/GrOovtm.jpg)

4.	You can also enter the SSID and password of your Wi-Fi (Skip these steps if you are using Ethernet)
5.	When it is complete, plug the SD card into your Pi
6.	Boot Raspberry Pi
7.	Download and Open [Wireless network watcher](https://www.nirsoft.net/utils/wireless_network_watcher.html) and find the ip address of pi (click for the download link)
8.	Download Putty and Install [Putty](https://www.putty.org/) (Click for the Link)
    - Open putty, select ssh, then enter the IP address and click open
    - IF asking any permission click accept and Enter
9.	Enter username: pi
    - Password: ***** (enter the password given during flashing raspberry pi using raspberry pi imager) (default password is “ raspberry ”)

10.	First you need update the OS. Type the below commands on putty
```sh
sudo apt update
```
```sh
sudo apt full-upgrade
```
11.	Type “Y” for yes
12.	Reboot PI, Type
```sh
sudo reboot now
```
13.	Reconnect to Putty (type ssh username and password)
14.	Next we are going to Install VNC in Raspberry Pi (Skip If you have display)
```sh
sudo raspi-config
```
15. Select 3rd option “Interfacing option”

![This is an image](https://i.imgur.com/s8XrLxM.jpg)

16.	Select “VNC”
	
![This is an image](https://i.imgur.com/ALzZnOU.jpg)

17.	Then Select OK
18.	Select finish and press enter
19.	Reboot Pi, Type
```sh
sudo reboot now
```
 20. After reboot, Download [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) and Install In your PC or any devices
 
![This is an image](https://i.imgur.com/k8l8K3M.jpg)

- Enter the IP Address of raspberry pi
- Type SSH username and password.

# Raspberry Pi network-attached storage (NAS) Server—2nd  Part
### Raspberry Pi SSD BOOT  



![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white)![Raspberry Pi](https://img.shields.io/badge/-RaspberryPi-C51A4A?style=for-the-badge&logo=Raspberry-Pi)![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)![Mac OS](https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0)![IOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=ios&logoColor=white)![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)

This Tutorial is a Part of RPI NAS Server. If you do not want ssd boot and  prefer old sd boot, skip this tutorial.

### Why do we need SSD BOOT ?
 Raspberry Pi boots up and stores all of its programs on a microSD memory card by default, which has a maximum theoretical bandwidth of 50 MBps on the Raspberry Pi 4 and just 25 MBps on prior models. In real-life, even the best microSD cards for Raspberry Pi get no faster than about 38 MBps in sequential writes.  Using an external SSD as your main storage drive could speed things up significantly.
  - Faster Boot Time
  - Longevity
 
### What are the things we need for SSD boot?
  - New OS update
  - New firmware update
  - New Bootloader
  - Compatible USB Adapters 
   Contains a huge list of compatible USB Adapters for this Project by James A. Chambers
   https://jamesachambers.com/raspberry-pi-4-usb-boot-config-guide-for-ssd-flash-drives/
  
### Before starting, we need external monitor / VNC remote desktop access or SSH access to the Raspberry Pi.
Tutorail link for VNC and SSH https://github.com/smartsreenath/Raspberry-Pi-VNC-Install
 
1. Prepairing SD Card: 
   - If you have already running pi with new OS and SSh enabled, skip these. Otherwise follow steps from this tutorial.
   - https://github.com/smartsreenath/Raspberry-Pi-VNC-Install (contains sd card setup, SSh setup and VNC install)
  
2. Prepairing SSD
   - Format SSD  in PC
3.	Download Putty and Install [Putty](https://www.putty.org/) (Click for the Link)
    - Open putty, select ssh, then enter the IP address and click open
    - IF asking any permission click accept and Enter
4.	Enter username: pi
    - Password: ***** (enter the password given during flashing raspberry pi using raspberry pi imager) (default password is “ raspberry ”)

5.	First you need update the OS. Type the below commands on putty
```sh
sudo apt update
```
```sh
sudo apt full-upgrade
```
6.	Type “Y” for yes
7.	Reboot PI, Type
```sh
sudo reboot now
```
6. Connect SSD and Boot the PI
7. 	When you’re back on your desktop, go to your menu, then accessories and then SD Card Copier. This will open a simple window with a dropdown list. Select your SD card as the “from” target and your SSD as your “to” target. Then click on Start and Yes to continue. This will partition your SSD and copy the contents of your SD card to each partition.

![This is an image](https://i.imgur.com/xuNmnhN.jpg)

8. It will take some time.
9. Now we  have to tell the Pi to boot from the SSD instead of the SD card
10.	For that we need new bootloader for pi
11.	Open up a new terminal window and enter the following command
```sh
sudo rpi-eeprom-update -d -a
```
12.	Next, open up the configuration tool, type
```sh
sudo raspi-config
```
13.	Go to 6 “Advanced Options”  

![This is an image](https://i.imgur.com/fpiWU3b.jpg)

14. Then A7 “Bootloader Version”

![This is an image](https://i.imgur.com/x7ghiE8.jpg)

15.	Select the first option E1 Latest Use the latest version boot ROM software

![This is an image](https://i.imgur.com/ObLJyMZ.jpg)

16.	Then select “Ok”
17.	Then “No” (so that it doesn’t revert to defaults)
	
![This is an image](https://i.imgur.com/JTNhFB4.jpg)

18.	Then Click “OK” for BOOT ROM not reset to defaults 

![This is an image](https://i.imgur.com/kiLcBXz.jpg)

19.	Go back to 6 “Advanced Options”

![This is an image](https://i.imgur.com/fpiWU3b.jpg)

20.	Select A6 “Boot Order”

![This is an image](https://i.imgur.com/TtPRjXb.jpg)

21.	Select the second option B2 “USB Boot Boot from USB if available, otherwise boot from SD card”

![This is an image](https://i.imgur.com/9JFYpDy.jpg)

22.	Then “Finish” and then select “No” when asked if you would like to reboot
23.	Shutdown the pi
24.	Remove power source
25.	Remove SD Card
26.	Boot the pi ..

### TEST SSD SPEED
   - Quick and basic write test by opening up our terminal
```sh
dd if=/dev/zero of=./speedTestFile bs=20M count=5 oflag=direct
```
  - Reading the same file with the following command
```sh
dd if=./speedTestFile of=/dev/zero bs=20M count=5 oflag=dsync
```


