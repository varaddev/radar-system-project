# Arduino Radar System 📡

A simple Arduino-based radar system made using an **Arduino UNO, HC-SR04 ultrasonic sensor, and servo motor**.

The ultrasonic sensor is mounted on the servo motor and continuously scans an area of **180°**. The Arduino measures the distance of objects and sends the angle and distance data through the Serial Monitor. This data can also be used with a Processing-based radar interface to display the detected objects visually.

## 🔧 Components Used

* Arduino UNO
* HC-SR04 Ultrasonic Sensor
* SG90 Servo Motor
* Mini Breadboard
* Jumper Wires
* USB Cable
* Computer/Laptop

## 🔌 Circuit Connections

### Servo Motor

| Servo Wire | Arduino       |
| ---------- | ------------- |
| Brown      | GND           |
| Red        | 5V            |
| Yellow     | Digital Pin 6 |

### HC-SR04

| HC-SR04 Pin | Arduino        |
| ----------- | -------------- |
| VCC         | 5V             |
| GND         | GND            |
| TRIG        | Digital Pin 9  |
| ECHO        | Digital Pin 10 |

The **5V and GND from the Arduino are connected to the mini breadboard**, which is then used to provide power to the servo and ultrasonic sensor.

## ⚙️ How It Works

The servo motor moves the HC-SR04 sensor from **0° to 180°** and then back from **180° to 0°**.

At every position:

1. The HC-SR04 sends an ultrasonic pulse.
2. The sensor receives the reflected pulse.
3. Arduino calculates the distance of the object.
4. The servo angle and distance are sent through Serial communication.

The data is sent in this format:

```text
angle,distance
```

For example:

```text
90,35
```

This means that an object was detected at approximately **35 cm at an angle of 90°**.

## 🚀 Servo Speed

The sweep speed was increased by:

* Moving the servo in **2° steps**
* Reducing the delay between movements

This makes the radar scan faster while still giving useful distance readings.


## 📊 Output

The Arduino sends the scanning information through the Serial port at **9600 baud**.

The output can be used to create a radar-style visualization showing:

* Scanning angle
* Detected distance
* Object position
* 180° scanning area

## 🎯 Purpose of the Project

The main purpose of this project was to understand how **ultrasonic sensing, servo control, Arduino programming, and serial communication** work together in a practical system.

The project is also a small-scale demonstration of the basic idea behind radar-style object detection and scanning.

## 🔮 Future Improvements

Some improvements I would like to add in the future:

* A proper graphical radar interface
* Real-time object tracking
* Object detection indicators
* Adjustable scanning range
* Better distance filtering
* Faster and smoother scanning
* Possible applications in obstacle detection and assistive systems

## 📁 Project Structure

```text
Arduino-Radar/
│
├── Arduino-Radar.ino
├── README.md
└── images/
    └── circuit-diagram.png
```

## 👨‍💻 Project

Built as an Arduino electronics project to explore **embedded systems, sensors, servo control, and real-time object detection**.

---

⭐ If you found this project useful, feel free to star the repository.
