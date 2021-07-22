# ipad2_ipad3_icloud_bypass
How To Remove bypass iCloud Lock in iPad2 and iPad3 in iOs 8.x.x

# Method 1 (only for 4G Devices)
Remove Resistor R1024 and Recover via iTunes


# Method 2 (for Wifi-Model and Wifi/4G Model)
Bypass via Arduino + USB Host Shield (https://www.youtube.com/watch?v=oMuprT7YCFo&t=11s)

1) Download Arduino IDE
2) Install USBHost Library
3) Patch USB Library
> cd path/to/Arduino/libraries
> git clone https://github.com/felis/USB_Host_Shield_2.0
> cd USB_Host_Shield_2.0
> git checkout cd87628af4a693eeafe1bf04486cf86ba01d29b8
> git apply path/to/usb_host_library.patch
6) Download Sliver 5.4 and Move it to Application Folder (Sliver must be in your Applications folder in Finder! Sliver only supports MacOS High Sierra and Higher!)
7) Left click on Sliver and select 'show package contents'. Type 'sudo chmod -R 755' in a new terminal window, then click the space bar, then drag and drop the resources folder into Terminal. Click enter.
8) Open Sliver
9) Connect iPad via USB
10) Enter DFU Mode on iPad (Press Power-Button and Home-Button for 10s > Release Home-Button keep Power-Button pressed > Wait till iTunes detect iPad in Recovery Mode(iTunes))
11) Check ID Number via Sliver "A6 Bypass" > "iPhone 5" > "Enter pwned DFU" > Note The ID-Number, mine is 8940
12) Download Arduino Project https://github.com/synackuk/checkm8-a5
13) Rename Project to "checkm8-a5"


