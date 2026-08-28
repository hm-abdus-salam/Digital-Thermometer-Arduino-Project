# 🌡️ Digital Thermometer Using Arduino

It is a university-level project
Created By
Md. Abdus Salam (Team Leader), Nawshin Rahman, Md. Hasan Sarder
Department: Computer Science & Engineering
Khulna Khan Bahadur Ahsanullah University

Submitted By
Jerin Tasnim
Designation: Lecturer, Department of CSE
Email: jerin@kkbau.ac.bd
Khulna Khan Bahadur Ahsanullah University

Project YouTube link (Here you see how the project works): https://youtu.be/QbOLVbSkEmA?si=_IL3KgRYwSAj6xhG


A simple and practical **Digital Thermometer** project developed using an **Arduino UNO**, temperature sensor, and LCD display. The project measures the surrounding/environmental temperature and displays the temperature value on an LCD in real time.

This project was first designed and tested virtually using **Proteus Design Suite**. After successfully verifying the circuit and program in simulation, the same project was implemented physically using an **Arduino UNO board**, temperature sensor, potentiometer, LCD display, and connecting wires.

---

## 📌 Project Overview

The main purpose of this project is to build a low-cost and easy-to-use digital thermometer capable of measuring environmental temperature and displaying the measured value on an LCD.

The complete development process was divided into two major stages:

1. **Simulation and testing using Proteus**
2. **Physical implementation using Arduino UNO**

First, the circuit was created in Proteus and the Arduino program was tested virtually. After confirming that the circuit and code were working correctly, the project was built physically by connecting the required components to an Arduino UNO board.

Finally, the program was uploaded to the Arduino UNO using the Arduino IDE. Once all connections were completed correctly, the LCD started displaying the surrounding temperature according to the sensor reading.

---

## 🎯 Project Objectives

The main objectives of this project are:

* To learn the basic working principle of a digital thermometer.
* To understand how Arduino UNO works with sensors.
* To measure environmental temperature using a temperature sensor.
* To display temperature readings on an LCD.
* To understand LCD interfacing with Arduino.
* To practice circuit simulation using Proteus.
* To learn how to upload Arduino programs to a physical Arduino UNO board.
* To gain practical experience in embedded systems and hardware interfacing.

---

## 🛠️ Technologies and Tools Used

| Technology / Tool         | Purpose                                       |
| ------------------------- | --------------------------------------------- |
| Arduino UNO               | Main microcontroller board                    |
| Arduino IDE               | Writing, compiling, and uploading the program |
| Proteus                   | Circuit design and simulation                 |
| Temperature Sensor        | Measuring environmental temperature           |
| LCD Display               | Displaying temperature readings               |
| LiquidCrystal Library     | Interfacing with a standard LCD               |
| LiquidCrystal_I2C Library | Interfacing with an I2C LCD                   |
| Potentiometer             | LCD contrast adjustment                       |
| Jumper Wires              | Connecting components                         |
| Breadboard                | Circuit prototyping                           |

---

## 🔩 Required Components

The following hardware components were used to build the physical project:

* Arduino UNO
* Temperature Sensor
* 16×2 LCD Display
* Potentiometer
* Breadboard
* Jumper Wires
* USB Cable
* Computer/Laptop

> **Note:** The exact temperature sensor and LCD interface may vary depending on the circuit design. The Arduino code and wiring should be configured according to the specific sensor and LCD module being used.

---

# 🔄 How the Project Works

The basic working process of the digital thermometer is:

```text
Temperature Sensor
        ↓
  Detects Temperature
        ↓
      Arduino UNO
        ↓
  Processes Sensor Data
        ↓
      LCD Display
        ↓
 Displays Temperature
```

The temperature sensor detects the surrounding temperature and sends an electrical signal to the Arduino UNO.

The Arduino reads this signal, processes the sensor data, and calculates the corresponding temperature value.

The calculated temperature is then sent to the LCD display, where it is shown in a readable format.

As the surrounding temperature changes, the sensor detects the change and the Arduino updates the LCD accordingly.

---

# 🧪 Step 1: Designing the Circuit in Proteus

Before building the physical circuit, I first designed and tested the project in **Proteus**.

Proteus was used to create a virtual representation of the Arduino-based thermometer circuit. All the required components were placed in the Proteus workspace and connected according to the circuit design.

The main components included:

* Arduino UNO
* Temperature Sensor
* LCD Display
* Potentiometer
* Power and Ground connections
* Required connecting wires

After completing the circuit connections, the Arduino program was loaded into the simulated Arduino UNO.

The simulation was then started to verify whether the sensor, Arduino, and LCD were communicating correctly.

### Why Proteus was used

Using Proteus before hardware implementation was useful because it allowed me to:

* Check the circuit connections.
* Test the Arduino program.
* Identify wiring mistakes.
* Verify LCD operation.
* Observe temperature readings virtually.
* Reduce the possibility of hardware connection errors.

After confirming that the circuit and program were working properly in Proteus, I proceeded to the physical implementation.

---

# 💻 Step 2: Writing the Arduino Program

