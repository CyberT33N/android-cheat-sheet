# android-cheat-sheet
android-cheat-sheet









# TWRP

## Redmi Note 12 4G NFC - Lineage OS 20

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
fastboot flash recovery /home/dennis/Documents/dennis/twrp-3.7.0-RN124G_V2.img
```


4. Reboot recovery
```shell
fastboot reboot recovery

# Check if everything is working - If yes Reboot -> System and check if your phone is still working
```















<br>
<br>
___________________________________________________
___________________________________________________
<br>
<br>





# Magisk

## Root with Magisk by using TWRP

<br><br>

## Magisk v26.4 - Redmi Note 12 4G NFC - Lineage OS 20

### Guide 
- https://www.youtube.com/watch?v=7eR7bVu-e4s

1. Download latest Magisk
- https://github.com/topjohnwu/Magisk/releases/tag/v26.4

2 Reboot recovery
```shell
adb reboot bootloader
fastboot reboot recovery
```

3. Install
a) TWRP -> Advanced -> ADB Sideload -> SWIPE (No need to check anything)

b) Check devices
```
# You should see there sideload next to your device in the other column
adb devices
```

c)
```
adb sideload /home/dennis/Documents/dennis/Magisk-v26.4.apk
```
- Click Reboot System

d) Open Magisk app
- It will ask for re-flash > Click direct installation -> Reboot Button

d) Download Root Checker Basic APP and verify if your are rooted



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

#### After Magisk 24
0. Hide Magis app via settings
1. Make sure Zygisk is enabled & enfore deny list is disabled (Reboot if you enabled it for first time)
2. Run YASNAC SafetyNet Checker and pass
    - If you can not pass download (https://www.youtube.com/watch?v=rggvk3DPD1o):
        - https://github.com/kdrag0n/safetynet-fix/releases
            - Flash .zip -> Reboot -> re-run YASNAC SafetyNet Checker and pass
              - If not go to step 3
3. Download Shamiko: https://github.com/LSPosed/LSPosed.github.io/releases and flash it with magisk -> Reboot
   - Make sure Universal fix and shamiko modules are sucessfully enabled
     - If not work try to go to step 4
       
4. (optional) Magisk -> Settings -> configure deny list -> 3 dots show system apps -> enable play store and google play services
   - At google play service only enable:
    - com.google.com.android.gms 
    - com.google.android.gms.unstable
5. Now go to Settings -> Coonfigure deny list and now add apps where you want to hide root from

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

## Redmi Note 12 4G NFC - Lineage OS 20

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
<br><br>


# Redmi Note 12 4G NFC - lineage-20.0-20231214-UNOFFICIAL-arm64_bgN
- **WARNING** - In my case I was not able to recieve sms with this ROM**

## gui
- https://github.com/francescotescari/XiaoMiToolV2

## Guides
- https://droidwin.com/how-to-install-lineageos-on-redmi-note-12-pro/
- https://droidwin.com/fix-failed-remote-not-enough-space-to-resize-partition/

## nice 2 know
- https://droidwin.com/best-magisk-modules-2020-part-1/
- https://droidwin.com/install-xposed-framework-on-android-10-11-12-using-lsposed/
- https://droidwin.com/install-substratum-themes-android/
- https://droidwin.com/fix-viper4android-not-working-with-selinux-enforcing/

## How to insert the SIM card?
- https://www.youtube.com/watch?v=TPcXMbwgO48


### Install dependencies
- https://developer.android.com/studio/run/device

#### Ubuntu
```
sudo apt install adb fastboot
# sudo apt install android-tools-adb
# sudo apt-get install android-sdk-platform-tools-common

# virtualbox usb detection - If you want to try unlock your phone via windows virtual box
sudo usermod -G vboxusers -a $USER

sudo usermod -aG plugdev $LOGNAME

reboot

# This command should work or alternative check if you see usb devices at your vm settings
vboxmanage list usbhost
```

#### Windows
- https://www.youtube.com/watch?v=u4zHekIABrI
  - Basicly download platform tools and install google usb driver



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

### Install Lineage OS

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
fastboot --disable-verification flash vbmeta '/home/username/Documents/dennis/stock firmware/topaz_eea_global_images_V14.0.12.0.TMGEUXM_13.0/images/vbmeta.img'
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

9. Install TWRP
10. Install Magisk
11. Install LSposed
12. Instal Substratum Theme



