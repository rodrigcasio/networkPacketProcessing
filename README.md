# Network Packet Processing Simulation: C++ Console Project

A lightweight C++ console-based simulation for processing network packets, designed to demonstrate the use of **enums**, **enum classes**, and **status management** in a networking context. The project models real-world packet types, protocols, and validation logic, providing a clear example of how C++ can be used for protocol simulation and error handling.

## Features

- **Packet Modeling**: Represents network packets with types (DATA, CONTROL, GROUP, RESOLUTION, ERROR, UNKNOWN) and protocols (TCP, UDP, ICMP, IGMP, ARP, HTTP, FTP) using enums and enum classes.
- **Status Management**: Assigns and tracks packet status (PENDING, VALID, INVALID, TIMEOUT) to simulate real-world packet validation and error handling.
- **Validation Logic**: Validates packets based on their type and protocol, demonstrating conditional logic and status assignment.
- **Formatted Output**: Displays detailed information for each packet, including type, protocol, and status, with clear console output for simulation steps.
- **Error Handling**: Identifies invalid packets for logging or further processing.

## C++ Principles Demonstrated

- **Enums and Enum Classes**: Uses traditional enums for packet types and enum classes for protocols, illustrating the differences and best practices.
- **Encapsulation**: The `Packet` class encapsulates all packet-related data and behavior, including validation and display logic.
- **Const-Correctness**: Read-only methods are marked as `const` to ensure data integrity.
- **Switch Statements**: Extensively uses `switch` for mapping enums to string names and for validation logic.
- **Constructor Initialization Lists**: Initializes member variables efficiently in the `Packet` constructor.
- **Status Management**: Demonstrates how to manage and update object state based on business logic.

## Purpose

Developed as part of my C++ learning journey, this project demonstrates how to model and process network packets using enums, encapsulation, and status management. It is intended as a practical example for those learning about protocol simulation, error handling, and object-oriented design in C++.

## How to Run

```sh
g++ src/mainNetworkPacket.cpp src/fns_Packet.cpp -I include -o network_packet_sim
./network_packet_sim
```

## Sample Output

```
	=== Packet ===
Packet Type Name: DATA
Protocol Name: UDP
Status Name: PENDING
	=== Packet ===
Packet Type Name: DATA
Protocol Name: UDP
Status Name: VALID
---
	=== Packet ===
Packet Type Name: CONTROL
Protocol Name: TCP
Status Name: PENDING
	=== Packet ===
Packet Type Name: CONTROL
Protocol Name: TCP
Status Name: VALID
---
	=== Packet ===
Packet Type Name: UNKNOWN
Protocol Name: TCP
Status Name: PENDING
	=== Packet ===
Packet Type Name: UNKNOWN
Protocol Name: TCP
Status Name: INVALID
---
	=== Packet ===
Packet Type Name: ERROR
Protocol Name: HTTP
Status Name: PENDING
	=== Packet ===
Packet Type Name: ERROR
Protocol Name: HTTP
Status Name: VALID
---
	=== Packet ===
Packet Type Name: GROUP
Protocol Name: IGMP
Status Name: PENDING
	=== Packet ===
Packet Type Name: GROUP
Protocol Name: IGMP
Status Name: VALID
---
	=== Packet ===
Packet Type Name: RESOLUTION
Protocol Name: ARP
Status Name: PENDING
	=== Packet ===
Packet Type Name: RESOLUTION
Protocol Name: ARP
Status Name: INVALID
```

## File Structure

- **include/h_Packet.hpp**: Defines the `Packet` class, encapsulating type, protocol, and status, with methods for validation and display.
- **include/h_PacketType.hpp**: Declares the `PacketType` enum for various network packet types.
- **include/h_Protocol.hpp**: Declares the `Protocol` enum class for supported network protocols.
- **src/fns_Packet.cpp**: Implements the `Packet` class methods, including validation logic and formatted output.
- **src/mainNetworkPacket.cpp**: Contains the main simulation logic, creating and processing various packets to demonstrate the system.

## Author

Rodrigo Casio ([View my Github profile](https://github.com/rodrigcasio))
