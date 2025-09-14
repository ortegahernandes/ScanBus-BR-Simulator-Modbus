# ScanBus-BR Modbus Simulator Master/Client. 
 **For Windows and Linux**

_The "Swiss Army Knife" of the Modbus network_.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scanbus-BR-linux.png)

## What is ScanBus-BR?

ScanBus-BR is much more than a Modbus Master/Client simulator software. 
It is a set of tools that will help you solve problems related to the Modbus network. 

Completely free (Freeware).

The ScanBus is PORTABLE, meaning it DOES NOT REQUIRE INSTALLATION and can be used even on pen drives.

ScanBus-BR is **NOT** limited to Ubuntu and derivatives; it works on virtually all popular Linux distributions, just extract and run. On rare occasions, it is enough to install the GTK2 library.

Free from any advertising or any Adware.

Designed to help developers find errors in slave devices and for anyone who wants to simulate, test and study the Modbus protocol.

You will hardly find another free or even paid software that will provide you with as many features as ScanBus-BR

Errors and exception codes are displayed in the status line and in data traffic.

### Available protocols:

- RTU(serial)
- TCP/IP
- RTU over TCP/IP

### Operating systems:

- Windows 7, 10 and 11 (64 bits).
- Linux "Various" (64-bit).
  
On Linux, simply extract the file and use it.

### ATTENTION UBUNTU USERS: 
- Do not drag the file to the desktop; it will not work there. Use it in the download folder or any other folder.

### ATTENTION LINUX USERS: 
- The images and software were created using Linux Mint (Cinnamon or Xfce). Depending on the distro/theme or appearance, the items may appear distorted or even hidden on the sides. For example, in Xubuntu, the items are misaligned.

### Note: on some operating systems Linux, it is necessary to install the GTK2 library

- Lubuntu , Kubuntu = sudo apt-get install libgtk2.0-dev

- Fedora = sudo dnf install gtk2-devel

### In languages:

- Portuguese.
- Spanish.
- English.
- Italian


# Link Download:

https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/releases/
***

For software questions, update notifications, and bug reports:

WhatsApp Group in Portuguese 
https://chat.whatsapp.com/D8ZMNuLCYgLK8Eeg8LdmF6

WhatsApp Group International.
https://chat.whatsapp.com/JjndsgL4jXF7VfToQ3cuBN

Telegram Group (All) 
https://t.me/Scanbus_br

YouTube Channel
https://www.youtube.com/channel/UCU19Zzi0tI-7OPVz2x3Vh9Q

***

## Traffic Data:
Search the input and output bytes (in hexadecimal format).

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Traffic_Data.png)
#### Options:
- Show or hide valid data (useful for discovering occasional communication errors).
- Show or hide errors.
- Save to .CSV file (with separator choice)
- Search for a specific term; the cell containing the terms will be highlighted in yellow.
- If there are errors, they will appear in the status column, and the cell will be highlighted in red.
- Start/Pause button.
  
Note: If active, you can close the Traffic Data window, and it will continue counting.

  ***

## Connection and adjustment tab: 
#### Serial RTU:

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/menu_rtu.png)

- Reescan Port:
  - Rescan the available serial ports.
- Serial Port:
  - Select the serial port.
- Stopbit bit:
  - 1 or 2
- Delay (Read/Write):
  - If you use more than one table, it is a good idea to set aside time to separate the transmissions.
- Baudrate: 
  - Select the communication speed.
- Parity.
  - select parity, none, even and odd.
- Timeout:
  - Determine the server response waiting time, if it exceeds it, consider it an error.
- ScanRate.
  - Set the scan rate, the time of each question to the slave.


#### TCP/IP:

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/menu_tcp.png)

- Copy Local IP Button:
  - As the equipment's IP must generally belong to the same subnet as the PC to work, the equipment's IP will have a number close to the local IP.
- Edit the IP address:
  - IPV4 addresses and DNS addresses are accepted.
    
 *** Note : In DNS or very slow connections, if a connection is not established, try increasing the timeout.
 
- Edit TCP/IP port:
  -The default port for modbus is 502.
