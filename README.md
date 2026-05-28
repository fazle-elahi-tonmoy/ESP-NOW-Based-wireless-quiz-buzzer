# ESP-NOW Based Wireless Quiz Buzzer System

A low-latency wireless quiz buzzer system built using ESP32 and ESP-NOW communication protocol.

This system is designed for:

* 🧠 Quiz competitions
* 🎓 Classroom activities
* 🏫 Science fairs
* ⚡ Fast-response buzzer rounds
* 🕹 Multiplayer reaction games

The system consists of:

* 🎛 One **Master Unit**
* 🔘 Multiple **Wireless Buzzer Nodes (Slave Units)**

The first participant to press the buzzer is instantly detected and locked by the master unit.

---

# 🚀 Features

## 📡 ESP-NOW Wireless Communication

Uses ESP-NOW protocol for:

* Ultra-low latency communication
* No WiFi router required
* Reliable local wireless networking

---

## ⚡ Instant First Press Detection

The system instantly:

* Detects first buzzer press
* Locks all remaining buzzers
* Displays winning participant

---

## 🔒 Anti-Cheat Lock System

Once a participant presses:

* Other buttons become disabled
* Prevents multiple winners

---

## 🎯 Wireless Multi-Player Support

Supports multiple wireless buzzer nodes.

Each participant has:

* Dedicated ESP32 node
* Individual buzzer button
* Unique device ID

---

## 🔄 Broadcast Communication

Master device broadcasts:

* Reset commands
* Lock state
* Game control signals

---

## 🖥 Expandable Display Support

Can be extended with:

* OLED displays
* TFT displays
* LED indicators
* Sound feedback

---

# 🛠 Hardware Used

| Component           | Purpose            |
| ------------------- | ------------------ |
| ESP32 Dev Board     | Main controller    |
| Push Buttons        | Quiz input         |
| LEDs / Buzzers      | Feedback           |
| Battery / USB Power | Portable operation |

---

# 📂 Project Structure

| File                   | Description              |
| ---------------------- | ------------------------ |
| `Broadcast_master.ino` | Master controller        |
| `Broadcast_slave.ino`  | Wireless buzzer node     |
| `callback.ino`         | ESP-NOW receive callback |
| `callback(1).ino`      | Master callback logic    |
| `button(1).ino`        | Button handling          |

---

# 🧠 System Architecture

```text id="d7y9eh"
PLAYER NODE → ESP-NOW → MASTER UNIT
```

The first node to send a signal wins the round.

---

# ⚙ Working Principle

## Step 1 — Power On

All ESP32 devices initialize ESP-NOW communication.

---

## Step 2 — Wait for Input

Slave nodes continuously monitor their buzzer buttons.

---

## Step 3 — Button Press

When a participant presses a button:

* Slave sends wireless packet
* Master receives signal instantly

---

## Step 4 — Winner Lock

Master:

* Stores winner ID
* Locks remaining participants
* Broadcasts lock state

---

## Step 5 — Reset Round

Quiz master resets the system for the next round.

---

# 📡 Why ESP-NOW?

ESP-NOW provides:

* Very low latency
* Peer-to-peer communication
* No router dependency
* Better response time than WiFi HTTP systems

Perfect for competitive quiz systems.

---

# 🎯 Applications

## 🧠 Quiz Competitions

* School quiz contests
* University competitions
* Science olympiads

---

## 🎓 Educational Activities

* Classroom interaction
* Fast-answer sessions
* Student engagement

---

## 🕹 Reaction Games

* Multiplayer gaming systems
* Reflex testing systems

---

# 🔌 Suggested Connections

## Slave Unit

| Component   | ESP32 Pin   |
| ----------- | ----------- |
| Push Button | GPIO input  |
| LED         | GPIO output |
| Buzzer      | GPIO output |

---

## Master Unit

| Component    | Purpose          |
| ------------ | ---------------- |
| ESP32        | Central receiver |
| Display      | Winner display   |
| Reset Button | New round        |

---

# 📶 Communication Flow

```text id="f7x3mq"
Slave Button Press
        ↓
ESP-NOW Packet Transmission
        ↓
Master Receives Packet
        ↓
Winner Determined
        ↓
Lock Other Participants
```

---

# ⚡ Advantages of This System

✅ No Internet Required
✅ No WiFi Router Needed
✅ Fast Wireless Response
✅ Portable Design
✅ Low Power Consumption
✅ Expandable for More Players
✅ Real-Time Locking System

---

# 🔮 Future Improvements

Possible upgrades:

* OLED scoreboards
* TFT ranking display
* Rechargeable battery system
* Wireless charging dock
* Sound effects
* Team mode
* Mobile app monitoring
* Web dashboard
* Quiz timer integration

---

# 🏫 Educational Value

This project is excellent for learning:

* ESP32 programming
* Wireless communication
* ESP-NOW networking
* Embedded systems
* Event-driven programming
* Real-time systems

---

# ⚠ Disclaimer

This project is intended for:

* Educational purposes
* Research
* Prototype quiz systems
* STEM learning

---

# 👨‍💻 Author

Developed by **Fazle Elahi Tonmoy**

Areas of interest:

* Robotics
* Embedded Systems
* IoT Communication
* Wireless Automation
* Smart Devices

---

# 📄 License

MIT License

```text id="79z3pl"
MIT License © 2026 Fazle Elahi Tonmoy
```


