# Temperature Monitoring System

This project uses a Dallas DS18B20 temperature sensor to monitor the temperature in real-time. The system displays the temperature on a 16x2 LCD and triggers an alert (red LED and buzzer) when the temperature exceeds 38°C. A green LED indicates normal temperature conditions.

## 🔧 Hardware Components

- Arduino Uno (or compatible board)
- 1 x Dallas DS18B20 Temperature Sensor
- 1 x 16x2 I2C LCD Display
- 1 x Red LED
- 1 x Green LED
- 1 x Buzzer
- Resistors
- Breadboard and jumper wires

## 📚 Libraries Required

To use this project, you need to install the following libraries:

1. **OneWire** - For communication with the Dallas DS18B20 sensor.
   - Install via the Library Manager: **Sketch > Include Library > Manage Libraries** and search for "OneWire".

2. **DallasTemperature** - For reading temperatures from the DS18B20 sensor.
   - Install via the Library Manager: **Sketch > Include Library > Manage Libraries** and search for "DallasTemperature".

3. **LiquidCrystal_I2C** - For controlling the 16x2 LCD display via I2C.
   - Install via the Library Manager: **Sketch > Include Library > Manage Libraries** and search for "LiquidCrystal_I2C".

## 🧠 Functionality

- **Temperature Display**: The current temperature is displayed on the LCD.
- **Alert Trigger**: If the temperature exceeds 38°C, a red LED lights up and a buzzer sounds for 1 second.
- **Normal Condition**: A green LED is illuminated when the temperature is within the safe range.
- **Serial Monitor**: Displays the temperature readings in real-time.

## 📋 Pin Configuration

| Component         | Arduino Pin |
|-------------------|-------------|
| DS18B20 Sensor    | Pin 2       |
| Red LED           | Pin 9       |
| Green LED         | Pin 8       |
| Buzzer            | Pin 10      |

## 🛠️ Setup

1. Connect the Dallas DS18B20 sensor to Pin 2.
2. Connect the Red LED to Pin 9, the Green LED to Pin 8, and the Buzzer to Pin 10.
3. Set up the 16x2 LCD display using the I2C interface.
4. Install the required libraries listed above.
5. Upload the provided code to the Arduino.

## 🧑‍💻 How It Works

- The system reads the temperature every 100 ms (10 times per second).
- If the temperature exceeds 38°C, the red LED and buzzer activate to indicate an alert.
- If the temperature is below 38°C, the green LED stays on, and the buzzer is silent.
- The LCD continuously updates with the current temperature.

## 📝 License

This project is open-source and free to use under the MIT License.

---

Made with ❤️ by Javier Siliacay | USTP 🇵🇭
