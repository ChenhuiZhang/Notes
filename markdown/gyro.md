# Gyro

[TOC]

## Module

- [ICM20600](https://www.invensense.com/wp-content/uploads/2015/12/DS-000184-ICM-20600-v1.0.pdf)

## Code

- drivers/iio/imu/inv_mpu6050
- patches for WoM/Temp in meta-axel

## Framework

- [IIO](https://wiki.analog.com/software/linux/docs/iio/iio)

## Interfaces

The Gyro driver provide the standard iio interface for below data:

- Gyroscope - X/Y/Z
- Temperature sensor
- Accelerometer - X/Y/Z


## Tools

- tools/iio in kernel

  - Build
  ```
  cd tools/iio
  make CROSS_COMPILE=aarch64-linux-gnu-
  ```
  
  - Run
  
  * Enable all channels and read the data in 100 times:
  ```
  iio_generic_buffer -a -N 0 -c 100
  ```
  
  * Enable only temperature sensor and anglvel_z channel:
  
  ```
  echo 1 > /sys/bus/iio/devices/iio\:device0/scan_elements/in_temp_en
  echo 1 > /sys/bus/iio/devices/iio\:device0/scan_elements/in_anglvel_z_en
  iio_generic_buffer -N 0 -c 100
  ```
  
- [libiio](https://wiki.analog.com/resources/tools-software/linux-software/libiio)
- [iio_oscilloscope](https://wiki.analog.com/resources/tools-software/linux-software/iio_oscilloscope)


