# ScanBus-BR Modbus Master/Client Simulator. 

_"The most complete GUI (Graphical User Interface) for Linux."_

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scanbus-BR-linux.png)

## What is ScanBus-BR?

ScanBus-BR is a free Modbus Master / Client simulator software (Freeware) that stands out for its versatility and simplicity.

The ScanBus is PORTABLE, meaning it DOES NOT REQUIRE INSTALLATION and can be used even on pen drives.

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

Note: on some operating systems Linux, it is necessary to install the GTK2 library

### In languages:

- Portuguese.
- Spanish.
- English.
  
***
***
# Link Download:
http://www.scanbus.com.br

***
***

## Hex Dump:
Search the input and output bytes (in hexadecimal format).

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Traffic_Data.png)
#### Options:
- Show or hide valid data (useful for discovering occasional communication errors).
- Show or hide errors.
- Save to .CSV file (with separator choice)

  ***

## Connection and adjustment tab: 
![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/aba_conexao.png)

- Serial RTU.
- TCP/IP.
- Record log.
- Advanced adjustments.

***

## 16-Bit Data Reading Screen:

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scanbus-BR-linux.png)

- Two 16-bit tables.
- Visualization of values received in decimal, hexadecimal and binary simultaneously.
- Receiving status.
- Receipt count.
- Slave/server response times (minimum, current, average and maximum).

## 16-bit recording window: 

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Recorde_16bits.png)

***

## 32-Bit Data Reading Screen:

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Screeen_32bits.png)

- Visualization of values received in decimal or float, hexadecimal and binary simultaneously.
- Receiving status.
- Receipt count.
- Slave/server response times (minimum, current, average and maximum).

## 32-bit recording window: 

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Recorde_32bits.png)

***

## 64-Bit Data Reading Screen: 

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Screeen_64bits.png)

- Receiving status.
- Receipt count.
- Slave/server response times (minimum, current, average and maximum).

## 64-bit recording window:

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Recorde_64bits.png)

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

## Device Scanner: 
Find connected device ID, functions and registers.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scan_Device.png)

#### Options:
- Display only valid data (Avoid filling the table with rows only reporting invalid data, e.g. registers with timeout).
- Show exception (exception indicates that the device ID exists but something is wrongly configured).
- Stop when found (when a valid register is found, the scan ends).
- Stop at the end (when it reaches the value of Id = 255, finish the scan, otherwise it will return to ID 1 cyclically).
- Save to .CSV file (with separator choice).

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
- big endian
- little endian
- big endian / byte swap
- little endian / byte swap
    
Note:
- 32-bit values ​​use 2-byte wide registers.

***

## Serial RTU Scanner:
Find the serial configuration of the connected device

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scan_RTU.png)

***

## TCP Scanner:
Find the device's IP and TCP port.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/Scan_TCP.png)

#### Scanner of: 
- IP (TCP)
- Port
- ID 

You will need to know in advance the function and address that the equipment responds to.

***

## Wide vision function:
Individually check which 16-bit registers are active.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/wide_vision_1.png)

Apply multiplication factor, decimal place and off set to 16-bit values.

![ScanBus-BR](https://github.com/ortegahernandes/ScanBus-BR/blob/main/wide_vision_2.png)

