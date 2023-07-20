# dwm - dynamic window manager

dwm is an extremely fast, small, and dynamic window manager for X.

## Patches
- [xresources](https://dwm.suckless.org/patches/xresources/)
    allows to handle settings from Xresources
- [attachbottom](https://dwm.suckless.org/patches/xresources/)
    new clients attach at the bottom of the stack
- [actualfullscreen](https://dwm.suckless.org/patches/actualfullscreen/)
    actually fullscreen window instead of toggling status bar and monocle layout
- [warp](https://dwm.suckless.org/patches/warp/)
    warps mouse cursor to center of focused window
- [pertag](https://dwm.suckless.org/patches/pertag/)
    keeps layout, mwfact, barpos, nmaster per tag
- [gaps](https://dwm.suckless.org/patches/ru_gaps/)
    adds runtime resizable, useless gaps
- [save floats](https://dwm.suckless.org/patches/save_floats/)
    saves size and position of every floating window

## Installation
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

To install dwm from suckless on Debian based systems, you'll need to install a few dependencies and build it from source. Here are the packages you'll need to install:

1. Xorg: Install the Xorg display server:
```sh
sudo apt update
sudo apt install xorg
```

2. Build tools: Install the necessary build tools to compile dwm:
```sh
sudo apt install build-essential
```

3. X11 development headers: Install the development headers for X11:
```sh
sudo apt install libx11-dev libxft-dev libxinerama-dev
```
Once you have installed these packages, you can proceed to download and build dwm. Here are the steps:

1. Download dwm source code:
```sh
git clone https://github.com/alibehrozi/dwm.git
```

2. Change to the dwm directory:
```sh
cd dwm
```

Edit the config.def.h file according to your preferences, if needed.

3. Build and install dwm:
```sh
make
sudo make install
```

## Running dwm

Add the following line to your .xinitrc to start dwm using startx:
``` sh
exec dwm
```
In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:
``` sh
DISPLAY=foo.bar:1 exec dwm
```
(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:
``` sh
while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
do
	sleep 1
done &
exec dwm
```

## Configuration

The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.