This repo holds all the stuff I used to install Gentoo on my Chromebook Pixel 2. This repo is mainly personal but could be of use to others

**Contents**
* A ChromiumOS img that can be booted from usb
* The Gentoo installation iso
* Stuff to be added
    * ucm alsa confs

**Kernel**
At the moment I'm using ChromiumOS's chromeos-3.14 kernel. I've added bfs, uksm, and graysky2's gcc optimization pathes. There's a issue with
the backlight where it turns off when switching to a tty from X or leaving X. I've made a change to where it will turn back on, but I would like 
to have it never turn off during the switch. I also will be poking around more with the audio, most likely bdw-rt5677.

I would also like to track the mainline kernel's progress on support. As of 4.1-r4 I know they have thouchpad and touchscreen support. I don't 
believe they have audio support. There's also a bug that when switching to a tty from X or leaving X, you lose video sync so it looks like
everything is spinning. Suspend has also been iffy on a few kernels.

**Audio**
Speakers work but the volume is always zero when first turned on. Alsamixer always shows it at zero when launched even if there's audio playing at a
volume you can hear. Also there's not a automatic switch to headphones when plugged in.

**Grub2**
I had a issue where grub wouldn't display it's menu and possibly not even boot (can't remember). But to fix that I had to add the following to 
/etc/grub/default GRUB_GFXMODE=2560X1700

**Coreboot**
I would like to make my own coreboot image to get rid of the ugly screen, but it may be too dangerous.

