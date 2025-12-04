# Network Packet Transmission Monitoring System

**Course:** SECR 1013: Digital Logic Design  
**Institution:** Universiti Teknologi Malaysia (UTM)  
**Tools:** Deeds (Digital Electronics Education and Design Suite)

## Project Overview
This project simulates a real-world scenario where data packets are transmitted between computers in two different laboratories (Lab 1 and Lab 2) over a single cable. The system is designed to regulate, monitor, and secure data packet transmission using fundamental digital logic components.

The project demonstrates the practical application of multiplexers, counters, comparators, and logic gates to create a synchronized, full-duplex communication system with built-in error detection.

## Key Features
* **Packet Routing:** Uses 8-to-1 MUX and 1-to-8 DEMUX to select source and destination computers dynamically.
* **Synchronous Counting:** Implements a 3-bit synchronous counter using T flip-flops to track transmitted packets.
* **Traffic Control:** Features a **Comparator** and **Clock Enabler** to automatically stop transmission when a user-defined packet limit is reached.
* **Full Duplex Communication:** Allows simultaneous data transmission and reception between Lab 1 and Lab 2.
* **Security:** Includes a **Password Module** that requires a 4-digit PIN (default: 2025) to authorize data transfer.
* **Fault Detection System:** A dedicated logic circuit that detects and reports 6 specific error types:
    * Power Error (001)
    * Counter Error (010)
    * Comparator Error (011)
    * Password Error (100)
    * Data Error (101)
    * Multiple Errors (111)

## System Architecture
The system is composed of several distinct logic modules:

1.  **Computer Module:** Simulates the user end-point with Power, Data, and Clock inputs.
2.  **Mux/Demux Connection:** Handles the routing logic (Selecting 1 of 8 computers).
3.  **3-Bit Up Counter:** Tracks the number of packets sent (0 to 7).
4.  **Clock Enabler:** The "Gateway" that allows the system to run only when specific conditions (Power, Auth, Limit) are met.
5.  **Comparator:** Compares `Data Sent` vs. `Max Limit` to prevent overflow.
6.  **Fault Detection Panel:** Visual feedback for system status and debugging.

## 🚀 How to Run the Simulation
To run this project, you need the **Deeds** software.

1.  Open the circuit file in Deeds.
2.  **Configure Routing:** Choose to transfer data (Lab 1 → Lab 2 OR Lab 2 → Lab 1) and select computer numbers.
3.  **Power Up:** Toggle the **POWER** switch on the chosen computers to `HIGH`.
4.  **Initialize Clock:** Click the **CLK** on the chosen input computer.
5.  **Setup Counter:** Activate the Counter Activator by setting `Preset` and `Clear` to `1`.
6.  **Set Limits:** Input the maximum Data Transfer Limit (Max: 7).
7.  **Authenticate:** Enter the security PIN (Default: `2025`).
8.  **Verify Status:** Check the Fault Detection Panel to ensure "NO ERROR" is displayed.
9.  **Transmit:** Click the Clock in the "SEND DATA" section to begin transmission.

---
*This project was developed for the Semester 01 2024/2025 session.*
