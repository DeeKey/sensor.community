---
title: Install the firmware
---

You do not have to program, don’t worry!
We already programmed the firmware. You only have to installed it on the NodeMCU (ESP8288). Managable for computer beginners.

If you take a look inside the [sapper-template](https://github.com/sveltejs/sapper-template) repo, you'll see some files that Sapper expects to find:

```bash
├ package.json
├ src
│ ├ routes
│ │ ├ # your routes here
│ │ ├ _error.svelte
│ │ └ index.svelte
│ ├ client.js
│ ├ server.js
│ ├ service-worker.js
│ └ template.html
├ static
│ ├ # your files here
└ rollup.config.js / webpack.config.js
```

When you first run Sapper, it will create an additional `__sapper__` directory containing generated files.

You'll notice a few extra files and a `cypress` directory which relates to [testing](docs#Testing) — we don't need to worry about those right now.

> You *can* create these files from scratch, but it's much better to use the template. See [getting started](docs#Getting_started) for instructions on how to easily clone it


### Firmware Windows

#### Download and install drivers for Windows
To communicate with the ESP8266 you need usb2serial drivers. The chipset for NocdeMCUs is usually CH341. Choose the link that corresponds to the operating system of your computer.

#### Drivers for the old V2 model (CP2102) for Windows
* Windows 10: https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip
* Windows 7/8/8/8/8.1: https://www.silabs.com/documents/public/software/CP210x_Windows_Drivers.zip (32-bit version not supported for 64-bit version of system)

#### Driver for model V3 (CH341) for Windows
* Windows: http://www.wch.cn/downloads/file/5.html

#### Extract the downloaded file for Windows. Unpack it:
* for V2: Open the folder CP210x and double click on the application CP210xVCPInstaller_x64 (or x86)
* for V3: open the folder CH341SER and double click on the application SETUP.

### Download Firmware Flasher for Windows
Download Firmware Flasher Tool   
* Windows (64-bit): https://luftdaten.info/flashtool/luftdaten-tool.zip
* Source Code: https://github.com/opendata-stuttgart/airrohr-firmware-flasher

### Install Firmware for Windows
Now connect the NodeMCU to the computer with a short micro-USB cable (the cable should not be longer than 1m, otherwise the installation may fail). Select the latest version latest_en.bin (or another language version) and click “Upload”.
Wait until the process is done and done. Now we assemble the sensor.

A big thank you goes to [Piotr, from Poland](https://dropbox.inf.re/), for his help! 🙋‍♂️ 


### Firmware MacOS

#### Download and install drivers for MacOS
To communicate with the ESP8266 you need usb2serial drivers. The chipset for NocdeMCUs is usually CH341. Choose the link that corresponds to the operating system of your computer.

#### MacOS Drivers for the old V2 model (CP2102)
* MacOS: https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip (restart computer after installation)

#### MacOS Driver for model V3 (CH341)
* MacOS: http://www.wch.cn/downloads/file/178.html (restart your computer after installation)

#### Extract the downloaded file for MacOS. Unpack it:
* for V2: Open the folder CP210x and double click on the application CP210xVCPInstaller_x64 (or x86)
* for V3: open the folder CH341SER and double click on the application SETUP.

### Download Firmware Flasher for MacOS
Download Firmware Flasher Tool   
* MacOS: https://luftdaten.info/flashtool/luftdaten-tool.dmg
* Source Code: https://github.com/opendata-stuttgart/airrohr-firmware-flasher

### Install Firmware for MacOS
Now connect the NodeMCU to the computer with a short micro-USB cable (the cable should not be longer than 1m, otherwise the installation may fail). Select the latest version latest_en.bin (or another language version) and click “Upload”.
Wait until the process is done and done. Now we assemble the sensor.

A big thank you goes to [Piotr, from Poland](https://dropbox.inf.re/), for his help! 🙋‍♂️ 


### Firmware Linux

#### Download and install drivers for Linux 
To communicate with the ESP8266 you need usb2serial drivers. The chipset for NocdeMCUs is usually CH341. Choose the link that corresponds to the operating system of your computer.

#### Drivers for the old V2 model (CP2102) & V3 (CH341)
No drivers need to be installed. Chip should be supported directly (verifiable with dmesg)

#### Driver for model V3 (CH341)
* MacOS: http://www.wch.cn/downloads/file/178.html (restart your computer after installation)

#### Extract the downloaded file for Linux. Unpack it:
Download Firmware Flasher Tool   
* Linux (64-bit): https://luftdaten.info/flashtool/luftdaten-tool.linux-x64
* Source Code: https://github.com/opendata-stuttgart/airrohr-firmware-flasher

### Download Firmware Flasher for Linux
Download Firmware Flasher Tool   
* Linux (64-bit): https://luftdaten.info/flashtool/luftdaten-tool.linux-x64
* Source Code: https://github.com/opendata-stuttgart/airrohr-firmware-flasher

### Install Firmware for Linux 
Now connect the NodeMCU to the computer with a short micro-USB cable (the cable should not be longer than 1m, otherwise the installation may fail). Select the latest version latest_en.bin (or another language version) and click “Upload”.
Wait until the process is done and done. Now we assemble the sensor.

A big thank you goes to [Piotr, from Poland](https://dropbox.inf.re/), for his help! 🙋‍♂️ 
