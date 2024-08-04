# Flight Computer
A versatile flight computer based around (currently) the RP2040 microprocessor.
The unpopulated pin header is meant to host an
[Adafruit KB2040](https://www.adafruit.com/product/5302) as a processor
daughterboard, to reduce board complexity.

# Design Information
This design should be capable of using input voltages from 3v → 17v on the
battery input to allow for a wide range of batteries to be used. It is designed
to control and independently fire up to 3 individual high power in-flight events
(eg. ejection charges).

## Built-in Sensors
The sensor package includes a Bosch BNO055 motion co-processor for acceleration,
magnetic heading, and 3d orientation. It also includes a Bosch BME280 sensor for
pressure (along with altitude), temperature, and humidity measurements. These
sensor measurements can be used for flight control, and can also be logged to a
MicroSD card mounted on the board for ease of data recovery.

## Extensibility
Additionally, the major feature of this board is the ability to be expanded by
connecting via an I2C (and hopefully in the future CAN Bus) connection to other
boards and sensors with the same connectors. These expansion  boards could
provide additional capabilities while being modular for quickly swapping and
replacing parts.

Such capabilities could include:
 - GPS and other location packages
 - Radio transmitters for rangefinding, and telemetry
 - Additional motion sensors in other parts of the rocket
 - Controlling other electronic devices such as servos, cameras, etc.

This would allow for both expansion, and could allow for cheap sensors to be
placed in otherwise dangerous places on a rocket, where a more expensive board
would make no sense.

## Toolchain Support
All programmable components of this board were selected to be compatible with
Rust-based microcontroller frameworks like Embassy, for ease of programming and
future extension of software capabilities.

# Image
![image](https://github.com/user-attachments/assets/24aaa132-3298-4307-a318-a837f41479aa)