- Set the TCP/IP Protocol used:
  - TCP/IP (Default) or RTU over TCP/IP
- Checking for transaction errors:
  - Used to ensure Frame by frame does not use the previous frame, for very slow networks or networks subject to packet loss it can be disabled.
-  Enable or disable TCP/IP autoconnect:
   - !!! Be careful when activating, as you may fall into an infinite loop (connecting and disconnecting) and crash the software.!!! 
- Timeout:
  - Determine the server response waiting time, if it exceeds it, consider it an error.
- ScanRate.
  - Set the scan rate, the time of each question to the slave.



#### Advanced adjustments:

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/menu_advanced_TCP.png)

- Time to reconnect (TCP/IP only).
- Read only (does not write data).
- Limit the maximum size per packet in Holding, if the packet is smaller than the limit nothing will be done, if it is larger it will be divided into smaller packets, useful for equipment that does not support 125 Words of transmission at a time.
- Limit the maximum size per packet in Analog, if the packet is smaller than the limit nothing will be done, if it is larger it will be divided into smaller packets, useful for equipment that does not support 125 Words of transmission at a time.
- Disconnects the connection in case of error.

***

## Data Reading Screen

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scanbus-BR-linux.png)

- Visualization of values received in decimal, hexadecimal and binary simultaneously.
- Receiving status.
- Receipt count.
- Slave/server response times (minimum, current, average and maximum).
- Number with or without sign.
- [New Table button, Open new universal tables (16, 32 or 64 bit).](#new-universal-table)
- Single-read button.
- [Auto simulation button.](#16-bit-auto-simulation )
- Button to save a table activity log file.
- [Button to open the "wide vision" function window.](#wide-vision-function)


The table offers the following number formats:
  - 16-bit Unsigned Decimal
  - 16-bit Signed Decimal
  - 32-bit Unsigned
  - 32-bit Signed
  - 32-bit Float
  - 64-bit Unsigned
  - 64-bit Signed
  - 64-bit Double
    
With the bit order of:
  - Big endian
  - Little endian
  - Big endian / swap byte
  - Little endian / swap byte

Address display format in the following modes: 
 - Relative (Base-0).
 - Absolute (Base-1).
 - Hexadecimal (Base-0).
 - Hexadecimal (Base-1).
    
Note: The format Addr item is only for modifying the display of addresses in the table, for adjustment use relative addresses (Base-0).

  ***
  
## 16-bit recording window 

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/write_16bits.png)
- Make recordings in:
  - Coil (Function 05).
  - Holding (Function 06).
  - Multiple coil (Function 15).
    - Until 1998 simultaneous coils. 
  - Multiple holding (Function 16).
    - Up to 123 simultaneous holdings 

 - For function 06, values ​​can be in: 
   - Decimal.
   - Hexadecimal.
   - Binary. 

***
## 32-bit recording window 

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/write_32bits.png)

- For function 06 or 16, values ​​can be in: 
   - Decimal.
   - Hexadecimal.
- Optional to send with double sending with function 06 or single sending with function 16 (default). 
***

## 64-bit recording window

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/write_64bits.png)

***

## 16-bit Auto Simulation 
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Auto_Simulation.png)
- Make automatic recordings:
  - adjust the address for auto simulation (multiple independent addresses can be adjusted by simply selecting the desired address, adjusting and enabling it):
    - Operating modes:
      - Increment
      - Decrement
      - Random
    - Time adjustment for each recording.
    - Adjust steps.
    - Adjust minimum value (accepts negative values).
    - Set maximum value (accepts negative values).
  - Select recording mode (Global);
    - Function 06 (default).
    - Function 16.
      
Note: " Automatic Simulation" will only work while the window is open and the table is set to 16 bits. The address that has "automatic simulation" will be colored green in the table.

***

## Log. windows
Keep a log of table activity.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Log_register.png)

- Checkbox (Write log?).
- Set the file name:
  - The file in Windows will be saved in the same directory as the executable file, in Linux it can be in the same directory or in the home folder.
- Extension, choose the type of file to be saved, TXT and CSV (opens in excel). 
- Separator (SEP), choose the data separator between comma or semicolon.
- Choose the types of data to collect:
  - Errors
  - Date
  - Time
  - ID
  - Function
  - Addresses
    
 ***
 
