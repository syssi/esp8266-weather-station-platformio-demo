# esp8266-weather-station-platformio-demo

Please read http://blog.squix.org/2016/06/new-weather-station-demo-on-github.html for more information

## Setup

```
# Install platformio https://docs.platformio.org/en/latest/installation.html#python-package-manager
$ pip install platformio

# Clone this repository
$ git clone https://github.com/syssi/esp8266-weather-station-platformio-demo
Cloning into 'esp8266-weather-station-platformio-demo'...
remote: Enumerating objects: 6, done.
remote: Counting objects: 100% (6/6), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 24 (delta 0), reused 2 (delta 0), pack-reused 18
Unpacking objects: 100% (24/24), done.

$ cd esp8266-weather-station-platformio-demo

# Edit src/main.and update WIFI_SSID, WIFI_PWD, TZ, SDA_PIN, SDC_PIN, OPEN_WEATHER_MAP_APP_ID, OPEN_WEATHER_MAP_LOCATION_ID
# How to create OpenWeatherMap API key: https://docs.thingpulse.com/how-tos/openweathermap-key/

# Build and flash
$ platformio run --target upload --upload-port /dev/ttyUSB0
Processing d1_mini (framework: arduino; platform: espressif; board: d1_mini)
-------------------------------------------------------------------------------------------------------
Detected non-PlatformIO `lib_install` option in `[env:d1_mini]` section
Warning! Platform `espressif` is deprecated and will be removed in the next release! Please use `espressif8266` instead.
Verbose mode can be enabled via `-v, --verbose` option
CONFIGURATION: https://docs.platformio.org/page/boards/espressif8266/d1_mini.html
PLATFORM: Espressif 8266 > WeMos D1 R2 & mini
HARDWARE: ESP8266 80MHz 80KB RAM (4MB Flash)
Library Dependency Finder -> http://bit.ly/configure-pio-ldf
LDF MODES: FINDER(chain) COMPATIBILITY(soft)
Collected 30 compatible libraries
Scanning dependencies...
Dependency Graph
|-- <ESP8266_SSD1306> 4.0.0
|   |-- <Wire> 1.0
|-- <WeatherStation> 1.6.5
|   |-- <JsonStreamingParser> 1.0.5
|   |-- <ESP8266HTTPClient> 1.1
|   |   |-- <ESP8266WiFi> 1.0
|   |-- <ESP8266WiFi> 1.0
|-- <JsonStreamingParser> 1.0.5
|-- <Wire> 1.0
Retrieving maximum program size .pioenvs/d1_mini/firmware.elf
Checking size .pioenvs/d1_mini/firmware.elf
Memory Usage -> http://bit.ly/pio-memory-usage
DATA:    [====      ]  37.9% (used 31052 bytes from 81920 bytes)
PROGRAM: [===       ]  30.9% (used 322324 bytes from 1044464 bytes)
Configuring upload protocol...
Looking for upload port...
Use manually specified: /dev/ttyUSB0
Uploading .pioenvs/d1_mini/firmware.bin
Uploading 326464 bytes from .pioenvs/d1_mini/firmware.bin to flash at 0x00000000
................................................................................ [ 25% ]
................................................................................ [ 50% ]
................................................................................ [ 75% ]
...............................................................................  [ 100% ]
==================================== [SUCCESS] Took 23.29 seconds ====================================

```
