# android-cheat-sheet
android-cheat-sheet







## Android 13

<br><br>

### How to bring back Android's 3-button navigation
- From Settings, go to System, Gestures, and then tap System Navigation. Gesture navigation will be selected by default, but you can tap 3-button navigation to make buttons appear at the bottom of your screen.

  













<br><br>
<br><br>
__________________________________________________________________________
__________________________________________________________________________
<br><br>
<br><br>




## Nice apks

<br><br>

### Wallpaper engine
- https://play.google.com/store/apps/details?id=io.wallpaperengine.weclient

### Keyboard
- Gboard
  
- Microsoft Swift Key
  - With Dall-E Image Generation
 














<br><br>
<br><br>
__________________________________________________________________________
__________________________________________________________________________
<br><br>
<br><br>




## KWLP (PAID)
- https://play.google.com/store/apps/details?id=org.kustom.wallpaper&hl=en_US
- https://www.youtube.com/watch?v=4S8aiCl-ktc

<br><br>

### requirements
- https://play.google.com/store/apps/details?id=com.teslacoilsw.launcher&hl=de&gl=US

<br><br>

#### Install
1. Download Nova Launcher
2. Settings -> Apps -> Default Apps -> Start-App -> Choose Nova Launcher
3. Download KLWP Live Wallpaper Maker (https://play.google.com/store/apps/details?id=org.kustom.wallpaper&hl=en_US)
4. Download KLWP Live Wallpaper Pro Key (https://play.google.com/store/apps/details?id=org.kustom.wallpaper.pro&hl=de&gl=US)
5. Download any KLWP Preset but do not open
  - Alternative you can do it in step 9 aswell there is a section

6. Remove everything from home screen aswell from other screens
  - If you can not remove search bar widget -> Nova Launcher Settings -> desktop -> search -> suchleistenplatzierung 'none'
  - You should also disable dock
  - You should add 3 home screens because most themes use multiple screens for effects

7. Hold screen and click Settings -> erscheinungsbild -> Unclick show notification bar
8. Hold screen and click Settings -> Backup blank home screeen to not do it again in future
9. Hold screen and click Wallpapers -> Click live wallpapers -> Kustom -> click settings icon -> Load presets -> select theme and apply (save icon) -> apply walppaper - select home and lock screen

10. done :) 


<br><br>
<br><br>

#### FAQ

<br><br>

##### I can not apply live wallpaper anymore
- try to open the app instead of your theme

<br><br>

##### I can not change theme anymore
- Change to default live wallpaper and then apply again theme

<br><br>

##### touch on live wallpaper not working
- Try going into Settings for Kustom. Go to Advanced settings. There will be a toggle for "Use Direct Touch". Toggle it. See if that helps
- close all opend apps

<br><br>
<br><br>

#### Themes
- Just search in play store for kwlp














## Recovery

### Best Recovery Tool
- For my opinion
  1. PItchBlack
  2. OrangeFox
  3. TWRP


<br><br>
<br><br>

### Understand what partition you WIPE
- https://xdaforums.com/t/info-android-device-partitions-and-filesystems.3586565/

#### Dalvik / ART Cache 
- This is the runtime cache, where executable binaries are stored (after APK files are "optimized"). It is a unique partition of the system
  
#### Cache
- /cache partition, where temporary data is stored. These (numbers 1&2) are wiped on any clean or dirty flash of a ROM, or if problems occur in a running system. Wiping these is usually done together and do not effect actual user information or data.

#### System (**NO NEED TO WIPE** - *1)
- the /system partition, basically the operating system. This is only wiped when changing ROMs and a clean flash is required, it should never be done on a "stock" system in most cases other than already stated.

#### Data 
- the /data partition EXCLUDING /data/media (Internal Storage). This is how to perform a "factory reset", this will wipe all applications and user data, but not user's file (picture, music, documents, etc). When doing this, both cache and Dalvik/Art cache should be wiped as well.

#### Internal Storage 
- This is your /data/media folder, or user files. If you want a TRUE factory reset, you need to wipe this as well... be aware this will wipe all user file such as pictures, music, documents, and ROM images if you downloaded them there.

#### MicroSD 
- self explanatory

#### USB OTG 
- An external USB OTG storage device (often a USB stick) - self explanatory

#### Vendor (**NO NEED TO WIPE** - *1)
- This partition is replaced with a shortcut (symbolic link in fact) to /system/vendor directory. It contains system applications and libraries that do not have source code available on AOSP but added by vendors (OEM's).

*1 You should NEVER have to wipe system or vendor manually. If the instructions for flashing your ROM recommend doing this, you should ignore the recommendation. If your device has dynamic partitions, then you cannot wipe system or vendor anyway, even if you wanted to (unless you do it via fastboot - and if you attempt this, you are on your own).
























<br><br>
<br><br>
___________________________________________________
___________________________________________________
<br><br>
<br><br>

# Pitch Black Recovery Project

<br><br>

## Redmi Note 12 4G NFC (Topaz) (UNOFFICIAL at the moment) (PBRP-topaz-4.0-20230524-0619-UNOFFICIAL.img)
- https://sourceforge.net/projects/recovery-topaz/
- https://sourceforge.net/projects/recovery-topaz/files/TWRP/PBRP-topaz-4.0-20230524-0619-UNOFFICIAL.img.7z/download

<br><br>

### Install
```shell
fastboot flash recovery /home/dennis/Dennis/PBRP-topaz-4.0-20230524-0619-UNOFFICIAL.img

fastboot reboot recovery
```

































<br><br>
<br><br>
___________________________________________________
___________________________________________________
<br><br>
<br><br>

# OrangeFox Recovery

<br><br>

## Redmi Note 12 4G NFC (Topaz) (UNOFFICIAL at the moment)
- https://xdaforums.com/t/unofficial-recovery-13-14-orangefox-recovery-project-tapas-topaz.4600157/
- https://github.com/chickendrop89/orangefox_device_xiaomi_tapas/releases/download/2023-12-09/OrangeFox-Unofficial-tapas.img

<br><br>

### Install
```shell
fastboot flash recovery /home/dennis/Dennis/OrangeFox-Unofficial-tapas.img --slot=all

# If command above not work try
# fastboot flash recovery_a /home/dennis/Dennis/OrangeFox-Unofficial-tapas.img
# fastboot flash recovery_b /home/dennis/Dennis/OrangeFox-Unofficial-tapas.img

fastboot reboot recovery
```

<br><br>

### How to select sd card
- Files -> sdcard1

<br><br>

### Flash Guide
- https://wiki.orangefox.tech/en/guides/flashing
































<br>
<br>
___________________________________________________
___________________________________________________
<br>
<br>



# TWRP

<br><br>


## Redmi Note 12 4G NFC (Topaz) (UNOFFICAL at the moment)

### Guides
- https://www.youtube.com/watch?v=Apf-wx7wi9c

### Download
- https://sourceforge.net/projects/recovery-topaz/files/TWRP/twrp-3.7.0-RN124G_V2.img.7z/download

1. - Reload in fastboot
```shell
adb reboot bootloader
# If needed to go back use fastboot reboot
```

2.  Verify if it works
```shell
fastboot devices
```

3.  Flash recovery
```shell
fastboot flash recovery /home/dennis/Dennis/twrp-3.7.0-RN124G_V2.img
```


4. Reboot recovery
```shell
fastboot reboot recovery

# Check if everything is working - If yes Reboot -> System and check if your phone is still working
```















<br><br>
<br><br>
___________________________________________________
___________________________________________________
<br><br>
<br><br>



# Magisk

<br><br>

## Best Modules

<br><br>

### Pixelify
- https://telegra.ph/Pixelify-Troubleshooting-guide-03-12
- https://github.com/Kingsman44/Pixelify
- https://www.pling.com/p/1794976


#### Good2Know
- You can not add new live wallpapers.. So it is a bit useless to install pixelify if you only want live wallpapers

<br><br>

#### Supported OS & Devices

<br><br>

#### Not working
- **Pixel-Live-Wallpapers not really working with ProjectElixir_3.13_arm64_bgN-13.0-20231105-0917-OFFICIAL.img on Redmi Note 12 4G NFC (Topaz) - APP is crashing or only some Wallpaper are moving - Also everything is very unsmooth when using it**
- lineage-20.0-20231214-UNOFFICIAL-arm64_bgN.img on Redmi Note 12 4G NFC (Topaz)
  - Pixel Live Wallpapers is working doe but Google settings are not working anymore. But in my case I never was sign-in when I installed pixelify and that was maybe the problem. So if you install the ROM and sign-in to google and then install pixelify and follow the instructions from github then it may work..**

  
#### Install

<br><br>

##### Dependencies
- Make sure device is rooted with magisk
- Enable Zygsik (https://github.com/CyberT33N/android-cheat-sheet?tab=readme-ov-file#root-with-magisk-by-using-twrp-recovery--pitch-black-recovery)
- Add Google Play Services and inside com.google.android.gms.unstable in DenyList


1.  As usually install .zip via modules section of magisk
```

Quick Phrase spoofing (Not needed):
- Quick phrases are exactly what the name implies – phrases that you can say in earshot of your Google Pixel to perform a certain action.

<br><br>

next generation Assistant (optional):
- https://blog.google/products/assistant/next-generation-google-assistant-io/

<br><br>

Skip boot logo replacement if you can otherwhise you remove the nice one from your custom rom

<br><br>

Install Pixel Launcher

<br><br>

Install Google settings service
```

2. Reboot






<br><br>
<br><br>

#### Uninstall
- Due to some magisk uninstall.sh limitation whole pixelify cannot be removed by automatically.
  - To remove completely clear data of Google play services and Google Dialer and then reboot.














<br><br>
<br><br>

<br><br>
<br><br>

<br><br>
<br><br>





## Iconify
- https://github.com/Mahmud0808/Iconify/releases


### requirements
- Android 12+ Pixel / AOSP based custom ROM
- Magisk (Recommended) or KernelSU
- LSPosed

### Install
1. Download and install the Iconify app.

2. Open the app, grant root permission and follow the instructions.

3. Wait for it to finish generating rom specific module.

4. Reboot the device when prompted, profit!

5. Open LSposed -> hold iconify and selet re-optimize. Then enable module and then restart

















<br><br>
<br><br>


<br><br>
<br><br>


<br><br>
<br><br>



## Root with Magisk by using TWRP Recovery / Pitch Black Recovery

<br><br>
<br><br>

## Magisk v26.4 - Redmi Note 12 4G NFC (Topaz) - GSI
- If you have problem with recieving sms on gsi treble images you may read this here before installing magisk or try the steps below
  - https://github.com/CyberT33N/android-cheat-sheet?tab=readme-ov-file#not-able-to-recieve-sms-on-trebledroid---android-13-gsi
 
  - 
<br><br>

### Guide 
- https://www.youtube.com/watch?v=7eR7bVu-e4s

<br><br>

1. Download latest Magisk
- https://github.com/topjohnwu/Magisk/releases/tag/v26.4

<br><br>

2 Reboot recovery
```shell
adb reboot bootloader
fastboot reboot recovery
```

<br><br>

3. Install
a) TWRP Recovery / Pitch Black Recovery -> Advanced -> ADB Sideload -> SWIPE (No need to check anything)

<br><br>

b) Check devices
```
# You should see there sideload next to your device in the other column
adb devices
```

<br><br>

c)
```
adb sideload /home/dennis/Dennis/Magisk-v26.4.apk
```
- Click Reboot System

