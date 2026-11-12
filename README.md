# Bluetooth-Based Wireless Smart Toll Barrier Using LPC2129

## Project Overview

This project implements a wireless toll barrier control system using the LPC2129 ARM7 microcontroller. It uses Bluetooth communication to receive commands and control a servo motor to open or close the toll barrier.

An IR sensor detects the presence of an object or vehicle. The detection signal triggers an external interrupt (EINT0), while an LCD displays the system status.

## Hardware Requirements

- LPC2129 ARM7 Microcontroller
- Bluetooth Module
- IR Sensor
- 16x2 LCD Display
- Servo Motor
- LED
- Power Supply

## Technologies Used

- Embedded C
- ARM7 LPC2129
- UART Communication
- PWM
- External Interrupt (EINT0)
- LCD Interfacing
- IR Sensor Interfacing

## Project Structure

| File | Description |
|---|---|
| `main.c` | Main program and barrier control logic |
| `bluetooth_header.h` | Bluetooth communication using UART0 |
| `lcd_header.h` | LCD interfacing functions |
| `servo_motor.h` | Servo motor control using PWM |

## Working Principle

1. The LPC2129 initializes UART0, LCD, PWM5, and EINT0.
2. The IR sensor detects an object or vehicle and triggers an external interrupt.
3. A detection message is displayed on the LCD and transmitted through Bluetooth.
4. The user sends a command through a Bluetooth-connected device.
5. The `open` command moves the servo motor to 90 degrees, opening the barrier.
6. The `close` command moves the servo motor to 0 degrees, closing the barrier.
7. The LCD displays the corresponding barrier status.

## Bluetooth Commands

| Command | Action |
|---|---|
| `open` | Opens the toll barrier |
| `close` | Closes the toll barrier |

## Applications

- Automated toll barriers
- Wireless gate control systems
- Parking management systems
- Vehicle access control

## Learning Outcomes

- ARM7 microcontroller programming
- Bluetooth and UART communication
- IR sensor interfacing
- PWM-based servo motor control
- External interrupt handling
- LCD interfacing using Embedded C
