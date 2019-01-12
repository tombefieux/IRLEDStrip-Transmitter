# IR LED Strip - Transmitter
A simple code in Python to command LED strips with a Raspberry Pi by infrared. The LED Strips need to be controlled by [this controller](https://github.com/tombefieux/IRLEDStrip-Controller).

## Getting Started
### Prerequisites
You need first to install the LIRC Package. You can follow [this tutorial](http://www.raspberry-pi-geek.com/Archive/2015/10/Raspberry-Pi-IR-remote).
If you have issues to send commands, just copy this line below in your /boot/config.txt file and reboot.
```
dtoverlay=lirc-rpi,gpio_out_pin=22,gpio_in_pin=18,gpio_in_pull=up
```
Then, you must copy the 'lircd.conf' file in the '/etc/lirc/' directory and reboot.

### Installing
You don't need to install anything more than prerequisites and you can start to use the python class.

## Examples
If you want to send the RGB color (120, 120, 120) to the LED strip 0:
```
IRLEDStripTransmitter.sendRGBColorTo(0, 120, 120, 120)
```

And to turn if off:
```
IRLEDStripTransmitter.turnOff(0)
```