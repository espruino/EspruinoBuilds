# ESP8266 Espruino binaries
This folder contains binaries for Espruino running on the ESP8266.  The build version will be as of the date of the files in Github.

The command to flash the device is:

    esptool --port COM18 --baud 115200 write_flash  --flash_freq 40m --flash_mode qio --flash_size 4m 0x00000 ESP8266_0x00000.bin 0x10000 ESP8266_0x10000.bin

Make sure to change the COM port to match your own.

The files in the repository that you need are:

* ESP8266_0x00000.bin
* ESP8266_0x10000.bin

These are available as direct download as well as included in the [ZIP](Espruino_ESP8266_Binaries.zip) file.  If you are downloading
directly from GitHub I recommend the ZIP as reports are coming in that if you try and download
binaries directly from the web page (as opposed to checking them out from a repository), data
can be corrupted.

