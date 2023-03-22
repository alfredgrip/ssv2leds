# SteelSeries Siberia v2 headset LEDs control tool

**This is a forked version with updated descriptions, since some were outdated**

## Why?

SteelSeries software supports Windows and MacOSX.
This tool is able control headset's LEDs in Linux.

## Supported hardware

Original author: "I tested SteelSeries Siberia v2 Frost Blue only."
It works with SteelSeries Siberia v2 Heat Orange too

## Requirements

* Go compiler
* libusb >= 1.0

```bash
sudo apt install golang-go libusb-1.0-0-dev libusb-1.0-0
```

## Instalation

```bash
git clone git://github.com/antage/ssv2leds.git
cd ssv2leds
go install github.com/hanwen/go-mtpfs@latest
go mod init example.com/m
go mod tidy
go build
sudo install -m 0644 m /usr/local/bin/ssv2leds
```

## Usage
(Run as `sudo`)

Turn off LEDs:
```
ssv2leds -i 0
```

Maximal brightness:
```
ssv2leds -i 255
```

Medium brightness:
```
ssv2leds -i 128
```

Set pulsation mode:
```
ssv2leds -p slow
```


Pulsation modes:

* steady - LEDs are on always
* slow - slow pulsation
* medium - medium pulastion
* fast - fast pulsation
* trigger - I don't know

