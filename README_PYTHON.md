# Motor Control GUI Application

This Python application provides a graphical user interface (GUI) for controlling a motor through an Arduino. 
The GUI allows users to set various motor parameters, control the motor's direction and speed, and read encoder values.
The application communicates with the Arduino via serial communication.

## Features

- **Set Pulses Per Revolution**: Configure the encoder settings.
- **Set Gear Ratio**: Define the gear ratio for the antenna.
- **Set Antenna Angle**: Specify the rotation angle in degrees.
- **Set Clock For Rotation**: Set a timer to control the duration of rotation.
- **Direction Controls**: Rotate the motor clockwise or anticlockwise.
- **Speed Controls**: Set and display the motor's speed.
- **Read Encoder Value**: Read the current value from the encoder.
- **Submit and Reset Parameters**: Submit motor parameters to the Arduino and reset all settings.
- **Dark Mode**: The application features a dark mode theme for better visibility and user experience.
- **Logging**: Log all actions and commands sent to the Arduino for record-keeping and debugging purposes.

## Requirements

- Python 3.x
- PyQt5
- pyserial

## Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/motor-control-gui.git
    cd motor-control-gui
    ```

2. **Install Dependencies**:
    ```bash
    pip install PyQt5 pyserial
    ```

## Usage

1. **Connect the Arduino**: Ensure your Arduino is connected to your computer via USB. Adjust the serial port in the code if necessary (default is `/dev/ttyUSB0`).

2. **Run the Application**:
    ```bash
    python motor_control_gui.py
    ```

3. **Use the GUI**:
    - **Encoder Settings**: Enter the pulses per revolution and click "Submit Pulses".
    - **Gear Ratio**: Enter the gear ratio and click "Submit Gear Ratio".
    - **Antenna Angle**: Enter the desired rotation angle and click "Submit Angle".
    - **Set Clock for Rotation**: Enter hours, minutes, and seconds, then click the appropriate buttons to start or stop the timer.
    - **Direction Controls**: Click "Clockwise" or "Anticlockwise" to rotate the motor in the desired direction.
    - **Speed Controls**: Set the speed using the calculated PWM value and click "Speed Set".
    - **Encoder Value**: Click "Read Encoder Value" to read the current encoder value.
    - **Submit Parameters**: Click "Submit Parameters" to send all settings to the Arduino.
    - **Reset Parameters**: Click "Reset Parameters" to clear all settings.
    - **Reset Antenna Position**: Click "Reset Antenna Position" to reset the antenna position to the encoder count of 0.

## File Structure

- `motor_control_gui.py`: Main application code.
- `motor_settings.txt`: File to save and load motor settings.
- `motor_logs/`: Directory to store log files.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## Issues


For any questions or feedback, please contact madhavhadge@gmail.com.

---
