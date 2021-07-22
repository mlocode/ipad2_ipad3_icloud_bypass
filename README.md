# ipad2_ipad3_icloud_bypass
How To Remove bypass iCloud Lock in iPad2 and iPad3 with iOS 8.x.x

# Method 1 (only for 4G Devices)
Remove Resistor R1024 and Recover via iTunes


# Method 2 (for Wifi-Model and Wifi/4G Model)
Bypass via Arduino + USB Host Shield which is mainly the Tutorial from Apple Tech 752
Apple Tech 752 (https://www.youtube.com/watch?v=oMuprT7YCFo&t=11s)

## Parts 
1) Buy Arduino Uno LINK
2) Buy USBHost Shield for Arduino LINK
3) LED and 220Ohm Resitor (for Bypass Status)

## Prequisites
1) Download Arduino IDE
2) Install USBHost Library
3) Patch USB Library
> cd path/to/Arduino/libraries

> git clone https://github.com/felis/USB_Host_Shield_2.0

> cd USB_Host_Shield_2.0

> git checkout cd87628af4a693eeafe1bf04486cf86ba01d29b8

> git apply path/to/usb_host_library.patch

4) Download Arduino Project https://github.com/synackuk/checkm8-a5
5) Rename Project to "checkm8-a5" and open it in Arduino IDE
6) Download Sliver 5.4 https://www.appletech752.com/Downloads/SliverV5.4.dmg
7) Move Sliver to Application Folder (Sliver must be in your Applications folder in Finder! Sliver only supports MacOS High Sierra and Higher!)
8) Left click on Sliver and select 'show package contents'. Type 'sudo chmod -R 755' in a new terminal window, then click the space bar, then drag and drop the resources folder into Terminal. Click enter.

## Get iPad ready
10) Open Sliver
11) Connect iPad via USB
12) Enter DFU Mode on iPad (Turn iPad off, press Power-Button and Home-Button for 10s, then release Power-Button and keep Home-Button pressed, then wait until iTunes detect iPad in Recovery Mode(iTunes))
13) Check CPID-Number via Sliver "A6 Bypass" > "iPhone 5" > "Enter pwned DFU" > Note The CPID-Number, mine is 8940
14) Download Arduino Project https://github.com/synackuk/checkm8-a5

## Get Arduino ready 
16) Rename Project to "checkm8-a5" and open it in Arduino IDE
17) Change the CPID Number in the Arduino project to cour noted CPID-Number
18) Connect Aruduino via USB to Computer (USB A cable) (Greed LED on Arduino should be on)
19) Select USB Port in Arduino IDE
20) Upload sketch to Arduino Uno
21) Unplug Arduino from Computer
22) Plug USBHost-Shield onto Arduino
23) Connect LED and Resitor to USBShield SCHALTPLAN

## Bypass iPad
24) Connect iPad to USBHost-Shield via USB
25) Connect Arduino Uno to Computer via USB
26) LED shloud blink 3 Times and 


