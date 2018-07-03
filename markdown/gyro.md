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

The Gyro driver provide the standard iio channels as below:

- Accelerometer - X/Y/Z
- Temperature sensor
- Gyroscope - X/Y/Z
- Timestamp

The accelrometer channel also support the event feature which used as WoM in
ICM20600. 

The temperature sensor also can export as a HWMON interface as below:

```
186         iio-hwmon {
187                 compatible = "iio-hwmon";
188                 io-channels = <&gyro 3>;
189         };
```

The temperature value can be read from:

```
cat /sys/class/hwmon/hwmon0/temp1_input
```

## Tools

- tools/iio in kernel

  - Build
  ```
  cd tools/iio
  make CROSS_COMPILE=aarch64-linux-gnu-
  ```
  
  - Enable all channels and read the data in 100 times:
  ```
  iio_generic_buffer -a -N 0 -c 100
  ```
  
  - Enable only temperature sensor and anglvel_z channel:
  ```
  echo 1 > /sys/bus/iio/devices/iio\:device0/scan_elements/in_temp_en
  echo 1 > /sys/bus/iio/devices/iio\:device0/scan_elements/in_anglvel_z_en
  iio_generic_buffer -N 0 -c 100
  ```
  
  - Enable WoM in axis X and set the threshold to 100:
  ```
  echo 1 > /sys/bus/iio/devices/iio\:device0/events/in_accel_x_thresh_either_en
  echo 100 > /sys/bus/iio/devices/iio\:device0/events/in_accel_x_thresh_either_value
  ```
  
  Then you can monitor the event from X axis is the motion is over threshold:
  ```
  iio_event_monitor icm20600
  ```
  
- [libiio](https://wiki.analog.com/resources/tools-software/linux-software/libiio)
- [iio_oscilloscope](https://wiki.analog.com/resources/tools-software/linux-software/iio_oscilloscope)


