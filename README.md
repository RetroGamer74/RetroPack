# RetroPack

(Para leer esta información en Español pulsa [aquí](readme_es.md)
RetroPack - Image with RetroReloaded + Emunand + Android

# Why RetroPack?

Simple. Instead having 2 SD cards, one for switch, and one for android, RetroPack brings you both solutions in one SD.

# Partitions Size

Some of you want to know how the size is shared between partitions. So here is the layout I'm using:

emuMMC requires around 30 GBytes.
Android requires around 20 Gbytes.
The rest is used for the common FAT32 partition we use for switch, to store homebrew, retroreloaded, atmosphere, games and so on.

So this is basically the layout. If you own 64 GBytes sd Card, you can guess in this case Switch partition will be around 14 Gbytes, in case of 128 GBytes, will be around 78 GBytes, and for 256 GBytes, it should be around 206 Gigabytes.

Always the biggest partition is the FAT32 used for switch because when using only one SD card Android will be able to get access to this big partition, so we don't need to make a bigger userdata partition for Android.

# Installation

Because of the heavy work to prepare the partitions, and the mandatory use of Linux to do it, I thought the best way would be to pack the result in an image ready for download.

And it is like that.

There will be 2 flavors of RetroPack and several options depending of what you want and the size of your microSD card.

For booting the final SD, copy the payload.bin existing in the HOS_DATA partition and copy it into your PC, and use TegraRCMGUI. Remember!! Do not remove the payload.bin from the SD.
For people using Dongle, just boot with your dongle referencing the payload.bin existing in the root of the SD.

## Flavour Red ( RetroPack Red )

RetroPack Red is ready to use with EmuMMC and Android. Partition for EmuMMC is already reserved to be installed.

### Steps for red flavours

Flash the image into your SD card using EtcherBalena.

Here is the link: [Etcher-Balena](https://www.balena.io/etcher/)

Select image file -> Select your microSD destination -> Flash

1 .- The first time you boot up RetroPack, which in fact will boot using RetroReloaded, you will see there is no emunand button close to Atmosphere icon. This is because emummc must be created from your own switch.

![alt text](rr_boot_v2_noemu.png)

To do this, you have to touch Hekate option.

2.- Once in Hekate, touch emuMMC option.

![alt text](hekate1.png)

3.- On the right side, touch, Create emuMMC

![alt text](hekate2.png)

4.- Now select SD Partition button.

5.- Then continue.

6.- And that's all. When the procedure ends, which usually takes around 10 minutes, you can touch Close at the right top corner, and press Back to RR in the footer, to reload RetroReloaded again.

![alt text](rr_boot_v2.jpg)

7.- Once on RetroReloaded you will see this time emunand button.

8.- For booting up Android, just touch Hekate button, and in the Launch option, select in the right side SwitchRoot Android.

#### Your download

Here is the link to all the RetroPack packages. Remember to select your Flavour and Size for your microSD.

Note: By the way just RetroPack Red for 128 Gb is available. I'm currently working creating the other sizes.

[RetroPack Images](https://mega.nz/#F!TvYyGS5D!4CRLomt3FVgD2c4UvcB_fQ)

## Flavour Blue ( RetroPack Blue )

RetroPack Blue is ready use for RetroReloaded and Android only. It doesn't provide a partition ready to install emuMMC. So if you want RetroReloaded + emuMMC + Android, then you need RetroPack Red.

### Steps for blue flavours

Flash the image into your SD card using EtcherBalena.

Here is the link: [Etcher-Balena](https://www.balena.io/etcher/)

Select image file -> Select your microSD destination -> Flash

1.- Download your image according to your microSD size and that's all.

![alt text](rr_boot_v2_noemu.png)

Remember, by the way, you will find the Android launcher in Hekate => Launch option.

2.- So, from the first screen of RetroPack, which is RetroReloaded interface, touch Hekate.

![alt text](hekate1.png)

3.- Once in Hekate touch Launch option.

4.- At the right side is the icon for SwitchRoot Android.

#### Your download

Here is the link to all the RetroPack packages. Remember to select your Flavour and Size for your microSD.

Note: By the way just RetroPack Red for 128 Gb is available. I'm currently working creating the other sizes.

[RetroPack Images](https://mega.nz/#F!TvYyGS5D!4CRLomt3FVgD2c4UvcB_fQ)

