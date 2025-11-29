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
This project uses **CMake** build system generator for easy, cross-platform compilation. Follow these steps from the root directory of the project `networkPacketProcessing/`

1. **Ensure CMake is installed:**
- Make sure you have CMake (version 3.1- or higher please) and a C++ compiler (g++ or clang++) installed on your system.

2. **Generate the build system (configure):**
- Create a separated directory for the build files  and run CMake inside it. Keeping source files clean

```bash
mkdir build
cd build
cmake ..
```

3. **Build:**
- Use generated build system (`make` on Unix-like systems) to compile the executable.

```bash 
make
```

4. **Run the program:**
- The executable (PacketProcessing) will be placed inside the `build` directory.

```bash 
./PacketProcessing
```

**IMPORTANT: Note for windows users:**

- Windows developers have two ways to build the project using CMake.
  - **Command line (MSYS2/Cygwin):** If you use an environment like **MSYS2** or **WLS** (Windows Subsystem for Linux), you can follow the **Standard Build** steps above exactly.
  - **Visual Studio:** CMake can generate a Visual Studio solution. Run CMake from your `developer command prompt`, specify the generator:

```bash 
cmake .. -G "Visual Studio 17 2022"
```

Then, open the generated `.sln` file and build within Visual Studio IDE.

## Author

Rodrigo Casio  
[My GitHub Profile](https://github.com/rodrigcasio)
