# Arduino mkr1010 Environment Sensor to API server
This is an IoT project to use an Arduino mkr1010 with a BME 085 and a TSL 2561 sensors to post environment data to a secured API server.

The Arduino mkr1010 is programmed to make GET and POST over TLS using WiFi to a node js Express API server storing the data on MongoDB.

The JWT Json Web Token module is used to authenticate the sensor data the Arduino is sending by issuing and short life token to do so.

The Deep Sleep function on the mkr1010 is used as the device is solar powered with a 6w solar panel and a 1400mA/h LiPo battery.

The device wakes up every 5 minutes to authenticate and receive its token.

Gather the sensor data and finaly post the data to the API server using the token provided to do so, then going back to sleep.