## New Universal Table

Open new tables in floating windows.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Universal_table.png)

Universal tables, in the connection section, click on the new table button, the tables contain settings for viewing registers up to (125 = 16 bits, 64 = 32 bits, 32 = 64 bits), adjustable size windows/tables with fixed hexadecimal values ​​in all modes and with configurable format.

With the Formats of:
  - 16-bit Binary
  - 16-bit Unsigned Decimal
  - 16-bit Signed Decimal
  - 32-bit Unsigned
  - 32-bit Signed
  - 32-bit Float
  - 64-bit Unsigned
  - 64-bit Signed
  - 64-bit Double
    
With the bit order of:
  - Big endian
  - Little endian
  - Big endian / swap byte
  - Little endian / swap byte

Note: The format Addr item is only for modifying the display of addresses in the table, for adjustment use relative addresses (Base - 0).

***

## Special functions

### Time graph:
Generates graphs (time x values) with the values ​​received via Modbus.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Graphic_time_1.png)
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Graphic_time_2.png)

#### Available up to 8 lines with the following configuration:
- Thread colors 
- Multiplication Factor
- Offset
- Caption
- LINE style
- line width 
- Points on the line
  
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Graphic_time_3.png)

#### Chart options:
- Background color adjustment
- Grid color adjustment
- Gridline Adjustment
- Maximum value (manual)
- Minimum value (manual)
- Auto graph limit adjustment (automatic)
- Time adjustment

***

## Device/Network Scanner: 
Find connected device ID, functions and registers.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scan_Device.png)

#### Options:
- Display only valid data (Avoid filling the table with rows only reporting invalid data, e.g. registers with timeout).
- Show exception (exception indicates that the device ID exists but something is wrongly configured).
- Stop when found (when a valid register is found, the scan ends).
- Stop at the end (when it reaches the value of Id = 255, finish the scan, otherwise it will return to ID 1 cyclically).
- Save to .CSV file (with separator choice).
- Search for a specific term; the cell containing the terms will be highlighted in yellow.
- If there are errors, they will appear in the status column, and the cell will be highlighted in red.

- Filter option according to the received value. The options are:

  - All: regardless of the record value, shows the record as long as it is valid.

  - Greater than: only shows results when the record has a value greater than the entered value.

  - Less than: only shows results when the record has a value less than the entered value.

  - Equal to: only shows the record that has the same value as the entered value.

  - Different from: hides the record if the record value is equal to the entered value.
  
- Can be set to values: 
  - 16 bits unsigned (default).
  - 16 bits signed.
  - 32 bits unsigned.
  - 32 bits signed.
  - 32 bits floating point.
    
For 32-bit values the following byte order is available: 
- Big endian
- Little endian
- Big endian / byte swap
- Little endian / byte swap
    
Note:
- 32-bit values ​​use 2 word (4 bytes) wide registers.

***

## Serial RTU Scanner:
Find the serial configuration of the connected device

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scan_RTU.png)

#### Scanner of: 
- BaudRate
- Parity:
  - None, Odd, Even.
- StopBit:
  - 1 and 2
- ID:
  - from 1 to 255
- Function:
  - If "All" is selected, the following functions will be scanned: (01 Coil, 02 Digital, 03 Holding, 04 Analog).
- Addresses:
  - from 0 to 65535.

Note:
  
  Use the same connection as the simulator.

  With the exception of some exotic baudRate.
    
  The software is capable of checking all network/device "Modbus RTU" combinations, however,depending on the amount of data you put in for scanning, it can be extremely time-consuming. 
    
  Each item added simply doubles the scanner time. 
    
  The more information you have about your device or network, the more items NOT existing on your device you can remove,making the scanner faster.

  In this scanner, only truly valid data (valid + exceptions) is accepted, unlike other scanners that consider any Echo/Noise on the network as a valid result.

Attention!!!

  The scan takes about two and a half hours to complete at default settings. With each item added to the default settings, the time doubles.
***

