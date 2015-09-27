# ESP8266 Espruino binaries
This folder contains binaries for Espruino running on the ESP8266.  The build version will be as of the date of the files in Github.

The command to flash the device is:

    esptool -bm qio -bz 512K -bf 40 -cp COM14 -cb 115200 -cd nodemcu -ca 0x00000 -cf ESP8266_0x00000.bin -ca 0x10000 -cf ESP8266_0x10000.bin

Make sure to change the COM port to match your own.  The COM port is supplied with the `-cp` flag parameter.

The files in the repository that you need are:

* ESP8266_0x00000.bin
* ESP8266_0x10000.bin

These are available as direct download as well as included in the [ZIP](Espruino_ESP8266_Binaries.zip) file.  If you are downloading
directly from GitHub I recommend the ZIP as reports are coming in that if you try and download
binaries directly from the web page (as opposed to checking them out from a repository), data
can be corrupted.

----

##Tools
In order to flash the ESP8266 you will need a tool to load the binaries into the Flash of the board.   There are a number
of such tools available.  The one that will be demonstrated here is called `esptool` and can be downloaded from [here](https://github.com/igrr/esptool-ck/releases) for a variety of platforms.

Documentation on the `esptool` itself can be found [here](https://github.com/igrr/esptool-ck).