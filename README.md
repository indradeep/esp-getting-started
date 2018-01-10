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



## Connecting the device

### Mac / Linux

The device should detect automatically.  References to indicative steps are in [Installing firmware on ESP32](https://www.cnx-software.com/2017/10/16/esp32-micropython-tutorials/)

[TODO] Instructions on installing the device and finding port

### Windows

1.  Install the [CP210x USB to UART Bridge VCP Drivers](https://www.silabs.com/products/development-tools/software/usb-to-uart-bridge-vcp-drivers)
1. Connect Device
1. Open Device Manager
1. Under Ports, note the port for `Silicon Labs CP210x USB to UART Bridge` (e.g. COM4)

If you use Windows Subsystem for Linux (WSL), the COM ports are mapped under `/dev/ttyS<COM PORT #>`.  For example, `COM4` will be `/dev/ttyS4`.

## Download Firmware Images

The generic Micropython firmwares for ESP boards can be downloaded from their site:
* [Micropython for ESP32](https://micropython.org/download#esp32)
* [Micropython for ESP8266](https://micropython.org/download#esp8266)

## Installing micropython

1. Install `esptool` to flash firmwares: 
    ```bash
    pip3 install esptool --upgrade
    ```

1. Erase the ESP flash:
    ```bash
    esptool.py --port <port or device> erase_flash

    # Examples:
    #  - Windows: esptool.py --port COM4 erase_flash
    #  - WSL Example: esptool.py --port /dev/ttyS4 erase_flash
    #  - Mac / Linux: esptool.py --port /dev/ttyUSB0 erase_flash
    ```
    On Mac / Linux / WSL, you may need to run the command with `sudo`

1. Install Micrpython Firmware:

    For ease, copy over the downloaded micropython firmware to the current directory.
    ```bash
    # ESP 32 Only
    esptool.py --chip esp32 --port <port or device> write_flash -z 0x1000 <path to micropython firmware binary>

    # Example:
    # esptool.py --chip esp32 --port /dev/ttyUSB0 write_flash -z 0x1000 esp32-20180107-v1.9.3-238-g42c4dd09.bin
    ```

    ```bash
    # ESP 8266 Only
    esptool.py --port <port or device> --baud 460800 write_flash --flash_size=detect 0 <path to micropython firmware binary>

    # Example:
    # esptool.py --port COM4 --baud 460800 write_flash --flash_size=detect 0 esp8266-20170108-v1.8.7.bin
    ```

## Connecting to Micropython REPL
A common way to get to the Micropython Read Execute Print Loop (REPL), is using the serial connection over USB.  

### Windows
1. Download and install [Putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)
1. Open putty, and set the following:
    * Connection type: `Serial`
    * Serial Line: `COM<Port#>` (e.g. COM4)
    * Speed: `115200`
1. Click `Open` to connect


### Mac / Linux
1. Install Picocom: `sudo apt install picocom`





# Setup
## Installing Firmware

### ESP32


#### Step 1: Insal




### Transfering files

1. Install `ampy` utility for transfering files to and fro: 
    ```bash
    pip3 install adafruit-ampy --upgrade
    ```


https://techtutorialsx.com/2017/06/04/esp32-esp8266-micropython-uploading-files-to-the-file-system/




## ESP8266



# References

1. [Installing firmware on ESP32](https://www.cnx-software.com/2017/10/16/esp32-micropython-tutorials/)
1. [`Ampy` bu  for file transfer](https://techtutorialsx.com/2017/06/04/esp32-esp8266-micropython-uploading-files-to-the-file-system/)