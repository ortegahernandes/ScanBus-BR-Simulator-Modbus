# ScanBus-BR Modbus Simulator Master/Client and Sniffer Modbus RTU. 
 **For Windows and Linux**

_The "Swiss Army Knife" of the Modbus network_.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scanbus-BR-linux.png)

### ATTENTION THIS SOFTWARE IS DISTRIBUTED COMPLETELY VOLUNTARILY. USE IT IF YOU WISH.

### !!! ATTENTION LINUX USERS !!!: 

- This project includes a precompiled Linux binary (ELF).
Because it is new and not widely downloaded, Chrome may warn that the file is uncommon.
This is expected and does not indicate malware.

- The images and software were created using Linux Mint (Cinnamon ,Xfce or Mate). Depending on the distro/theme or appearance, the items may appear distorted or even hidden on the sides. For example, in Xubuntu, the items are misaligned.

 #### Note: on some operating systems Linux, it is necessary to install the GTK2 library:

- Lubuntu , Kubuntu, Debian = sudo apt-get install libgtk2.0-dev

- Fedora = sudo dnf install gtk2-devel

  
### !!! ATTENTION UBUNTU USERS !!!: 
- Do not drag the file to the desktop; it will not work there. Use it in the download folder or any other folder.


### !!! ATTENTION WINDOWS USERS !!!: 

SmartScreen images in Portuguese; you can modify the text in your language.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Windows%20smartscreen%2001.png)
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Windows%20smartscreen%2002.png)

- Why doesn't ScanBus-BR have a digital signature?
  
   - To be recognized by Windows, a digital signature is required. I distribute ScanBus-BR for free (Freeware) and on a voluntary basis. ScanBus-BR does not generate any income and I do not have the resources to pay for a digital signature.

- How to run ScanBus-BR?

   - Click on:
      - More Information
      - Run anyway



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

### In languages:

- Portuguese.
- Spanish.
- English.
- Italian

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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Traffic_Data.png)
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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/menu_rtu.png)

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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/menu_tcp.png)

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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Modbus_Definition_RTU.png)
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Modbus_Definition_TCP.png)

- Time to reconnect (TCP/IP only).
- Read only (does not write data).
- Limit the maximum size per packet in Holding, if the packet is smaller than the limit nothing will be done, if it is larger it will be divided into smaller packets, useful for equipment that does not support 125 Words of transmission at a time.
- Limit the maximum size per packet in Analog, if the packet is smaller than the limit nothing will be done, if it is larger it will be divided into smaller packets, useful for equipment that does not support 125 Words of transmission at a time.
- Disconnects the connection in case of error.

***

## Data Reading Screen

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scanbus-BR-linux.png)

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
  - 32-bit Float "IEEE754"
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
  
  ***
  
## 16-bit recording window 

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/write_16bits.png)
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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/write_32bits.png)

- For function 06 or 16, values ​​can be in: 
   - Decimal.
   - Hexadecimal.
- Optional to send with double sending with function 06 or single sending with function 16 (default). 
***

## 64-bit recording window

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/write_64bits.png)

***

## 16-bit Auto Simulation 
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Auto_Simulation.png)
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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Log_register.png)

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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Universal_table.png)

Universal tables, in the connection section, click on the new table button, the tables contain settings for viewing registers up to (125 = 16 bits, 64 = 32 bits, 32 = 64 bits), adjustable size windows/tables with fixed hexadecimal values ​​in all modes and with configurable format.

With the Formats of:
  - 16-bit Binary
  - 16-bit Unsigned Decimal
  - 16-bit Signed Decimal
  - 32-bit Unsigned
  - 32-bit Signed
  - 32-bit Float "IEEE754"
  - 64-bit Unsigned
  - 64-bit Signed
  - 64-bit Double
    
With the bit order of:
  - Big endian
  - Little endian
  - Big endian / swap byte
  - Little endian / swap byte

***

## Special functions