## TCP Scanner:
Find the device's IP and TCP port.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scan_TCP.png)

#### Scanner of: 
- IP (TCP)
- Port
- ID 

You will need to know in advance the function and address that the equipment responds to.

Note:
- The scanned device or network must be in the same IP range as the computer.

- To perform the TCP/IP Scanner it is NOT NECESSARY to establish a valid connection, just press the connection button.

***
## Wide vision function
Individually check which 16-bit registers are active.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/wide_vision_1.png)
- In the register where there is activity, the address cell will turn red for the time specified in "signaling time".

***

## Terminal Serial
#### Simple serial terminal (decimal , hexadecimal and text).

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Terminal_serial.png)

- FDTI chip?:
  - For correct operation when using converters with these chips and using the "lines per frame" function.
    The COM port is ignored, and the device that is not in use will be connected.
    Only for Windows version, Linux is not supported at the moment.

- Dec/HEX/Text:
  - Select whether the read and written bytes are in decimal , hexadecimal or Text (ASCII).
    
- Lines per frame : 
  - Each received packet is skipped by one line.
    For FTDI chips, select the FTDI Chip? function before connecting (support for Windows only).

- Show Sent:
  - Shows the bytes sent on the screen.
 
- Separator:
  - Place any character separating the Bytes
 
- Line counter:
  -  Line count written on screen.

- Count of the last packet received.

- Search for a specific term.

#### SPY Mode - Modbus-RTU.
Find out what data the master device is sending to the slave.
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/SPY_Mode_1.png)
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/SPY_Mode_2.png)

It can be used to discover data sent by the master, for example: what an HMI is sending to a PLC. It can also be used to debug equipment/software that you are programming as a master to validate the data sent by it.

- Filters:
   - Search only by ID.
   - Search only by function.
   - Mode:
      - Chronological:
         - Displays data on the screen in the order it is captured.
      - Don't Repeat:
         - If the results are identical, i.e. they reappear more than once on the screen, subsequent identical results will not be shown, the data includes (ID, Function, Address, Quantity/Value).

- Simulate Modbus Slave:
  - Activates an internal Modbus RTU slave simulator.
  - This simulator responds to any ID (when zero) or to an ID you specify.
  - It is particularly useful for testing only on the master device.
  - Open Slave Table button.

  - Table Slave:
    - ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Table_Slave.png)

    - ID Edit.
    - Function Edit.
    - Address Edit.
    - Editing the number of registers.
      
    - Numeric format changer:
      - 16 bits unsigned.
      - 16-bit signed.
      - 32-bit unsigned.
      - 32-bit signed.
      - 32-bit float.
        
    - Byte order:
      - Big-endian.
      - Little-endian.
      - Big-endian / Byte Swap
      - Little-endian / Byte Swap
     
    - Write button. Opens a window to write the value.
    - Clear data button, deletes all received data.
          
      - Write slave:      
        - ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Write_Slave.png)
        - ID Edit.
        - Function Edit.
        - Address Edit.
        - Value.
        - Write button or ON OFF buttons (coil or discrete input).
   
  - Note: The internal slave simulator will always respond to all standard functions (01 Coil, 02 Input discrete, 03 Holding, 04 Input register, 05 Write Coil, 06 Write Holding, 15 Multiple Write Coil, 16 Multiple Write Holding) and register addresses from 0 to 65535 without any configuration.
          
- Notes:
  - Functions 15 and 16 have a limitation due to the USB converter, which typically splits the packet into 32-byte segments. As a result, packets larger than 32 bytes (approximately 10 registers) may not be detected.

  - When functions 5 or 6 occur, they may appear duplicated, as the slave's response is the same as the master's question.
 
***
#### Did you like ScanBus-BR ? 

It was created with great care and dedication. 

Your donation allows me to maintain and improve this software free of charge for everyone. 

Any donation is welcome. 
Thank you for your contribution! 

Rodrigo F. Hernandes
***

# Donation via Paypal:
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/QR%20Code.png)

https://www.paypal.com/donate/?hosted_button_id=6EUN9X4VDY88N


# Donation via PIX:
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Pix_ScanBus-BR.jpeg)

  
***