After successfully testing the project in Proteus, I prepared the Arduino program using the **Arduino IDE**.

The program performs several important tasks:

1. Initializes the LCD.
2. Initializes the temperature sensor.
3. Reads the sensor value.
4. Converts the sensor reading into temperature.
5. Sends the temperature value to the LCD.
6. Continuously updates the displayed temperature.

Depending on the LCD module being used, either the standard **LiquidCrystal** library or the **LiquidCrystal_I2C** library can be used.

### Standard LCD

For a traditional parallel 16×2 LCD, the `LiquidCrystal` library can be used.

### I2C LCD

For an LCD equipped with an I2C module, the `LiquidCrystal_I2C` library can be used.

The I2C version requires fewer Arduino pins because communication takes place through the I2C interface.

---

# 🔌 Step 3: Preparing the Physical Circuit

After completing the simulation and programming stage, I started building the physical version of the thermometer.

First, I placed the Arduino UNO and other components on the working area.

The required wires were then connected between the Arduino UNO, temperature sensor, potentiometer, and LCD.

The potentiometer was connected for controlling the LCD contrast.

The temperature sensor was connected to the appropriate Arduino power, ground, and signal pins according to the sensor's configuration.

The LCD was then connected to the Arduino UNO.

All power and ground connections were carefully checked before powering the circuit.

---

# 🔗 Step 4: Connecting the Temperature Sensor

The temperature sensor is the main sensing component of this project.

It detects the temperature of the surrounding environment and provides the corresponding signal to the Arduino UNO.

The Arduino continuously reads the sensor output and processes the received data.

The sensor connection generally includes:

* VCC → Arduino power supply
* GND → Arduino GND
* Signal/Output → Arduino input pin

The exact signal pin depends on the particular temperature sensor used in the project.

---

# 🖥️ Step 5: Connecting the LCD Display

The LCD is responsible for showing the measured temperature.

For a standard parallel LCD, multiple data and control pins are connected between the LCD and Arduino.

For an I2C LCD, the connection is simpler because the I2C module handles communication.

A typical I2C LCD connection is:

| LCD I2C Pin | Arduino UNO |
| ----------- | ----------- |
| VCC         | 5V          |
| GND         | GND         |
| SDA         | A4          |
| SCL         | A5          |

> **Note:** The I2C pins shown above are for the Arduino UNO. The exact connection may differ for other Arduino boards.

---

# 🎛️ Step 6: Connecting the Potentiometer

A potentiometer was used to adjust the contrast of the LCD display.

The potentiometer helps make the characters on the LCD clearly visible.

The contrast adjustment is especially important when using a traditional 16×2 LCD because an incorrect contrast setting can make the display appear blank even when the circuit is working correctly.

After connecting the potentiometer, I adjusted it until the LCD characters became clearly visible.

---

# 🔧 Step 7: Uploading the Program to Arduino UNO

Once all hardware connections were completed, the Arduino UNO was connected to the computer using a USB cable.

The Arduino IDE was then opened.

The Arduino UNO board was selected from the board settings, and the correct communication port was selected.

The program was then compiled to check for errors.

After successful compilation, the program was uploaded to the Arduino UNO.

The basic process was:

```text
Connect Arduino UNO to Computer
              ↓
        Open Arduino IDE
              ↓
        Select Arduino UNO
              ↓
        Select COM Port
              ↓
        Verify / Compile Code
              ↓
          Upload Code
              ↓
       Arduino Starts Running
```

After the upload was completed successfully, the Arduino UNO began executing the thermometer program.

---

# 🧪 Step 8: Testing the Complete Hardware

After uploading the program, I carefully checked the complete circuit.

I verified:

* Arduino UNO power connection
* Temperature sensor connection
* LCD connection
* Potentiometer connection
* Ground connections
* Jumper wire connections
* LCD visibility
* Sensor response

After confirming that everything was connected correctly, the LCD started displaying the environmental temperature.

The temperature value changed according to the surrounding environment.

For example:

```text
----------------
 Temperature
    28.5 °C
----------------
```

The actual displayed value depends on the surrounding temperature and the sensor being used.

---

# ⚙️ Working Principle

The working principle of the project is straightforward.

### 1. Temperature Detection

The temperature sensor detects the temperature of the surrounding environment.

### 2. Sensor Reading

The sensor generates an electrical signal corresponding to the detected temperature.

### 3. Arduino Processing

The Arduino UNO reads the sensor signal through its input pin.

The Arduino program processes the sensor data and converts it into a temperature value.

### 4. LCD Output

The calculated temperature is sent to the LCD display.

### 5. Continuous Monitoring

The Arduino repeatedly reads the sensor and updates the LCD.

Therefore, the display continuously provides the current environmental temperature.

---

# 🧩 Project Architecture

The complete project can be represented as:

