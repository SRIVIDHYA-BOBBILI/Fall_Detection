# 🧠 Fall Detection System (STM32 + FreeRTOS)

## 📌 Overview

This project implements a **fall detection system on an STM32F429ZI microcontroller** using **FreeRTOS**. It is designed as an embedded firmware application that can process motion-related inputs and detect fall events based on predefined logic.

Unlike a simple software simulation, this project is structured for **real-time embedded execution**, making it suitable for IoT and wearable safety applications.

---

## ⚙️ Key Features

* 🧵 **FreeRTOS-based multitasking architecture**
* ⚡ Real-time task scheduling for continuous monitoring
* 🧩 Modular firmware design (HAL + CMSIS)
* 🔄 Interrupt-driven system behavior
* 📊 Scalable for integration with sensors (accelerometer/gyroscope)
* 🛠️ Configurable detection logic (threshold/event-based)

---

## 🧱 System Architecture

* **Microcontroller:** STM32F429ZI
* **Framework:** STM32 HAL (Hardware Abstraction Layer)
* **RTOS:** FreeRTOS
* **Core Modules:**

  * Task scheduling (`freertos.c`)
  * Main control loop (`main.c`)
  * Interrupt handling (`stm32f4xx_it.c`)
  * System initialization (`system_stm32f4xx.c`)

---

## 📂 Project Structure

```
Fall_Detection_Simulator/
│
├── Core/
│   ├── Inc/        # Header files
│   ├── Src/        # Application source code
│   └── Startup/    # Startup assembly code
│
├── Drivers/
│   ├── CMSIS/      # ARM Cortex support
│   └── STM32 HAL   # Hardware abstraction layer
│
├── .ioc            # STM32CubeMX configuration
├── linker.ld       # Memory linker script
```

---

## 🚀 How It Works

1. System initializes hardware and RTOS scheduler
2. Multiple FreeRTOS tasks are created
3. Tasks simulate or process motion-related inputs
4. Detection logic evaluates abnormal patterns
5. Fall event is triggered based on defined conditions

---

## 🛠️ How to Build & Run

### Requirements:

* STM32CubeIDE
* STM32F4 board (e.g., STM32F429ZI)

### Steps:

1. Open `.ioc` file in STM32CubeIDE
2. Generate project code (if required)
3. Build the project
4. Flash to STM32 board
5. Monitor output via debugger/serial

---

## ⚠️ Limitations 

* No direct sensor integration included (currently firmware-ready structure)
* Detection logic depends on simulated or placeholder inputs
* No ML or advanced signal processing implemented


