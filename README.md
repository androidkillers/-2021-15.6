Razer Blade 15.6 2021 144hz  Hackintosh

Introduction

Configuration for getting macOS monteery to run on a Razer Blade 15 2021 using OpenCore 0.7.6. If you would like to get started with creating a Hackintosh on your Razer Blade but have no experience, I would highly reccomend following Dortania's fantastic [Opencore Install guide][1] and then returning here for troubleshooting.



Specs

Key	Value
CPU	Intel Core i7-10750H
GPU	Intel UHD Graphics 630
Screen	15.6 144hz
Camera	HD webcam (720p)
RAM	16 DDR4 2,933MHz (2x8GB)
建兴 SSD 970 EVO (MacOS) +  (Windows)
Audio	ALC298
Wireless intel ax201
Pre-Install

You'll need to use a hardware programmer to unlock DVMT Options. Follow the instructions on https://git.io/JkuFs for how to mod your BIOS.

Quick Note: My serial number, MLB, and UUID have been removed from the config.plist. Please use CorpNewt's [GenSMBIOS][2] to create your own



Get iServices working

Start Fresh:

Log into iCloud.com
Click Find iPhone
Click All Devices
Select each of your failed attempts and click Remove from Account
Sign Out of iCloud.com
Sign Out of iCloud
Disconnect internet and Restart computer
Clean House - Open a Finder - Click on your User Name - Right click in window and select Show View Options - Select Show Library Folder. - Open Library folder and then Caches - Delete all files and folders beginning with: * com.apple.iCloudHelper * com.apple.imfoundation.IMRemoteURLConnectionAgent * com.apple.Message

- Navigate to Username/Library/Preferences 
- Delete all files and folders beginning with:
    * com.apple.iChat
    * com.apple.icloud
    * com.apple.ids.service
    * com.apple.imagent
    * com.apple.imessage
    * com.apple.imservice
- Clear Recycle Bin and Restart computer
What works

iGPU
Audio
Battery
Touchpad
Touchscreen (if supported)
USB Ports
CPU Freq
Intel Bluetooth（except for 隔空投送） / Wifi