```text
                 ┌─────────────────────┐
                 │   Temperature       │
                 │      Sensor         │
                 └──────────┬──────────┘
                            │
                            │ Sensor Data
                            ↓
                 ┌─────────────────────┐
                 │     Arduino UNO     │
                 │                     │
                 │  Read Sensor Data   │
                 │        ↓            │
                 │ Process Temperature │
                 └──────────┬──────────┘
                            │
                            │ Temperature Data
                            ↓
                 ┌─────────────────────┐
                 │    LCD Display      │
                 │                     │
                 │   Temperature       │
                 │      28.5 °C        │
                 └─────────────────────┘
```

The potentiometer is used to control the LCD contrast, while the Arduino UNO acts as the central controller of the entire system.

---

# 🧑‍💻 Software Development Process

The complete software development process followed these steps:

### Phase 1: Circuit Design

The circuit was designed in Proteus using the required components.

### Phase 2: Simulation

The Arduino program was loaded into the Proteus simulation and the complete circuit was tested.

### Phase 3: Error Checking

The circuit and program were checked for incorrect connections and programming errors.

### Phase 4: Arduino IDE Development

The final Arduino program was prepared using the required LCD library such as `LiquidCrystal` or `LiquidCrystal_I2C`.

### Phase 5: Hardware Implementation

The same circuit was physically assembled using Arduino UNO, sensor, LCD, potentiometer, breadboard, and jumper wires.

### Phase 6: Program Upload

The verified program was uploaded to the physical Arduino UNO using the Arduino IDE.

### Phase 7: Final Testing

The complete hardware was powered on and tested under different environmental temperature conditions.

---

# 📁 Project Structure

A simple GitHub repository structure for this project can be:

```text
Digital-Thermometer-Arduino/
│
├── README.md
│
├── Arduino-Code/
│   └── Digital_Thermometer.ino
│
├── Proteus/
│   └── Digital_Thermometer.pdsprj
│
├── Circuit-Diagram/
│   └── circuit.png
│
├── Images/
│   ├── proteus-simulation.png
│   ├── hardware-setup.jpg
│   └── lcd-output.jpg
│
└── LICENSE
```

---

# 📸 Project Demonstration

You can add screenshots and photographs of the project to this section.

### Proteus Simulation

Add a screenshot of the completed Proteus circuit here.

```text
[ Add Proteus Simulation Screenshot Here ]
```

### Physical Hardware

Add a photograph of the physical Arduino thermometer here.

```text
[ Add Hardware Setup Image Here ]
```

### LCD Output

Add a photograph showing the temperature on the LCD.

```text
[ Add LCD Output Image Here ]
```

These images will make the GitHub repository easier to understand and more professional.

---

# ✅ Features

The Digital Thermometer includes the following features:

* Real-time environmental temperature measurement
* LCD-based temperature display
* Arduino UNO-based control system
* Temperature sensor integration
* Proteus simulation before hardware implementation
* Easy-to-understand circuit design
* Simple and low-cost hardware
* Continuous temperature monitoring
* Practical embedded-system implementation

---

# 🚀 Future Improvements

This project can be expanded with additional features in the future, such as:

* Adding a buzzer for high-temperature alerts.
* Adding temperature threshold settings.
* Displaying temperature in both Celsius and Fahrenheit.
* Adding humidity measurement using a DHT11/DHT22 sensor.
* Sending temperature data to a mobile application.
* Adding Bluetooth or Wi-Fi connectivity.
* Storing temperature readings for later analysis.
* Creating a web-based temperature monitoring system.
* Using an OLED display instead of a traditional LCD.
* Adding IoT functionality for remote temperature monitoring.

---

# 🎓 Learning Outcomes

Through this project, I gained practical experience in:

* Arduino programming
* Arduino UNO hardware interfacing
* Temperature sensor interfacing
* LCD interfacing
* I2C communication
* Circuit design
* Proteus simulation
* Embedded systems
* Hardware troubleshooting
* Arduino IDE
* Uploading firmware to a microcontroller
* Testing and debugging electronic circuits

Most importantly, this project helped me understand how software and hardware work together in an embedded system.

---

# 🏁 Conclusion

The **Digital Thermometer Using Arduino** project was successfully designed, simulated, implemented, and tested.

First, the complete circuit was designed and tested in **Proteus** to verify the circuit connections and Arduino program. After confirming that the simulation worked correctly, the project was physically assembled using an **Arduino UNO, temperature sensor, LCD display, potentiometer, breadboard, and jumper wires**.

The Arduino program was then loaded onto the Arduino UNO using the **Arduino IDE**. After checking all the hardware connections and powering on the system, the temperature sensor successfully detected the surrounding environmental temperature and the LCD displayed the corresponding temperature value.

This project demonstrates a simple but practical application of Arduino in real-world temperature monitoring. It also provided valuable hands-on experience in circuit simulation, sensor interfacing, LCD communication, microcontroller programming, and hardware implementation.

---

## 👨‍💻 Author 
Md. Abdus Salam (Team Leader)
Computer Engineer
Khulna Khan Bahadur Ahsanullah University


**Digital Thermometer Using Arduino**

Built with ❤️ using **Arduino UNO**

---

## ⭐ If You Like This Project
If you find this project useful or interesting, feel free to star ⭐ the repository and explore the source code, Proteus simulation, and project documentation.
