# GentooT530
Configs for Gentoo on a Lenovo Thinkpad T530 i7-3720QM

`Bus 002 Device 002: ID 8087:0024 Intel Corp. Integrated Rate Matching Hub
Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 001 Device 006: ID 5986:02d2 Acer, Inc 
Bus 001 Device 005: ID 0a5c:21e6 Broadcom Corp. BCM20702 Bluetooth 4.0 [ThinkPad]
Bus 001 Device 004: ID 147e:2020 Upek TouchChip Fingerprint Coprocessor (WBF advanced mode)
Bus 001 Device 003: ID 046d:c52b Logitech, Inc. Unifying Receiver
Bus 001 Device 002: ID 8087:0024 Intel Corp. Integrated Rate Matching Hub
Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
Bus 004 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
Bus 003 Device 003: ID 1199:9013 Sierra Wireless, Inc. Sierra Wireless Gobi 3000 Modem device (MC8355)
Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub`

## Configuration options for Acer UVC webcam
Bus 001 Device 006: ID 5986:02d2 Acer, Inc
Driver: uvcvideo

`Device Drivers  --->
 <M> Multimedia support  --->
  [*]   Cameras/video grabbers support
  [*]   Media USB Adapters  --->
   <M>   USB Video Class (UVC)  
   [*]     UVC input events device support (NEW) `



# Networking

## Configurations for Intel Centrino Advanced-N 6205 Dual Band Wirless Card
03:00.0 Network controller: Intel Corporation Centrino Advanced-N 6205 [Taylor Peak] (rev 34)
Driver: iwldvm
Bands: 2.4 GHz/5 GHz
Max Speed: 300 Mbps
WiFi: 802.11a/b/g/n
Form Factor: PCIe Half MiniCard

To make it work some kernel configuration is needed. The driver supports 802.11a/b/g/n/ac (depending on the device), so IEEE 802.11 should be enabled. 

`[*] Networking support  --->
    [*] Wireless  --->
        <*>   cfg80211 - wireless configuration API
        [ ]     nl80211 testmode command
        [ ]     enable developer warnings
        [ ]     cfg80211 regulatory debugging
        [ ]     cfg80211 certification onus
        [*]     enable powersave by default
        [ ]     cfg80211 DebugFS entries
        [ ]     use statically compiled regulatory rules database
        [ ]     cfg80211 wireless extensions compatibility
        <*>   Generic IEEE 802.11 Networking Stack (mac80211)
        [*]   Minstrel
        [*]     Minstrel 802.11n support
        [ ]       Minstrel 802.11ac support
              Default rate control algorithm (Minstrel)  --->
        [ ]   Enable mac80211 mesh networking (pre-802.11s) support
        -*-   Enable LED triggers
        [ ]   Export mac80211 internals in DebugFS
        [ ]   Trace all mac80211 debug messages
        [ ]   Select mac80211 debugging features  ----`

Use this driver for Intel's current wireless chips. Set it as a module <M> as shown here. Also the correct DVM or MVM option according to the Module column of the firmware table is needed. 

`Device Drivers  --->
 
        [*] Network device support  --->
 
        --- Network device support
        [*]   Wireless LAN  --->
 
            --- Wireless LAN
            [ ]   ADMtek devices
            [ ]   Atheros/Qualcomm devices
            [ ]   Atmel devices
            [ ]   Broadcom devices
            [ ]   Cisco devices
            [*]   Intel devices
            < >     Intel PRO/Wireless 2100 Network Connection
            < >     Intel PRO/Wireless 2200BG and 2915ABG Network Connection
            < >     Intel Wireless WiFi 4965AGN (iwl4965)
            < >     Intel PRO/Wireless 3945ABG/BG Network Connection (iwl3945)
            <M>     Intel Wireless WiFi Next Gen AGN - Wireless-N/Advanced-N/Ultimate-N (iwlwifi)
            <M>       Intel Wireless WiFi DVM Firmware support
            <M>       Intel Wireless WiFi MVM Firmware support
            [ ]       Enable broadcast filtering (NEW)
            [ ]       Enable runtime power management mode for PCIe devices (NEW)
                      Debugging Options  --->
            [ ]   Intersil devices
            [ ]   Marvell devices
            [ ]   MediaTek devices
            [ ]   Ralink devices
            [ ]   Realtek devices
            [ ]   Redpine Signals Inc devices
            [ ]   STMicroelectronics devices
            [ ]   Texas Instrument devices
            [ ]   ZyDAS devices
            < >   Simulated radio testing tool for mac80211
            < >   Wireless RNDIS USB support`

## Configuration options for Sierra Wireless 3G WWAN Card
Bus 003 Device 003: ID 1199:9013 Sierra Wireless, Inc. Sierra Wireless Gobi 3000 Modem device (MC8355)
Driver: sierra
