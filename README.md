# M3D Fio
OctoPrint plugin for the Micro 3D printer that provides a complete, platform independent alternative to the printer's official software 

© 2015 Exploit Kings. All rights reserved.

You can install it with OctoPrint's built in plugin manager. The URL for that is [https://github.com/donovan6000/M3D-Fio/archive/master.zip](https://github.com/donovan6000/M3D-Fio/archive/master.zip) or you can install it manually with the command

```shell
pip install https://github.com/donovan6000/M3D-Fio/archive/master.zip
```

OctoPrint's autodetect serial port and baudrate feature doesn't work with the Micro 3D printer, so you'll need to manually set the baudrate to `115200` and the serial port to something like `COMx` for Windows, `/dev/ttyACMx` for Linux, or `/dev/tty.usbmodemxxxx` for OS X.

If your using Windows and the printer isn't recognized in the device manager, then you'll need to install the drivers manually which are located in `/drivers/Windows/`.

If you are using Linux, the 90-m3d-local.rules needs to applied in order to avoid issues. You can apply it with the following commands:

```shell
wget -O /etc/udev/rules.d/90-m3d-local.rules https://raw.githubusercontent.com/donovan6000/M3D-Fio/master/drivers/Linux/90-m3d-local.rules
sudo /etc/init.d/udev restart
```
