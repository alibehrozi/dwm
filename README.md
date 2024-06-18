# dwm - Dynamic Window Manager
dwm is a lightweight, efficient dynamic window manager for X, optimizing window layouts for responsiveness and productivity.

## Installation

To install dwm on Arch Linux, follow these steps:

1. Install Dependencies

First, ensure that you have all the necessary dependencies installed. You can do this by running the following command:

```sh
sudo pacman -S base-devel libx11 libxft libxinerama xorg-server xorg-xinit fontconfig freetype2
```

### Once you have installed these packages, you can proceed to download and build dwm. Here are the steps:

2. Download dwm source code:
```sh
git clone https://github.com/alibehrozi/dwm.git
```

3. Change to the dwm directory:
```sh
cd dwm
```

Edit the config.def.h file according to your preferences, if needed.

4. Build and install dwm:
```sh
sudo make clean install
```

## Running dwm

To start dwm using `startx`, add the following line to your `.xinitrc`:
```sh
echo "exec dwm" >> ~/.xinitrc
```