<br><br>

d) Open Magisk app
- It will ask for re-flash (If not open magisk app and click install at magisk icon) > Click direct installation -> Reboot Button

<br><br>

e) Download Root Checker Basic APP and verify if your are rooted



<br><br>
<br><br>

## Magisk v23
- 1. Download Magisk-v23.0.apk (https://github.com/topjohnwu/Magisk/releases) to your smartphone
- 2. Rename file to Magisk-v23.0.zip, copy Magisk-v23.0.zip and rename it to uninstall.zip (So at the end you have 2x .zip)
- 3. Hold Volume Up + Power Button to boot into TWRP
- 4. Install > Select Magisk-v23.0.zip > Select Reboot
- 5. If you got endless loading screen go again into TWRP and then install uninstall.zip




<br><br>
<br><br>

## Magisk v20.4 (Works with Lineage 17.1)
- 1. Download Magisk-v20.4.zip (https://github.com/topjohnwu/Magisk/releases/download/v20.4/Magisk-v20.4.zip) and Magisk-uninstaller-20200323.zip(https://github.com/topjohnwu/Magisk/releases/download/v20.4/Magisk-uninstaller-20200323.zip) to your smartphone
- 2. Hold Volume Up + Power Button to boot into TWRP
- 3. Install > Select Magisk-v23.0.zip > Select Reboot
- 5. If you got endless loading screen go again into TWRP and then install uninstaller.zip









<br><br>
<br><br>

### Hide apps from being detected as root
- If you have problem with recieving sms on gsi treble images you may read this here before installing magisk or try the steps below
  - https://github.com/CyberT33N/android-cheat-sheet?tab=readme-ov-file#not-able-to-recieve-sms-on-trebledroid---android-13-gsi

#### After Magisk 24
0. Hide Magis app via settings
1. Make sure Zygisk is enabled & enfore deny list is disabled (Reboot if you enabled it for first time)
2. Download YASNAC SafetyNet Checker
3. Download safetynet-fix (https://www.youtube.com/watch?v=rggvk3DPD1o):
        - https://github.com/kdrag0n/safetynet-fix/releases
            - Install .zip via magisk module section -> Reboot

4. Install LSposed (https://github.com/CyberT33N/android-cheat-sheet?tab=readme-ov-file#lsposed-framework)
  - Download Shamiko: https://github.com/LSPosed/LSPosed.github.io/releases and flash it with magisk -> Reboot
   - Make sure Universal fix and shamiko modules are sucessfully enabled. Try pass YASNAC SafetyNet Checker and check any app that is detecting you from root. E.g. freenow
     - If not work try to go to step 5
       
6. (optional) Magisk -> Settings -> configure deny list -> 3 dots show system apps -> enable play store and google play services
   - At google play service only enable:
    - com.google.com.android.gms 
    - com.google.android.gms.unstable

7. Now go to Settings -> Coonfigure deny list and now add apps where you want to hide root from

<br><br>
<br><br>

#### Before Magisk 24
(https://www.youtube.com/watch?v=WrbY1UXw81M)
- Download Magisk Manager (https://github.com/topjohnwu/Magisk/releases)
- Open Magisk Manager and navigate to Modules. Search for "hide" and and install "MagiskHide Props Config". Reboot
- Go to settings and enable "Magisk Hide".  After click on "Systemless Hosts".
- Click on "Hide Magisk Manager". This will hide the Magisk Manager by giving the app a new name.
- Click on "Superuser" tab and select MagiskHide. Here you can select the app which you want to hide from Root. Thats it!





















<br>
<br>
___________________________________________________
___________________________________________________
<br>
<br>

# LSposed Framework

## Redmi Note 12 4G NFC (Topaz) - Lineage OS 20

### Guide
- https://www.youtube.com/watch?v=FtZuoynM0p4

1. Open Magisk -> Settings -> Enable Zygisk -> Reboot

2. Download latest LSposed Zygisk Release
- [https://github.com/LSPosed/LSPosed](https://github.com/LSPosed/LSPosed/releases/tag/v1.9.2)

3. Open Magisk -> Modules -> Install the download zip -> Reboot

4.  If you can not see the app then unzip there archive and open manager.apk
   


















<br>
<br>
___________________________________________________
___________________________________________________
<br>
<br>

## Substratum Theme engine
- https://droidwin.com/install-substratum-themes-android/

### Guides
- https://droidwin.com/install-substratum-themes-android/

1. Install Substratum Theme engine -> Start APP -> Access root -> Accept usage
2. Reboot





























<br><br>
_________________________________________________________
_________________________________________________________
<br><br>

# Custom Roms

<br><br>
<br><br>

## Best in slot (My personal list)
1. LineageOS with Pixelify
2. Project Elixir
3. SparkOS
4. Evolution X
5. Superior OS
6. Derpfest
7. VoltageOS








<br><br>
<br><br>


## Privacy

<br><br>

#### grapheneos
- https://grapheneos.org/
- Pixel, Xiaomi Mi A2

#### calyxos
- https://calyxos.org/install/
- Pixel, Xiaomi Mi A2

#### copperhead
- https://calyxos.org/install/
- Pixel














<br><br>
_________________________________________________________
_________________________________________________________
<br><br>

# Install custom ROM Guides
- Below you will find guides which I wrote an tested..

<br><br>

## General Guides

<br><br>

### How to insert the SIM card?
- https://www.youtube.com/watch?v=TPcXMbwgO48




<br><br>
<br><br>

## Dependencies
- https://developer.android.com/studio/run/device

<br><br>

### Ubuntu
```
sudo apt install adb fastboot

# virtualbox usb detection - If you want to try unlock your phone via windows virtual box
sudo usermod -G vboxusers -a $USER

sudo usermod -aG plugdev $LOGNAME

reboot

# This command should work or alternative check if you see usb devices at your vm settings
vboxmanage list usbhost
```

### Windows
- https://www.youtube.com/watch?v=u4zHekIABrI
  - Basicly download platform tools and install google usb driver




















<br><br>
<br><br>
<br><br>
<br><br>


# Galaxy Tab 10.1 - GT-P7500

<br><br>

## Ipad ROM
- https://www.youtube.com/watch?v=eZG3lBX0Vx0





















<br><br>
<br><br>
<br><br>
<br><br>

<br><br>
<br><br>
<br><br>
<br><br>



# Redmi Note 12 4G NFC (Topaz)
- **As it seems for the moment no official & unofficial Android 14 GSI Image is working**
- **As it seems for the moment no official & unofficial Android 13 GSI Image is able to recieve SMS out of the box**
  - But most GSI images got Phh Treble Settings which can fix it
    - [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)
     - **But nothing is really stable beside of the rom from Project Elixir**


<br><br>
<br><br>


## Flash back to stock firmware
Download original stock firmware (https://new.c.mi.com/global/miuidownload/index)
- Redmi Note 12/NFC
  - https://new.c.mi.com/global/miuidownload/detail/device/1900579
    - Extract archive

- If you can not find the same MIUI-Version in the link above then try here:
  - https://miuirom.org/phones/redmi-note-12-4g-nfc#EEA
    - https://airtel.bigota.d.miui.com/V14.0.12.0.TMGEUXM/topaz_eea_global_images_V14.0.12.0.TMGEUXM_20231106.0000.00_13.0_eea_0d5c69604e.tgz
```
# go into fastboot

cd /home/dennis/Dennis/topaz_eea_global_images_V14.0.12.0.TMGEUXM_13.0 
chmod +x flash_all.sh
./flash_all.sh
```






<br><br>
<br><br>

## Generic System Image (GSI)
- https://github.com/phhusson/treble_experimentations/wiki/Generic-System-Image-%28GSI%29-list
- https://magiskzip.com/gsi-list-phhusson/
```
Download the “Project Info” app from the Google Play Store.
Launch the app and tap on the “Images” tab.
Look for the “Screen Message”.
If your phone supports Project Treble, then you see also which file you should download.
```
- If you’re looking to install a custom ROM on your Android device, you may be interested in using a Generic System Image (GSI). GSIs are pure Android implementations that can be flashed to any Project Treble-compliant device. This means that you can install a GSI ROM on your device even if it is not officially supported by the ROM’s developer.
    - **But this means as well there is a high chance that something will not work.. However my Prio is always OFFICIAL -> GSI -> UNOFFICIAL ROMS from XDA**






<br><br>
<br><br>



## official ROMS


<br><br>
<br><br>


### DroidX

<br><br>

#### Android 13
- https://sourceforge.net/projects/droidxui-releases/files/topaz/droidx-1.7-20231223-0504-OFFICIAL-topaz-Gapps.zip/download






<br><br>
<br><br>


### Cherish OS

<br><br>

#### Android 13
- https://cherishos.com/
- https://sourceforge.net/projects/cherish-os/files/device/topaz/Cherish-OS-v4.12-20230928-0417-topaz-OFFICIAL-GApps.zip/download




<br><br>
<br><br>

### Alpha Droid

#### Android 13
- https://github.com/AlphaDroid-Project
- https://sourceforge.net/projects/alphadroid-project/files/topaz/AlphaDroid-13.0-20231103-topaz-vanilla-v1.10.zip/download




<br><br>
<br><br>

### AfterLife Project

#### Android 13 - AfterLife-V3.0-Envy-OFFICIAL-topaz-20231104-CoreGApps.zip
- https://sourceforge.net/projects/afterlife-projects/files/release/topaz/
- https://sourceforge.net/projects/afterlife-projects/files/release/topaz/AfterLife-V3.0-Envy-OFFICIAL-topaz-20231104-CoreGApps.zip/download








<br><br>
<br><br>
<br><br>



## unofficial ROMS 
- https://xdaforums.com/t/shared-unofficial-list-of-roms-for-topaz-and-tapas.4630557/
```
These are some Popular tested Roms
There are more roms but i guess im lazy to paste it here

Please Follow this directions carefully
You dont wanna be like, left with hard bricked device after skipping a step
It was not booting

HOW TO FLASH ROMS
1. Boot to TWRP
2. Flash preflash before flash rom
3. Flash ROM Vanilla build
4. Flash twrp
5. Reboot twrp again
6. Flash RO2RW DFE
7. Reboot twrp again
8. Flash Gapps (Recomended Using nikGapps) If Needed
9. Wipe data, metadata, dalvik, cache


ROMS
FOR TOPAZ AND TAPAS

CrDroid
https://rb.gy/s2sg0

Paranoid
https://rb.gy/f1foe

Pixel OS
https://rb.gy/3daen

Evolution X
https://rb.gy/70221

Superior OS Extended
https://rb.gy/6ro4z

Pixel Extended
https://rb.gy/r1tss

Rising OS
https://rb.gy/hkme1

Arrow Os
https://rb.gy/0vz92

Proton Plus
https://rb.gy/7o6t2


pixysos

AlphaDroid
```






<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>

### Unlock phone with MI Unlock

1. entiwckler optionen aktivieren
- Einstellung -> Über das Telefon -> Mehrfach klciken auf MUI-Version
  - Einstellung -> Weitere Einstellung -> Entwickler Optionen -> OEM Entsperrung & USB Debugging
    - Verify that everything worked:
    ```shell
    adb devices
    ```
      - Your device should be shown with id

2. Connect to WLAN

3. Add your Mi Account
Settings > Mi Account

4. mi unlock status
- Turn off wifi & enable mobile data
  - Einstellung -> Weitere Einstellung -> Entwickler Optionen -> MI Entsperrstatus
    - Click add account
      - Donwload Unlock Tool (https://en.miui.com/unlock/download_en.html)
        - http://miuirom.xiaomi.com/rom/u1106245679/7.6.727.43/miflash_unlock_en_7.6.727.43.zip
          - Make sure that MI Entsperrstatus windows is opended and you use version 7.6.727.43 of MI Unlock to recieve the sms verificytion code
            - Reload in fastboot
            ```shell
            adb reboot bootloader
            # If needed to go back use fastboot reboot
            ```
              - Check devices:
              ```shell
              # This should show your device like adb devices
              fastboot devices
              ```
                - Now click unlock via MI Unlock GUI. Normally you have to wait now a few days before Xiaomi allows you to unlock the phone. After the time period is done you can retry it and the unlock should be successfully
                  - Restart the phone and then setup the phone again because we have to enable USB-Debugging again..


















<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>

## How to install any Generic System Image (GSI)
- Make sure TWRP is installed as fallback
   [Install TWRP](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#twrp)
### Fastboot
```
# Check if device can be found
adb devices

# unzip the .xz file
# unxz '/home/dennis/Dennis/ProjectElixir_3.13_arm64_bgN-13.0-20231105-0917-OFFICIAL.img.xz'

adb reboot bootloader

# Check if device can be found
fastboot devices





## --------------- TWRP METHOD - WIPE (RECOMMEND) --------
fastboot reboot recovery

## 1. TWRP -> WIPE -> ADVANCED WIPE -> Darvik, cache, data (If you get error then do first 2. and then 1. and then 3.)
### 2. TWRP -> WIPE -> FORMAT DATA
####  3. TWRP -> REBOOT -> into fastboot -> Flash rom



# If you face any errors here with red text beside of partition not found then you should do the steps above which are basicly the same in TWRP
## --------------- FASTBOOT METHOD - WIPE --------
fastboot erase userdata
fastboot erase cache
fastboot erase data
# fastboot erase system <-- Not sure about this.. A lot of ppl say never touch system or vendor..







fastboot flash system /home/dennis/Dennis/ProjectElixir_3.13_arm64_bgN-13.0-20231105-0917-OFFICIAL.img
```
- If error "not enough space to resize partition" (https://droidwin.com/fix-failed-remote-not-enough-space-to-resize-partition/)
```shell
# Search for (bootloader) current-slot
fastboot getvar all

# If it is (bootloader) current-slot:b
fastboot delete-logical-partition product_b
fastboot flash system_b /home/dennis/Documents/dennis/lineage-20.0-20231214-UNOFFICIAL-arm64_bgN.img
```

Then boot into your new oeprating system:
```
fastboot reboot
```
- **Make sure to do this directly after reboot (before the setup process) or it will maybe later not work after root**
  - [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)


























<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>


## VoltageOS

<br><br>

### Android 13 - UNOFFICIAL - VoltageOS-2.8-EOL-20230920-UNOFFICIAL_bgN.img
- https://github.com/ahnet-69/treble_voltage/releases/download/2.8-EOL-20230920/VoltageOS-2.8-EOL-20230920-UNOFFICIAL_bgN.img.xz

<br><br>

#### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)


<br><br>

#### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)

<br><br>

####
- Got pulse audio visuliazer but not really much UI modifications and no custom GS header image












<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>


## RisingOS

<br><br>

### Android 13 - UNOFFICIAL - risingOS-v1.4-Elysium-20231001-arm64_bgN.img
- **WARNING - not booting into setup - just background image**
- https://sourceforge.net/projects/misterztr-gsi/files/RisingOS/Android%2013/GApps/risingOS-v1.4-Elysium-20231001-arm64_bgN.img.xz/download
  
<br><br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)


<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)






















<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>




## ProjectBlaze

<br><br>

### Android 13 - UNOFFICIAL - ProjectBlaze_arm64-ab.img
- **WARNING - NOT BOOTING INTO SETUP**
- https://sourceforge.net/projects/any-artifact/files/GSI/ProjectBlaze/v2.5_230224/
- https://sourceforge.net/projects/any-artifact/files/GSI/ProjectBlaze/v2.5_230224/ProjectBlaze_arm64-ab.img.xz/download
  
<br><br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)







































<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>




## DerpFest

<br><br>

### Android 14 - UNOFFICIAL - DerpFest-arm64_bgN-14.0-unofficial-20231219.img
- ** NOT BOOTING**
- https://github.com/KoysX/treble_DerpFest_GSI/releases
- https://github.com/KoysX/treble_DerpFest_GSI/releases/download/v2023.12.19/DerpFest-arm64_bgN-14.0-unofficial-20231219.img.xz

  
<br><br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>






<br><br>
<br><br>

### Android 13 - UNOFFICIAL - DerpFest-13-Community-Tango-arm64_bvN-gsi-20231009-Gapps.img
- ** NOT BOOTING**
- https://github.com/KoysX/treble_DerpFest_GSI/releases
- https://github.com/KoysX/treble_DerpFest_GSI/releases/download/2023.10.09/DerpFest-13-Community-Tango-arm64_bvN-gsi-20231009-Gapps.img.xz

  
<br><br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>

### Review
- As it seems no custom GS image is changeble. But audio visualizer für lockscreen is integrated. overall ui looks not so good doe.

<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)














<br><br>
<br><br>
___________________________________________________
___________________________________________________

<br><br>
<br><br>




## Cherish OS

<br><br>

### Android 13 - UNOFFICIAL - CherishOS_A13-arm64-bgS-slim_20231022.img
**UI Bug - Can not setup installation - Only see background**
- https://github.com/ChonDoit/treble_cherishos_patches/releases
- https://github.com/ChonDoit/treble_cherishos_patches/releases/download/A13-v20231022/CherishOS_A13-arm64-bgS-slim_20231022.img.xz

  
<br>
<br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)



























<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>




## AlphaDroid OS
- https://github.com/ChonDoit/treble_alphadroid_patches/releases/
  
<br><br>

### Android 13 - UNOFFICIAL - AlphaDroid_A13-arm64-bgS-slim_20231009.img
- **Warning setup process not working - just background image**
- https://github.com/ChonDoit/treble_alphadroid_patches/releases/download/A13-v20231009/AlphaDroid_A13-arm64-bgS-slim_20231009.img.xz

<br><br>

### Install
- [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)



























<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>




## Superior OS
- https://github.com/ChonDoit/treble_superior_patches/releases
  
<br><br>

### Android 13 - UNOFFICIAL - SuperiorOS_A13-arm64-bgS-slim_20231103.img
- https://github.com/ChonDoit/treble_superior_patches/releases/download/A13-v20231103/SuperiorOS_A13-arm64-bgS-slim_20231103.img.xz

<br>
<br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)

### Review
- Not so much custom featurs and ui not so great































<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>




## SparkOS

<br>
<br>

### Android 13 - UNOFFICIAL - SparkOS-13.8-arm64_bgN-Unofficial.img.xz
- https://github.com/naz664/SparkOS_gsi/releases/download/v2023.10.15/SparkOS-13.8-arm64_bgN-Unofficial.img.xz

<br><br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)

### Review
- As it seems the UI is sometimes not stable but it happens very rar. And I'm not sure how to set custom QS Header image. Also for default no live wallpaper feature




























<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>




## crDroid

<br>
<br>

### Android 14 - UNOFFICIAL - crDroid-10.0-arm64_bgN-Unofficial.img
- **WARNING - Not booting**
- https://github.com/naz664/crDroid_gsi/releases

<br>
<br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)
























<br>
<br>
___________________________________________________
___________________________________________________

<br><br>




## Project Elixir OFFICIAL Generic System Image (ProjectElixir_3.13_arm64_bgN-13.0-20231105-0917-OFFICIAL.img) 
- https://www.pling.com/p/1960767/

<br><br>

### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

<br><br>

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)

<br><br>

### Review
- You can set custom GS header Image which is nice. But you do not have music bar playing setting for lockscreen





















<br>
<br>
___________________________________________________
___________________________________________________

<br><br>
<br><br>




## Pixel OS

<br><br>

### OFFICIAL Generic System Image - Android 14 (PixelOS_Beta_treble_arm64_bN-14.0-20231114.img) 
- **NOT WORKING - Boots back into recvory**
- https://github.com/MisterZtr/PixelOS_gsi/releases
    - https://sourceforge.net/projects/misterztr-gsi/files/PixelOS/Android%2014/PixelOS_Beta_treble_arm64_bN-14.0-20231114.img.xz/download
- https://github.com/MisterZtr/PixelOS_gsi

<br><br>

#### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)




<br><br>
<br><br>


### OFFICIAL Generic System Image - Android 13 (PixelOS-13.0-20230710-arm64_bgN.img) 
- https://sourceforge.net/projects/misterztr-gsi/files/PixelOS/Android%2013/PixelOS-13.0-20230710-arm64_bgN.img.xz/download

- <br><br>

#### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)




















<br><br>
<br><br>
___________________________________________________
___________________________________________________

<br><br>
<br><br>







# AOSP

<br><br>

## Android 14.0 v2023.10.14 - (aosp-arm64-ab-gapps-14.0-20231014.img)
- **NOT WORKING - goes into Recovery again**
- https://github.com/ponces/treble_aosp/releases/tag/v2023.10.14
- https://github.com/ponces/treble_aosp/releases/download/v2023.10.14/aosp-arm64-ab-gapps-14.0-20231014.img.xz

<br><br>

## Android  13.0 v2023.09.19 - (aosp-arm64-ab-gapps-13.0-20230919.img)
- **Warning - Google play protect is not working out of the box**
- https://github.com/ponces/treble_aosp/releases/download/v2023.09.19/aosp-arm64-ab-gapps-13.0-20230919.img.xz























<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>



## Evolution X

<br><br>

### Android 14 -  (evolution_arm64-ab-8.0.3-unofficial-20231201.img)
- **NOT WORKING - Boots back into recvory**
- https://github.com/KoysX/treble_build_evo/releases
  - https://github.com/KoysX/treble_build_evo/releases/download/v2023.12.01/evolution_arm64-ab-8.0.3-unofficial-20231201.img.xz

<br><br>

#### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)





<br><br>
<br><br>

### Android 13 - (evolution_arm64-ab-7.9.7-unofficial-20230823.img)
- https://github.com/ponces/treble_build_evo/releases

#### Install
-  [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

#### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)

#### Review
- Not sure how to set custom GS Header Image. But audio visuliaisier for lockscreen is there. Over aller medium - good





































  
<br>
<br>
___________________________________________________
___________________________________________________

<br>
<br>



## Cherish-OS-v4.12-20230928-0417-topaz-OFFICIAL-GApps (Guide not perfect yet - will update soon)
- https://cherishos.com/
- https://sourceforge.net/projects/cherish-os/files/device/topaz/Cherish-OS-v4.12-20230928-0417-topaz-OFFICIAL-GApps.zip/download

  
### Install
- TWRP must be installed
   [Install TWRP](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#twrp)
```
# Check if device can be found
adb devices

# Download a file and check if it can be found here at this path
adb shell ls /storage/emulated/0/Download/

# Upload the .zip to your download folder
adb push /home/dennis/Dennis/Cherish-OS-v4.12-20230928-0417-topaz-OFFICIAL-GApps.zip /storage/emulated/0/Download/

adb reboot bootloader

# Check if device can be found
fastboot devices

fastboot reboot recovery

# TWRP -> WIPE -> Advanced WIPE -> Cache, Dalvik, Data
# Vendor and System should not be wiped even if the guide is saying so!

# TWRP -> Install -> Choose .zip
# In my case there was an error with failed to mount /product (invalid argument) but at the the end it worked anyway..

# TWRP -> WIPE -> Format Data

# TWRP -> REBOOT -> System
```























<br><br>
<br><br>
<br><br>




# LineageOS 20 

<br><br>
<br><br>

## Light - Android 13 - lineage-20.0-20231212-UNOFFICIAL-gsi_arm64_gN.img
- https://sourceforge.net/projects/andyyan-gsi/files/lineage-20-light/lineage-20.0-20231212-UNOFFICIAL-gsi_arm64_gN.img.xz/download
- **Warning - Google play protect is not working out of the box. Also I experienced restart into Recovery idk why**


<br><br>
<br><br>


## TD - Android 13 - lineage-20.0-20231214-UNOFFICIAL-arm64_bgN
- **The Guide below was from droidwin. Because the Image is GSI it will be enough to just do this aswell**:
  - [Install any Generic System Image (GSI)](https://github.com/CyberT33N/android-cheat-sheet/?tab=readme-ov-file#how-to-install-any-generic-system-image-gsi)

## GUI

<br><br>

### XiaoMiToolV2 (Deprecated / Not supported any more)
- https://github.com/francescotescari/XiaoMiToolV2

<br><br>

## Guides
- https://droidwin.com/how-to-install-lineageos-on-redmi-note-12-pro/
- https://droidwin.com/fix-failed-remote-not-enough-space-to-resize-partition/

<br><br>

### Install
1. Get the details about your current MIUI-Version & Androidversion
  - Settings -> About this phone
    - In my case it is:
      - MIUI 14 14.0.12.0 TMGEUXM (Topaz)

2. Enable USB-Debugging

3. Donwload Lineage OS 20 (lineage-20.0-20231214-UNOFFICIAL-arm64_bgN.img.xz)
- With GAPPS
- https://sourceforge.net/projects/andyyan-gsi/files/lineage-20-td/
- https://sourceforge.net/projects/andyyan-gsi/files/lineage-20-td/lineage-20.0-20231214-UNOFFICIAL-arm64_bgN.img.xz/download
  - Extract archive and copy the .img to folder of your choice

4. Download original stock firmware (https://new.c.mi.com/global/miuidownload/index)
- Redmi Note 12/NFC
  - https://new.c.mi.com/global/miuidownload/detail/device/1900579
    - Extract archive

- If you can not find the same MIUI-Version in the link above then try here:
  - https://miuirom.org/phones/redmi-note-12-4g-nfc#EEA
    - https://airtel.bigota.d.miui.com/V14.0.12.0.TMGEUXM/topaz_eea_global_images_V14.0.12.0.TMGEUXM_20231106.0000.00_13.0_eea_0d5c69604e.tgz

- Extract the archive and copy to vbmeta.img to folder of your choice


4. Go into fastboot
  - Power off and then hold volume down and power button (Hold it long atleast 15 seconds)
  ```shell
  adb reboot bootloader
  ```
    - Verify fastboot connection:
    ```shell
    fastboot devices
    ```

5. Disable Verity Check
```shell
fastboot --disable-verification flash vbmeta '/home/dennis/Dennis/topaz_eea_global_images_V14.0.12.0.TMGEUXM_13.0/images/vbmeta.img'
```

6. Flash LineageOS ROM
```shell
# Wait until you see fastbootd logo
fastboot reboot fastboot

# maybe try this before and search for Search for (bootloader) current-slot in case that you directly get the correct partition
# fastboot getvar all

# Now delete the logical partition to free up some space on your device
fastboot delete-logical-partition product_a

# Flash rom
# NOTE: Make sure that the system.img is being flashed in the same partition whose product partition is deleted. In our case, product_a is deleted, so system.img is being flashed to the system_a partition. If that is not the case with you, then you’ll get a not enough space to resize partition error. In such cases, either delete the other product partition [b] and then flash system.img there [b] or flash the system.img to the partition [a] whose product is deleted [a].
fastboot flash system system.img
```
  - If error "not enough space to resize partition" (https://droidwin.com/fix-failed-remote-not-enough-space-to-resize-partition/)
  ```shell
  # Search for (bootloader) current-slot
  fastboot getvar all

  # If it is (bootloader) current-slot:b
  fastboot delete-logical-partition product_b
  fastboot flash system_b /home/dennis/Documents/dennis/lineage-20.0-20231214-UNOFFICIAL-arm64_bgN.img
  ```

7. format data
```shell
fastboot -w
```
  - If you get error "fastboot: error: Cannot generate image for userdata"
  ```shell
  fastboot erase userdata
  ```

8. reboot
```
fastboot reboot
```

9. [Install TWRP](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#twrp)
10. [Install Magisk](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#magisk)
11. [Install LSposed](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#lsposed-framework)
    
13. (optional) Instal Substratum Theme
    - Most themes are paid only
   

### Recieve SMS
- [FIX - SMS recieving not working](https://github.com/CyberT33N/android-cheat-sheet/blob/main/README.md#not-able-to-recieve-sms-on-trebledroid---android-13-gsi)


























































# FAQ


## Push files into internal storage from twrp
- If adb devices is working when you into twrp recovery you can use adb push:
```shell
adb push update.zip /sdcard
```
- if not working try disabling MTP from TWRP "Mount" men


<br><br>
<br><br>

## How To Fix Failed To Mount ( System_Root, '/ Vendor & More ( Invalid Argument & Resource Busy )
1. TWRP -> WIPE -> FORMAT DATA
2. TWRP -> REBOOT -> RECOVERY
3. TWRP -> WIPE -> ADVANCED WIPE -> Cache, Dalvik, Data (maybe aswell internal storage but should not be needed)


<br><br>
<br><br>

## Not able to recieve SMS on TrebleDroid - Android 13 GSI 
1. Disable WLAN and enable mobile data
   - Enable Mobile Data -> Set 4g as default

3. Settings -> Phh Treble Settings -> IMS features
    - Enable "Request IMS network"
    - Enable "Force the presence of 4G Calling setting"

4. Click "Install IMS APK for Qualcomm S+ vendor"

5. Click "Create APN"

6. Reboot

If above is not working with any GSI treble image then try to flash:
- https://github.com/CyberT33N/android-cheat-sheet?tab=readme-ov-file#project-elixir-official-generic-system-image-projectelixir_313_arm64_bgn-130-20231105-0917-officialimg

Then:
- Then do everything from Step 1 again
 - Configure this settings:
    - Deactivate VolTE
    - prefered network type LTE
    - Check Force LTE CA
       - Reboot  
        - If it now worked ... Then I opend magisk icon and direct installed it. Somehow it was already installed.. Maybe because I did not clean the magisk partition oder project elixir got it pre installed?

Then for some reasons at any point recieving sms stopped working but starts working again after reboot. However, this full logic of recieving sms ist extremly unstable and does not make any sense on Redmi Note 12 4G NFC (Topaz) with any treble gsi. Not sure what the problem is doe. However I noticed after installing 2 times project elixir gsi sms recieving starts working again but is also not really stable after rebooting... So whatever they did in this rom is a fix to this topic.

**Carefully** Then I installed LSposed Shamiko and recieving of sms stopped working again.
- https://github.com/CyberT33N/android-cheat-sheet?tab=readme-ov-file#hide-apps-from-being-detected-as-root
  - I deinstalled shamiko and then rebooted, then installed it again and rebooted
      - Then I deinstalled org.codeaurora.ims and removed apn and then did everything again from Step 1

Nothing helped?
- **Maybea a good approche in general if it does stop working again on any GSI or after you reboot and it stop work is**:
  - Disable WLAN and enable mobile data 
  - deinstalling org.codeaurora.ims and removed apn and then do everything again from Step 1-5**





<br><br>
<br><br>


### Alternatives fixes (not tested)

#### Way 1
```
For anyone is still having trouble with receiving messages on Pie GSIs(installed apk but still not working):
1. Download and install the apk in this thread
2. Rename the apk into "org.codeaurora.ims"(this is optional; I don't know if this changes anything).
3. Move the apk to /vendor/overlay
4. Reboot
5. Switch network to LTE
6. Done
This currently only works works on Pie GSIs only. I have tested(HavocOS and ArrowOS).
```

#### Way 2 (Depracted?)
```
You'll need my latest release v212.
Download https://treble.phh.me/ims-q.apk
Install it just like you would install any apk, by either clicking on it from file manager, or with adb install
Download https://treble.phh.me/android.hardwa...ephony.ims.xml
Push it to /system/etc/permissions: adb root & adb remount & adb push android.hardware.telephony.ims.xml /system/etc/permissions/android.hardware.telephony.ims.xml
Reboot, unlock your device, wait one minute. Reboot again, unlock your device, wait one minute.
Reboot. Wait one minute, go in *#*#4636#*#* and see if IMS works.
```


