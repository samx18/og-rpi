# The Open Guide to Raspberry Pi

## How - To
[Create bootable disk](#Create-a-bootable-SD-Card-Image)

### Create a bootable SD Card Image

Create a bootable SD card image for raspberry pi

**Get the official image**

Download from

https://www.raspberrypi.org/downloads/raspbian/

Recommended method via torrents

**Discover your card (Optional)**

Once you have attached the card to your laptop, you might need to find it if it does not show up automatically. Most windows and mac users may not need to do the below steps

`df -h`  or `fdisk -l`

**Unmount your card (Optional)**

`sudo umount /dev/sdd1`

**Copy the image**

Make sure to use the whole device name like sdd and not partion name like sdd1

`dd bs=4M if=2017-09-07-raspbian-stretch.img of=/dev/sdd conv=fsync`

If you face issuse with 4M try 1M

**GUI programs**

You can also use GUI programs like etcher to automatically format and copy the image to your SD card.

https://etcher.io/

### Finding the RPi on your network

If you want to quickly discover the IP address of your raspberry pi. This obviously will work only if you are on the same network as your rasppberry pi.

```
% arp -na | grep -i b8:27:eb
? (192.168.1.89) at b8:27:eb:1a:bd:ca on en0 ifscope [ethernet]
? (192.168.1.92) at b8:27:eb:62:6e:4 on en0 ifscope [ethernet]
```
