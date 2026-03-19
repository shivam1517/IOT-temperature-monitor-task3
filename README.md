🌡️ IoT Temperature Monitoring System (Tinkercad Simulation)

📌 Description

This project demonstrates a simple IoT-based temperature monitoring system using Tinkercad simulation.
It reads temperature values from a sensor and controls an LED based on the temperature level.

---

🚀 Features

- 🌡️ Temperature sensing using TMP36 sensor
- 🔴 LED indication for high temperature
- 💻 Fully simulated in Tinkercad (no hardware required)
- ⚡ Real-time output using Serial Monitor

---

🛠️ Components Used

- Arduino UNO
- TMP36 Temperature Sensor
- LED
- Resistor
- Breadboard

---

🔌 Circuit Connections

TMP36 Sensor:

- VCC → 5V
- GND → GND
- Output → A0

LED:

- Positive → Pin 13
- Negative → GND (via resistor)

---

💻 Code

int sensorPin = A0;
int ledPin = 13;

void setup() {
  Serial.begin(9600);
  pinMode(ledPin, OUTPUT);
}

void loop() {
  int value = analogRead(sensorPin);
  float voltage = value * (5.0 / 1023.0);
  float temperature = (voltage - 0.5) * 100;

  Serial.print("Temperature: ");
  Serial.print(temperature);
  Serial.println(" C");

  if (temperature > 30) {
    digitalWrite(ledPin, HIGH);
  } else {
    digitalWrite(ledPin, LOW);
  }

  delay(1000);
}

---

▶️ How to Run (Tinkercad)

1. Open Tinkercad Circuits
2. Create a new circuit
3. Add components (Arduino, TMP36, LED)
4. Connect as per diagram
5. Paste the code
6. Click Start Simulation
7. Open Serial Monitor to view output

---

📊 Output

- Displays temperature values
- LED turns ON when temperature > 30°C
- LED turns OFF when temperature ≤ 30°C

---

📸 Screenshots

Add:

- Circuit design screenshot
- Serial Monitor output

---

⚠️ Note

This project is implemented using Tinkercad simulation due to unavailability of physical hardware.

---

🎯 Future Scope

- IoT cloud integration
- Mobile app monitoring
- Real sensor implementation

---

👨‍💻 Author

Shivam Paswan
