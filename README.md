# android-cheat-sheet
android-cheat-sheet


<br><br>

# Root with Magisk by using TWRP

<br><br>

## Magisk v23
- 1. Download Magisk-v23.0.apk (https://github.com/topjohnwu/Magisk/releases) to your smartphone
- 2. Rename file to Magisk-v23.0.zip, copy Magisk-v23.0.zip and rename it to uninstall.zip (So at the end you have 2x .zip)
- 3. Hold Volume Up + Power Button to boot into TWRP
- 4. Install > Select Magisk-v23.0.zip > Select Reboot
- 5. If you got endless loading screen go again into TWRP and then install uninstall.zip

<br><br>

## Magisk v20.4 (Works with Lineage 17.1)
- 1. Download Magisk-v20.4.zip (https://github.com/topjohnwu/Magisk/releases/download/v20.4/Magisk-v20.4.zip) and Magisk-uninstaller-20200323.zip(https://github.com/topjohnwu/Magisk/releases/download/v20.4/Magisk-uninstaller-20200323.zip) to your smartphone
- 2. Hold Volume Up + Power Button to boot into TWRP
- 3. Install > Select Magisk-v23.0.zip > Select Reboot
- 5. If you got endless loading screen go again into TWRP and then install uninstaller.zip








<br><br>
<br><br>

## Hide apps from being detected as root (https://www.youtube.com/watch?v=WrbY1UXw81M)
- Download Magisk Manager (https://github.com/topjohnwu/Magisk/releases)
- Open Magisk Manager and navigate to Modules. Search for "hide" and and install "MagiskHide Props Config". Reboot
- Go to settings and enable "Magisk Hide".  After click on "Systemless Hosts".
- Click on "Hide Magisk Manager". This will hide the Magisk Manager by giving the app a new name.
- Click on "Superuser" tab and select MagiskHide. Here you can select the app which you want to hide from Root. Thats it!










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


# Redmi Note 12 4G NFC - Lineage 20

## gui
- https://github.com/francescotescari/XiaoMiToolV2

## guide
- https://droidwin.com/how-to-install-lineageos-on-redmi-note-12-pro/

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
  ```
  adb reboot bootloader
  ```
    - Verify fastboot connection:
    ```
    fastboot devices
    ```

5. Disable Verity Check
```
```
