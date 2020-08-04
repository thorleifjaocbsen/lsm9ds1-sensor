# Still a work in progress!

# lsm9ds1-sensor
[<img src="https://img.shields.io/badge/Node.js-4.x%20through%207.x-brightgreen.svg">](https://nodejs.org) [<img src="https://img.shields.io/npm/v/bme280-sensor.svg">](https://www.npmjs.com/package/bme280-sensor) [![bitHound Overall Score](https://www.bithound.io/github/skylarstein/bme280-sensor/badges/score.svg)](https://www.bithound.io/github/skylarstein/bme280-sensor)


[<img src="https://cdn-learn.adafruit.com/assets/assets/000/026/680/medium800/sensors_pinout.jpg" width="150" align="right">](https://www.adafruit.com/product/2652)

Welcome to lsm9ds1-sensor, a Node.js I2C module for the STMicroelectronics LSM9DS1 Gyro, Accelerometer and Magnometer + Temperature sensor. Adafruit sells a [LSM9DS1 breakout board](https://www.adafruit.com/product/3387) and [here is the datasheet](https://learn.adafruit.com/adafruit-lsm9ds1-accelerometer-plus-gyro-plus-magnetometer-9-dof-breakout/).

This module uses [i2c-bus](https://github.com/fivdi/i2c-bus) which should provide access with Node.js on Linux boards like the Raspberry Pi Zero, 1, 2, or 3, BeagleBone, BeagleBone Black, or Intel Edison.

Note: While the LSM9DS1 device does report temperature, it is measured by the internal temperature sensor. This temperature value depends on the PCB temperature and sensor element self-heating. Therefore ambient temperature is typically reported above actual ambient temperature.

Since lsm9ds1-sensor needs to talk directly to the I2C bus and requires access to /dev/i2c, you will typically need run Node with elevated privileges or add your user account to the i2c group: ```$ sudo adduser $USER i2c```

## Example Code

```
Com\ing
```

##Example Output

```
> sudo node example.js          
Coming
```
##Example Wiring

 Adafruit have a very good example on how to wire this one up. Look at their [learning page](https://learn.adafruit.com/adafruit-lsm9ds1-accelerometer-plus-gyro-plus-magnetometer-9-dof-breakout/assembly).

 ## Credits
 This repo is somewhat build up on how Stein did his repo for the [BME280 Sensoe](https://github.com/skylarstein/bme280-sensor/). The source is also modified from SparkFun's version for the Arduino found [here](https://github.com/sparkfun/SparkFun_LSM9DS1_Arduino_Library/)