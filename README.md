# Flight Computer
A versatile, inexpensive, modular, and **open source** flight computer and altimeter
system for amateur and experimental rocketry.

All designs in this repository are licensed under the [**CERN-OHL-S v2 or any later 
version**](https://ohwr.org/project/cernohl/-/wikis/uploads/b236492596cfc91c12def7d50bbf7da0/cern_ohl_s_v2.pdf). 
Contributions are welcome!

# Core Board
This design should be capable of using input voltages from 3v → 16v on the
battery input to allow for a wide range of batteries to be used. It is designed
to control and independently fire up to 3 individual high power in-flight events
(eg. ejection charges).

## Built-in Sensors
The sensor package includes a Bosch BNO055 motion co-processor for acceleration,
magnetic heading, and 3d orientation. It also includes a Bosch BME280 sensor for
pressure (along with altitude), temperature, and humidity measurements. These
sensor measurements can be used for flight control, and can also be logged to a
MicroSD card mounted on the board for ease of data recovery.

## Toolchain Support
All programmable components of this board were selected to be compatible with
Rust-based microcontroller frameworks like Embassy, for ease of programming and
future extension of software capabilities.

## Images
![front](https://github.com/user-attachments/assets/3bca23d6-af98-49bf-b8da-e52f9ee6c4af)

![back](https://github.com/user-attachments/assets/7c1cdd4c-f01e-4e7c-a63b-401bbc89d1e1)

# Expansion Modules
A major feature of the Core Board is the ability to be expanded by
connecting via an I2C (and hopefully in the future CAN Bus) connection to other
boards and sensors with the same connectors. These expansion  boards could
provide additional capabilities while being modular for quickly swapping and
replacing parts.

The connectors on the Core Board are compatible with any Adafruit Stemma QT or 
SparkFun Qwiic board, which immediately provides for a lot of options for
sensors without any design or soldering work needed.

In the future, this repository will host the KiCad files for expansion boards
created by UNL Aerospace Rocketry.
