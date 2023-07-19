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

## Requirements

In order to build dwm you need the Xlib header files.

## Installation

Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):
``` sh
make clean install
```

##Running dwm

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