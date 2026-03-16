# Wireless Sensor Data Transmission Using UART (PIC16F877A)

## Overview

This project demonstrates how to transmit sensor data from a **PIC16F877A microcontroller** to a **PC using UART serial communication**.

The microcontroller reads analog sensor data using its **ADC peripheral** and sends the formatted data through **UART at 9600 baud**. The transmitted data can be viewed using a **serial terminal such as Tera Term or PuTTY**.

Example output:

TEMP: 32 C
TEMP: 33 C
TEMP: 31 C

---

## Objectives

* Read analog sensor data using the **ADC module**
* Convert analog value to digital
* Transmit the data using **UART serial communication**
* Display the sensor value on a **PC serial terminal**

---

## Hardware Requirements

* PIC16F877A Microcontroller
* LM35 Temperature Sensor 
* 20 MHz Crystal Oscillator
* USB-to-TTL Serial Converter

* Connecting wires

---

## Software Requirements

* MPLAB X IDE
* XC8 Compiler
* Tera Term / PuTTY Serial Terminal

---

## Functional Description

1. The sensor output is connected to **AN0 (RA0)** of the PIC16F877A.
2. The internal **10-bit ADC** converts the analog signal into a digital value.
3. The microcontroller formats the sensor value using `sprintf()`.
4. The formatted data is transmitted through **UART TX (RC6)**.
5. A PC serial terminal receives and displays the transmitted data.

---

## UART Configuration

Baud Rate : 9600
Data Bits : 8
Parity    : None
Stop Bits : 1

---

## Hardware Connections

### Sensor Connection

PIC16F877A | Sensor
RA0 (AN0)  | Sensor Output
VCC        | 5V
GND        | GND

### UART Connection

PIC16F877A | USB-TTL Converter
RC6 (TX)   | RX
RC7 (RX)   | TX
GND        | GND

---

## Example Serial Output

TEMP: 512 C
TEMP: 498 C
TEMP: 501 C

---

## Applications

* Sensor data monitoring
* Embedded communication learning
* Industrial sensor logging
* IoT data transmission prototypes

---

## Learning Outcomes

* ADC peripheral usage
* UART serial communication
* Embedded C programming
* Sensor interfacing
* Serial debugging

---


**Sathiyaseelan**
Embedded Systems Developer
