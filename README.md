# Getting Started with ESP8266 and ESP32 from Scratch
This is a beginners guide that documents the steps to getting started with the ESP boards.  Please feel free to recommend edits 
and changes through pull requests

#### Chipsets
The prominent ESP chipsets are:
* ESP8266 - supports only WiFi
* ESP32 - supports WiFi and Bluetooh

There are many varients that of these boards made by several manufacturers.  This guide works on generic boards available on Amazon / Ebay.

#### Platforms
There are several platforms that can be used to program the ESP boards:
* [Micropython](http://micropython.org/) - lightweight implementation of a Python 3 subset for microcontrollers
* NodeMCU
* Arduino

We focus on **Micropython** in this guide.


# Preparation

### Python & Pip

You will need to have Python and Pip configured.

* [TODO] Python and PIP installation for Linux / Mac
* [TODO] Python and PIP installation for Windows


### Flash Tool
To flash firmwares on ESP board, we use `esptool`: 
```bash
pip3 install esptool
```

### File Transfer
The `ampy` utility by adafruit is an easy way to transfer files to and from the ESP boards. 

```bash
pip3 install adafruit-ampy --upgrade
```

### Download Firmware Images

The generic Micropython firmwares for ESP boards can be downloaded from their site:
* [Micropython for ESP32](https://micropython.org/download#esp32)
* [Micropython for ESP8266](https://micropython.org/download#esp8266)


### Connecting the device
F
#### Mac / Linux

The device should detect automatically.  References to indicative steps are in [Installing firmware on ESP32](https://www.cnx-software.com/2017/10/16/esp32-micropython-tutorials/)

#### Windows

1.  Install the [CP210x USB to UART Bridge VCP Drivers](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)
1. 


### Connecting to Micropython REPL


# Setup
## Installing Firmware

### ESP32


#### Step 1: Insal




### Transfering files

https://techtutorialsx.com/2017/06/04/esp32-esp8266-micropython-uploading-files-to-the-file-system/




## ESP8266



# References

1. [Installing firmware on ESP32](https://www.cnx-software.com/2017/10/16/esp32-micropython-tutorials/)
1. [`Ampy` bu  for file transfer](https://techtutorialsx.com/2017/06/04/esp32-esp8266-micropython-uploading-files-to-the-file-system/)