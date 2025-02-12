# VL53L0X Distance Sensor with Arduino

This project demonstrates how to interface the VL53L0X Time-of-Flight (ToF) distance sensor with an Arduino using the Wire (I2C) library. The sensor measures distances in millimeters and outputs the values via the Serial Monitor.

## Requirements
- Arduino board (e.g., Uno, Mega, Nano)
- VL53L0X distance sensor
- Jumper wires
- Arduino IDE
- VL53L0X library (available in Arduino Library Manager)

## Wiring
| VL53L0X Pin | Arduino Pin |
|------------|------------|
| VCC        | 5V         |
| GND        | GND        |
| SDA        | A4 (Uno) / Corresponding I2C SDA pin |
| SCL        | A5 (Uno) / Corresponding I2C SCL pin |

## Installation
1. Install the VL53L0X library:
   - Open Arduino IDE
   - Go to **Sketch** -> **Include Library** -> **Manage Libraries**
   - Search for **VL53L0X** and install the Adafruit or Pololu version
2. Connect the VL53L0X sensor to the Arduino as per the wiring table.
3. Upload the provided code to your Arduino board.

## Usage
- Open the Serial Monitor (**115200 baud**) to view distance readings.
- The sensor measures the distance and outputs values in millimeters.
- If a timeout occurs, the Serial Monitor will display an error message.

## Code Explanation
- Initializes the I2C communication and sensor.
- Reads distance values in a loop every 500ms.
- Detects and reports timeouts.

## Example Output
```
VL53L0X Ready!
Distance: 432 mm
Distance: 428 mm
Distance: 430 mm
Timeout occurred!
```


