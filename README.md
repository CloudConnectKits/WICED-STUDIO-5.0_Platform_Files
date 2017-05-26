# WICED-STUDIO-5.0_Platform_Files

Download this BCM94343W_AVN.zip file to your **...\WICED-Studio-5.0\43xxx_Wi-Fi\platforms folder** 

Unzip this file there to create the missing BCM94343W_AVN subfolder.

Note that these v5.0 platform files are not suitable for use with earlier versions of WICED SDK

# Note on BLE POWERSAVE !

The following **must** be added into the application **.mk** file in order for the BLE PowerSave function to work correctly!!!
(eg. **ble_hello_sensor.mk** in WICED Studio 5.0) 

#ENABLE_APP_POWERSAVE macro is also enabled for BCM94343_AVN platform (Avnet BCM4343W IoT Starter Kit)

ifeq ($(PLATFORM), BCM94343W_AVN)

ENABLE_APP_POWERSAVE := 1

GLOBAL_DEFINES += ENABLE_APP_POWERSAVE

#$(error $(ENABLE_APP_POWERSAVE))

endif
