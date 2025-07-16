# Network Packet Processing Simulation (C++)

This is a small C++ console project I made while learning about enums and basic C++ programming. The program simulates how different types of network packets (like DATA, CONTROL, ERROR, etc.) are processed and validated using simple logic.

## What does it do?

- **Creates several example network packets** with different types and protocols (like TCP, UDP, HTTP, etc.).
- **Shows the details of each packet** before and after validation.
- **Validates each packet** to check if it is valid or invalid, based on its type and protocol.
- **Prints the results** to the console, so you can see how the status of each packet changes.

## Example Output

When you run the program, you’ll see output like this:

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

## Why did I make this?

I wanted to practice using enums, classes, and simple validation logic in C++. This project helped me understand how to use enums for different categories (like packet types and protocols) and how to write basic class methods.

## How to Run

1. Make sure you have a C++ compiler (like g++) installed.
2. Compile the code:
   ```
   g++ src/mainNetworkPacket.cpp src/fns_Packet.cpp -I include -o network_packet_sim
   ```
3. Run the program:
   ```
   ./network_packet_sim
   ```

## Author

Rodrigo Casio  
[My GitHub Profile](https://github.com/rodrigcasio)
