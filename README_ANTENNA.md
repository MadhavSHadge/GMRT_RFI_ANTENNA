# Motor Control with Encoder Feedback for Arduino

This project provides an Arduino sketch to control a motor with encoder feedback. It allows for precise control of the motor's position and speed, and can handle commands sent via serial communication to set parameters and control the motor.

## Components Used

- Arduino board
- Motor driver (L298N)
- Encoder
- Power supply
- Connecting wires

## Pin Configuration

- **Motor Driver Enable Pin (PWM)**: 9
- **Motor Driver Input 1**: 8
- **Motor Driver Input 2**: 7
- **Encoder Pin A**: 2
- **Encoder Pin B**: 3

## Arduino Code

The provided Arduino sketch includes the following functionality:

- Setup and initialization of pins and interrupts.
- Conversion of pulses to maximum encoder value for a full 360-degree rotation.
- Serial communication to receive commands for setting parameters and controlling the motor.
- Functions to control motor direction, speed, and position based on encoder feedback.

### Commands

The Arduino listens for the following commands sent via serial communication:

- **'A'**: Set antenna angle
- **'P'**: Set pulse count per revolution
- **'G'**: Set gear ratio
- **'F'**: Rotate motor clockwise
- **'B'**: Rotate motor anti-clockwise
- **'D'**: Check rotation direction
- **'R'**: Reset antenna position to zero
- **'S'**: Stop the motor
- **'M'**: Set motor speed

### Functions

- **setup()**: Initializes the pins, serial communication, and encoder interrupts.
- **conversion()**: Converts pulses to maximum encoder value for a 360-degree rotation.
- **updateEncoder()**: Updates the encoder value based on the pulses received.
- **forward(int speed, long requiredPulsesforRotation)**: Rotates the motor clockwise.
- **backward(int speed, long requiredPulsesforRotation)**: Rotates the motor anti-clockwise.
- **stopMotor()**: Stops the motor.
- **directionCheck(long currentEncoderValue)**: Checks the rotation direction of the antenna.
- **requestStop()**: Software interrupt to stop the motor at any point.
- **reset(long requiredPulsesForRotation)**: Resets the antenna position to zero.

## Usage

1. Upload the provided Arduino sketch to your Arduino board.
2. Connect the motor driver, motor, and encoder to the Arduino board as per the pin configuration.
3. Open the Serial Monitor in the Arduino IDE and set the baud rate to 9600.
4. Send commands via the Serial Monitor to control the motor and set parameters.

### Example Commands

- Set antenna angle to 90 degrees:
  ```
  A90
  ```
- Set pulse count per revolution to 200:
  ```
  P200
  ```
- Set gear ratio to 2:
  ```
  G2
  ```
- Rotate motor clockwise:
  ```
  F
  ```
- Rotate motor anti-clockwise:
  ```
  B
  ```
- Check rotation direction:
  ```
  D
  ```
- Reset antenna position to zero:
  ```
  R
  ```
- Stop the motor:
  ```
  S
  ```
- Set motor speed to 150:
  ```
  M150
  ```

## Notes

- Ensure the motor driver and motor are properly connected and powered.
- Adjust the speed value (PWM) as needed for your specific motor and application.
- The encoder values are updated in real-time, and the motor control functions ensure precise movements based on the required pulses for rotation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
