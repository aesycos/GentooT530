# GentooT530
Configs for Gentoo on a Lenovo Thinkpad T530 i7-3720QM

`$ lsusb
Bus 002 Device 002: ID 8087:0024 Intel Corp. Integrated Rate Matching Hub
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

#Configuration options for Acer UVC webcam
Bus 001 Device 006: ID 5986:02d2 Acer, Inc
Driver: uvcvideo

`Device Drivers  --->
 <M> Multimedia support  --->
  [*]   Cameras/video grabbers support
  [*]   Media USB Adapters  --->
   <M>   USB Video Class (UVC)  
   [*]     UVC input events device support (NEW) `

#Configuration options for Sierra Wireless 3G WWAN Card
Bus 003 Device 003: ID 1199:9013 Sierra Wireless, Inc. Sierra Wireless Gobi 3000 Modem device (MC8355)
Driver: sierra

`$ lspci
00:00.0 Host bridge: Intel Corporation 3rd Gen Core processor DRAM Controller (rev 09)
00:01.0 PCI bridge: Intel Corporation Xeon E3-1200 v2/3rd Gen Core processor PCI Express Root Port (rev 09)
00:02.0 VGA compatible controller: Intel Corporation 3rd Gen Core processor Graphics Controller (rev 09)
00:14.0 USB controller: Intel Corporation 7 Series/C210 Series Chipset Family USB xHCI Host Controller (rev 04)
00:16.0 Communication controller: Intel Corporation 7 Series/C216 Chipset Family MEI Controller #1 (rev 04)
00:16.3 Serial controller: Intel Corporation 7 Series/C210 Series Chipset Family KT Controller (rev 04)
00:19.0 Ethernet controller: Intel Corporation 82579LM Gigabit Network Connection (Lewisville) (rev 04)
00:1a.0 USB controller: Intel Corporation 7 Series/C216 Chipset Family USB Enhanced Host Controller #2 (rev 04)
00:1b.0 Audio device: Intel Corporation 7 Series/C216 Chipset Family High Definition Audio Controller (rev 04)
00:1c.0 PCI bridge: Intel Corporation 7 Series/C216 Chipset Family PCI Express Root Port 1 (rev c4)
00:1c.1 PCI bridge: Intel Corporation 7 Series/C210 Series Chipset Family PCI Express Root Port 2 (rev c4)
00:1c.2 PCI bridge: Intel Corporation 7 Series/C210 Series Chipset Family PCI Express Root Port 3 (rev c4)
00:1d.0 USB controller: Intel Corporation 7 Series/C216 Chipset Family USB Enhanced Host Controller #1 (rev 04)
00:1f.0 ISA bridge: Intel Corporation QM77 Express Chipset LPC Controller (rev 04)
00:1f.2 SATA controller: Intel Corporation 7 Series Chipset Family 6-port SATA Controller [AHCI mode] (rev 04)
00:1f.3 SMBus: Intel Corporation 7 Series/C216 Chipset Family SMBus Controller (rev 04)
01:00.0 VGA compatible controller: NVIDIA Corporation GF108M [NVS 5400M] (rev a1)
02:00.0 System peripheral: Ricoh Co Ltd PCIe SDXC/MMC Host Controller (rev 05)
02:00.3 FireWire (IEEE 1394): Ricoh Co Ltd R5C832 PCIe IEEE 1394 Controller (rev 04)
03:00.0 Network controller: Intel Corporation Centrino Advanced-N 6205 [Taylor Peak] (rev 34)`

# Networking

##Configurations for Intel Centrino Advanced-N 6205 Dual Band Wirless Card
03:00.0 Network controller: Intel Corporation Centrino Advanced-N 6205 [Taylor Peak] (rev 34)
Driver: iwldvm
Bands: 2.4 GHz/5 GHz
Max Speed: 300 Mbps
WiFi: 802.11a/b/g/n
Form Factor: PCIe Half MiniCard

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
            < >   Wireless RNDIS USB support
            `
            
Additional firmware for the individual device is needed:
`$ emerge --ask sys-kernel/linux-firmware`
