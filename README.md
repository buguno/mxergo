# MX Ergo settings for Linux

This repository contains scripts for making good use of a MX Ergo mouse from Logitech in Linux.

## Packages needed

- xinput
  - xinput is a utility to list available input devices, query information about a device and change input device settings.

## Speed and Acceleration

Using xinput I set my acceleration to 0.85 so I don't have to move my finger a lot and reach the edges of my monitor.

First thing to do is run xinput to get the devices on your system, for example I get a list but all I care about is the MX Ergo

```bash
xinput --list

⎡ Virtual core pointer                          id=2    [master pointer  (3)]
⎜   ↳ **************************                id=4    [slave  pointer  (2)]
⎜   ↳ Logitech MX Ergo                          id=9    [slave  pointer  (2)]
⎜   ↳ **************************                id=13   [slave  pointer  (2)]
```

So from this, I know I need to modify device with id 9. Use next command to list MX Ergo all properties.

```bash
xinput --list-props 9

Device 'Logitech MX Ergo':
        Device Enabled (156):   1
        Coordinate Transformation Matrix (158): 1.000000, 0.000000, 0.000000, 0.000000, 1.000000, 0.000000, 0.000000, 0.000000, 1.000000
        libinput Accel Speed (303):     0.850000
```

> For didactic reasons, I ended up removing all other options from the output.

## License

Licensed under the MIT License. See [`LICENSE`](LICENSE) for more details.

