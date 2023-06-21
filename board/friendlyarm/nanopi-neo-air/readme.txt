Intro
=====

The instructions herein are valid for the FriendlyARM NanoPi NEO Air,
both the 256MiB and 512MiB versions.

The FriendlyARM Nanopi NEO Air is a 4x4cm² board with an Allwiner H3 SoC:
  - quad-core Cortex-A7 @1.2GHz
  - 256 or 512MiB of DDR
  - uSDCard storage option
  - pre-installed 8GB eMMC
  - 2x USB 2.0 host on expansion pin-holes
  - 1x USB 2.0 OTG (also used as power source)
  - GPIOs, SPI, I2c...

Support for the Nanopi NEO Air in U-Boot and Linux is very recent, so only
core, basic features are available.


How to build
============

    $ make friendlyarm_nanopi_neo_air_defconfig
    $ make

Note: you will need access to the internet to download the required
sources.

You will then obtain an image ready to be written to your micro SDcard:

    $ dd if=output/images/sdcard.img of=/dev/sdX bs=1M

Notes:
  - replace 'sdX' with the actual device with your micro SDcard,
  - you may need to be root to do that (use 'sudo').

Insert the micro SDcard in your NanoPi NEO Air and power it up. The console
is on the serial line, 115200 8N1.
