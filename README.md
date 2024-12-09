# Tutorial-BMP280
Files used for the Tutorial that shows how to read an Adafruit BMP280 temperature / pressure sensor.

main.cpp reads only temperature, to keep it simple, and to make it possible to simply clone / download and build.
Out of the box this project did not build in VScode/PlatformIO without the modifications made in ET1_Build.log
	Branch-->ESP32-devkit-v1-boards
		Changes in this branch required to get my two ESP32_devkit_v1 processor boards to behave properly. 
Boards passing [NULL] field for temperature: Got sensor to read and pass something akin to temp data to SignalK but readings don't change and are equal to 0+kelvin translation statement. Realized i have BME280 sensors not BMP! modified addressing in tutorial's main.cpp and sledge hammered it into submission.  do not merge this branch to MAIN until the libraries are modified for the sensors i have.  Arduino.BME library should exist and it should work without passing a hard coded address and ID for bmp280.begin(0x76,0x60);
