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

### ### If you have already running pi with new OS and SSh enabled, Then skip to 14th step.
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
8.	Download Putty and Install Putty
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


