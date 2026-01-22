## 🐍 Snake Game Player (Embedded System Project)

An embedded-system implementation of the classic **Snake Game**, developed using **C programming** on the **LPC2124 (ARM7) microcontroller**, featuring real-time input via keypad and graphical output on an LCD display.

---

## 📌 Project Overview

This project was developed as part of the **Embedded System Course Design** at **Hubei University of Technology**.
The game demonstrates core embedded concepts such as **hardware–software integration**, **data structures**, and **real-time control**.

The snake movement and body management are implemented using a **doubly linked list**, ensuring efficient updates during gameplay.

---

## ⚙️ Hardware Requirements

* **Microcontroller:** LPC2124 (ARM7TDMI-S)
* **Display:** LM3228 (128×64 Graphic LCD)
* **Input Device:** 4×4 Matrix Keypad
* **Power Supply:** 5V
* **Other Components:** 10K Resistors

---

## 💻 Software & Tools

* **Programming Language:** C
* **IDE / Toolchain:** Keil µVision
* **Simulation:** Proteus
* **Architecture:** ARM7TDMI

---

## 🎮 Game Features

* Classic snake movement (Up, Down, Left, Right)
* Boundary wrapping logic
* Random food generation
* Snake body growth on food consumption
* Collision detection (self & boundary)
* Efficient snake management using **Doubly Linked List**
* Real-time keypad control
* LCD-based graphical rendering

---

## 🧠 Key Concepts Used

* Embedded C programming
* GPIO & peripheral control
* Doubly linked list data structure
* Real-time input handling
* LCD graphics rendering
* Memory management

---

## 📂 Project Structure

```
Snake-Game-Player/
│
├── Snake Game/
│   ├── main.c
│   ├── lcddrv.c
│   ├── config.h
│   ├── target.c
│   ├── Startup.s
│   └── ...
│
├── README.md
```

---

## ▶️ How to Run

1. Open the project in **Keil µVision**
2. Compile the source files
3. Simulate the circuit using **Proteus**
4. Upload the program to **LPC2124**
5. Control the snake using the **4×4 keypad**

---

## 🏫 Academic Information

* **Course:** Embedded System Course Design
* **Department:** Computer Science & Technology
* **University:** Hubei University of Technology
* **Instructor:** Dr. Liu Chun
* **Student:** Muntasir Md Fahim (王一然)

---

## 📜 License

This project is created for **educational and academic purposes**.
Feel free to study, modify, and improve it with proper credit.

---
