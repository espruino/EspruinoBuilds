# ESP8266 Espruino binaries
This folder contains binaries for Espruino running on the ESP8266.  The build version will be as of the date of the files in Github.

The command to flash the device is:

    esptool -bm qio -bz 512K -bf 40 -cp COM14 -cb 115200 -cd nodemcu -ca 0x00000 -cf espruino_esp8266_board_0x00000.bin -ca 0x10000 -cf espruino_esp8266_board_0x10000.bin

Make sure to change the COM port to match your own.  The COM port is supplied with the `-cp` flag parameter.

The files in the repository that you need are:

* espruino_esp8266_board_0x00000.bin
* espruino_esp8266_board_0x10000.bin

These are available as direct download as well as included in the [ZIP](espruino_esp8266_board_binaries.zip) file.  If you are downloading
directly from GitHub I recommend the ZIP as reports are coming in that if you try and download
binaries directly from the web page (as opposed to checking them out from a repository), data
can be corrupted.

----

##Tools
In order to flash the ESP8266 you will need a tool to load the binaries into the Flash of the board.   There are a number
of such tools available.  The one that will be demonstrated here is called `esptool` and can be downloaded from [here](https://github.com/igrr/esptool-ck/releases) for a variety of platforms.

Documentation on the `esptool` itself can be found [here](https://github.com/igrr/esptool-ck).

----

##ESP8266 Community and ESP8266 docs
The ESP8266 has its own dedicated community that discusses operation and programming of the
ESP8266 itself.   Since the ESP8266 has its own technologies, stories, practices and gossip ... it doesn't make sense to try and repeat those here within Espruino land.  Instead, the ESP8266 user should look to the ESP8266 community for ESP8266 specific questions.

The ESP8266 community can be found here:

[http://www.esp8266.com/](http://www.esp8266.com/)

However, we realize that we don't want to make an Espruino user have to read and digest tons and tons of knowledge in order to get their Espruino environment going.  A useful resource that is available is a free book on the ESP8266 that is available for download:

[http://neilkolban.com/tech/esp8266/](http://neilkolban.com/tech/esp8266/)

This book has chapters and sections on most major areas including flashing the devices.

What must be realized though is that there isn't a "single" best recipe for flashing an ESP8266.  The reason for that is the ESP8266 is an integrated circuit and not a __board__.  There are **many** boards available hosting ESP8266s and all of them will work with Espruino ... however the recipes on how to flash differ subtly by board and selected tool.

Here are some YouTube videos on ESP8266 flashing:

* [ESP8266 How To Flash NodeMcu Firmware](https://www.youtube.com/watch?v=Gh_pgqjfeQc)
* [ESP8266 - Getting started and connected](https://www.youtube.com/watch?v=z07zjfOHb8E)
* [Reprogramming the ESP8266 Flash](https://www.youtube.com/watch?v=cOnPWltYtQs)
* [Flash ESP8266 Firmware using esptool.py](https://www.youtube.com/watch?v=PycRnjcXMRI)