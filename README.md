# ZOSI IPcam
I have ZOSI 360 degree rotation IPcam. Model 1ND-5122M-W-EU https://www.zositech.com/product/1080p-hd-wireless-ip-camera-with-two-way-audio-for-pet-baby-monitor/
This camera has 2Mp based on Hi3518-ERBCV200 processor and SC2235 sensor with RTL8188ETV Realtek wifi module. Onvif, telnet and up to 128Gb SD card supporting are on board.

The most often described issue with it is "freezing" after SD card removing. I have found the solution for this case. It looks like camera makes selftest by rotating after supplied power but nothing to do more. It doesn't respond on own ZosiApp and others Onvif Apps too. Hard reset button does'n work in this case. But the camera is presented on network in fact.

1. remove SD card
2. connect to camera IP adress by telnet
3. use login root password 123456asj
4. obsreve SD mount point cd /mnt/mmc1
5. delete folder YYYYMMDD with content rm -r ./FOLDERNAME
6. reboot

The main reason that this folder occupies all free space in memory and camera can't boot as usual. Main modules and lib are not run at all.
See attached pictures if you want to use UART in original topic in russian by link https://www.forum.videon.spb.ru/viewtopic.php?f=24&t=14163