### Time graph:
Generates graphs (time x values) with the values ​​received via Modbus.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Graphic_time_1.png)
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Graphic_time_2.png)

#### Available up to 8 lines with the following configuration:
- Thread colors 
- Multiplication Factor
- Offset
- Caption
- LINE style
- line width 
- Points on the line
  
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Graphic_time_3.png)

#### Chart options:
- Background color adjustment
- Grid color adjustment
- Gridline Adjustment
- Maximum value (manual)
- Minimum value (manual)
- Auto graph limit adjustment (automatic)
- Time adjustment

***

### Device/Network Scanner: 
Find connected device ID, functions and registers.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scan_Device.png)

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
  - 32 bits floating point "IEEE754".
    
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

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scan_RTU.png)

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

### TCP Scanner:
Find the device's IP and TCP port.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scan_TCP.png)

#### Scanner of: 
- IP (TCP)
- Port
- ID 

You will need to know in advance the function and address that the equipment responds to.

Note:
- The scanned device or network must be in the same IP range as the computer.

***

## Wide vision function
Individually check which 16-bit registers are active.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/wide_vision_1.png)
- In the register where there is activity, the address cell will turn red for the time specified in "signaling time".

***

### Sniffer "SPY" / Terminal.

#### Note: since the analysis is done via an RS485 line, there is no separation between transmitters and receivers. Therefore, in very rare cases, false positives may occur despite the filters in the programming.

### ATTENTION, THE BEST RESULTS WERE OBTAINED WITH CONVERTERS WITH THE CH340/CH343 CHIP.


#### Serial connection menu.
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Menu_Sniffer.png)

- Rescan button: Lists available serial ports, useful if you have connected the USB/serial converter after opening the software.

- COM Port: Select the COM port to which your network/device is connected.

- Virtual Port (Linux only): Displays internal ports.

- Data Bit: Select according to the device/network to be analyzed; note: if using Modbus RTU, always use 8.

- Stop Bit: Select according to your network/device.

- Parity: Select according to your network/device.

- Baud Rate: Select according to your network/device.

- LED "Buffer Full": Indicates that the Merged analysis table has reached its data limit.

- LED "AT": Indicates activity on the serial port.
  - The AT LED also indicates the connection status according to its color:
    - Blue = Never connected
    - Yellow = Connection problem
    - Red = Connected / inactive for more than 250ms.
    - Green / Black = Activity.
    - Aqua = Disconnected.
 
- LED "TX": Indicates that it has received data from a Modbus RTU Master.

- LED "RX": Indicates that it has received data from a Modbus RTU Slave.

- Real Time visualization:
  - With the "Real Time visualization" enabled:
    - You will see updates on the screen every 50 received data points or if no data is received for 100 ms'
    - 'Occasional data loss or misalignment between "master and slave" may occur'
   
  - With the "Real Time visualization" disabled:
    -  You will only see the data when the buffer is full or when data collection is stopped'
    -  Data loss or misalignment between "master and slave" is extremely rare'

  - The disabled mode "Real Time visualization" is extremely useful for saving the .CSV file for external analysis.'
  - Note: best results are achieved with converters using CH340/CH343 chips.'; 

- Connect/Disconnect Button: Connects and disconnects the serial port. Note: To use Modbus RTU analysis, remember to select the "Enable" item below.
  - Note: If you are using the serial terminal for non-Modbus data, leave the "Enable" option disabled.

- Clear Button: Clears all data from the table/terminal.
  
- A/B reversal detector for RS485 networks.
  - Detects if the A/B wires connected to the ScanBus-BR are swapped.
  - Valid only for Modbus RTU data.


#### Simple serial terminal (decimal , hexadecimal and text).
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Terminal_serial.png)

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


#### Table settings:

- Simulate Modbus Slave:
- ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Filter_Slave_Save_Sniffer.png)
  - Activates an internal Modbus RTU slave simulator.
  
  - Using the "Select ID" button, you can enable or disable slave IDs; by default, all are enabled.
    - ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Slave_ID.png)
      - "Select all IDs" button, fill all IDs.
      - "Deselect all IDs" button; removes all IDs.
  - Error simulation:
    -  ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Error_simulations.png)
      - Responds with an incorrect ID.
      - Responds with an incorrect CRC.
      - Responds with an exception code based on the selection.
        - None
        - 01 Illegal Function
        - 02 Illegal Data Address
        - 03 Illegal Data Value
        - 04 Slave Device Failure
        - 05 Acknowledge
        - 06 Slave Device Busy
        - 07 Negative Acknowledge
        - 08 Memory Parity Error
        - 0A (10) Gateway Path Unavailable
        - 0B (11) Gateway Target Device Failed to Respond
      - Responds with a delay
      
     
  - It is particularly useful for testing only on the master device.
  - Open Slave Table button.

  - Editable slave table:
    - ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Table_Slave.png)

    - ID Edit.
    - Function Edit.
    - Address Edit.
    - Editing the number of registers.
      
    - Numeric format changer:
      - 16 bits unsigned.
      - 16-bit signed.
      - 32-bit unsigned.
      - 32-bit signed.
      - 32-bit float "IEEE754".
        
    - Byte order:
      - Big-endian.
      - Little-endian.
      - Big-endian / Byte Swap
      - Little-endian / Byte Swap
     
    - Save button: Saves the table values ​​for all (ID, Function, Addresses), the file size is approximately 160Mb.
    - Open button: Opens the saved file of table values.
    - Clear button: Deletes all values ​​from the table.
    - Write button: Opens a window to enter the value.
          
      - Write slave:      
        - ![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Write_Slave.png)
        - ID Edit.
        - Function Edit.
        - Address Edit.
        - Value.
        - Write button or ON OFF buttons (coil or discrete input).
   
  - Notes:
    - The internal slave simulator will always respond to all standard functions (01 Coil, 02 Input discrete, 03 Holding, 04 Input register, 05 Write Coil, 06 Write Holding, 15 Multiple Write Coil, 16 Multiple Write Holding) and register addresses from 0 to 65535 without any configuration.

#### Merge Table analysis:

Shows the requests from the Master and the responses from the slaves.
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Sniffer_SPY_Merge.png)

- Use the filters if you want only master or slave, only one ID, or only one function.
  
 - With support for:
    - Exception codes.
    - Coil (01)
    - Discrete input (02)
    - Holding (03)
    - Input register (04)
    - Write coil (05)
    - Write holding (06)
    - Partial support (with limitations):
      - Multiple write coil (15)
      - Multiple write holding (16)

    - Note:
      - The generated file can be analyzed by ChatGPT or DeepSeek; preferably include additional information such as the baud rate and the type of communication (RS485).
      - The best results in networking were obtained with the USB/RS485 converters with CH340 or CH343 chips.

#### Parse-Modbus Table:

Shows each unique value on the network; if there are repetitions, they are added to the count.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Sniffer_SPY_Parse.png)

- With support for:
    - Exception codes.
    - Coil (01)
    - Discrete input (02)
    - Holding (03)
    - Input register (04)
    - Write coil (05)
    - Write holding (06)
    - Partial support (with limitations):
      - Multiple write coil (15)
      - Multiple write holding (16)

#### Warning: If you are using USB/RS485 converters with an FTDI chip, adjust the converter timing in the Windows device manager to 1ms.
The best results in networking were obtained with the USB/RS485 converters with CH340 or CH343 chips.
***

### Did you like ScanBus-BR ? 

It was created with great care and dedication. 

Your donation allows me to maintain and improve this software free of charge for everyone. 

Any donation is welcome. 
Thank you for your contribution! 

Rodrigo F. Hernandes

# Donation via Paypal:
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/QR%20Code.png)

https://www.paypal.com/donate/?hosted_button_id=6EUN9X4VDY88N


# Donation via PIX:
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Pix_ScanBus-BR.jpeg)

  
***
