# ScanBus-BR - Guia de Utilitarios / Utilities Guide

> Guia completo de cada utilitario, tela e ferramenta do ScanBus-BR (Sniffer, Scanners, Simulador de Slave, Tabelas, etc). Para apresentacao geral do projeto, download, licenca e contato, veja o [README.md](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/README.md).

# Traffic Data Analyzer

The **Traffic Data Analyzer** provides a real-time view of all Modbus communication exchanged between the master and the connected device.

It is particularly useful for diagnosing intermittent communication problems, validating data integrity, and recording communication sessions for later analysis.

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Traffic_Data.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Traffic_Data.png)

## Features

- Display only valid communication frames.
- Display only communication errors.
- Export captured data to CSV format.
- Select the CSV separator (comma or semicolon).
- Search for hexadecimal values or text.
- Automatic highlighting of search results.
- Error highlighting directly in the table.
- Start and Pause data acquisition at any time.

> **Note**
>
> The Traffic Data window may be closed while acquisition continues in the background.

* * *

# Connection Settings

ScanBus-BR supports both **Serial Modbus RTU** and **Modbus TCP/IP** communication.

Connection parameters can be configured independently for each protocol.

* * *

# Serial Modbus RTU

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/menu_rtu.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/menu_rtu.png)

## Available Settings

### Rescan Ports

Refreshes the list of available serial ports.

Useful when a USB/RS485 converter is connected after ScanBus-BR has already been started.

* * *

### Serial Port

Select the serial interface connected to the Modbus network.

* * *

### Baud Rate

Choose the communication speed supported by the connected device.

* * *

### Parity

Supported modes:

- None
- Even
- Odd

* * *

### Stop Bits

Supported values:

- 1
- 2

* * *

### Read / Write Delay

Adds a delay between Modbus requests.

This option is useful when communicating with slower devices or when multiple tables are active simultaneously.

* * *

### Timeout

Maximum waiting time for a device response.

If no response is received before the timeout expires, the request is considered failed.

* * *

### Scan Rate

Defines how frequently ScanBus-BR polls the connected device.

Lower values provide faster updates but increase communication traffic.

* * *

# Modbus TCP/IP

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/menu_tcp.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/menu_tcp.png)

## Copy Local IP

Copies the computer's local IP address.

This is useful because industrial devices are usually configured within the same subnet.

* * *

### Server Address

Supports:

- IPv4 addresses
- Host names (DNS)

> **Note**
>
> When using DNS or slow Internet connections, increase the timeout value if the connection cannot be established.

* * *

### TCP Port

The default Modbus TCP port is:

```
502
```

Any custom port may also be used.

* * *

### Communication Protocol

Supported options:

- Modbus TCP/IP
- Modbus RTU over TCP/IP

* * *

### Transaction Verification

Verifies transaction identifiers to ensure that every received response belongs to the corresponding request.

For unreliable or high-latency networks, this verification can optionally be disabled.

* * *

### Auto Connect

Automatically reconnects whenever communication is interrupted.

> **Warning**
>
> Incorrect configuration may create an endless reconnect loop.

* * *

### Timeout

Maximum waiting time for server responses.

* * *

### Scan Rate

Defines the polling interval for TCP communication.

* * *

# Advanced Communication Settings

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Modbus_Definition_RTU.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Modbus_Definition_RTU.png)

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Modbus_Definition_TCP.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Modbus_Definition_TCP.png)

The Advanced Settings window provides additional control over communication behavior.

## Available Options

### Automatic Reconnection

Reconnect automatically after communication loss.

(TCP/IP only.)

* * *

### Read Only Mode

Disables every write command.

Useful when monitoring production systems where accidental writes must be prevented.

* * *

### Maximum Holding Register Packet Size

Some Modbus devices cannot process the standard maximum of **125 registers** in a single request.

ScanBus-BR automatically splits large requests into smaller packets.

* * *

### Maximum Input Register Packet Size

Applies the same packet fragmentation to Input Register requests.

* * *

### Disconnect on Communication Error

Automatically closes the connection after a communication failure.

This can simplify recovery in unstable networks.

* * *

# Data Reading Screen

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Scanbus-BR-linux.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scanbus-BR-linux.png)

The main reading window provides continuous monitoring of Modbus registers.

Values are updated automatically according to the configured scan rate.

* * *

## Available Information

- Current register values
- Communication status
- Total received packets
- Current response time
- Minimum response time
- Average response time
- Maximum response time

* * *

## Numeric Display Formats

The same register can be viewed in multiple formats.

Supported formats include:

- 16-bit Unsigned Integer
- 16-bit Signed Integer
- 32-bit Unsigned Integer
- 32-bit Signed Integer
- IEEE754 Floating Point
- 64-bit Unsigned Integer
- 64-bit Signed Integer
- IEEE754 Double Precision

* * *

## Byte Order

Every numeric format supports:

- Big Endian
- Little Endian
- Big Endian + Byte Swap
- Little Endian + Byte Swap

* * *

## Address Display Modes

Addresses may be displayed as:

- Relative Address (Base 0)
- Absolute Address (Base 1)
- Hexadecimal Address

* * *

## Toolbar

The toolbar provides quick access to several functions.

- Create a new Universal Table.
- Perform a single read operation.
- Open the Automatic Simulation window.
- Save communication logs.
- Open the Wide Vision tool.

# Register Write Windows

ScanBus-BR provides dedicated write windows for **16-bit**, **32-bit**, and **64-bit** values, allowing data to be written in the most appropriate format for each application.

The available options automatically adapt according to the selected Modbus function.

* * *

# 16-bit Write Window

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/write_16bits.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/write_16bits.png)

The 16-bit write window supports all standard Modbus write functions.

## Supported Functions

- Function 05 — Write Single Coil
- Function 06 — Write Single Holding Register
- Function 15 — Write Multiple Coils
- Function 16 — Write Multiple Holding Registers

### Maximum Write Size

| Function                   | Maximum       |
|----------------------------|---------------|
| Multiple Coils             | 1998 Coils    |
| Multiple Holding Registers | 123 Registers |

* * *

## Value Formats

Single register values may be entered as:

- Decimal
- Hexadecimal
- Binary

This greatly simplifies debugging and firmware validation.

* * *

# 32-bit Write Window

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/write_32bits.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/write_32bits.png)

The 32-bit write window is intended for devices that store values across two consecutive Holding Registers.

Supported formats include:

- Unsigned Integer
- Signed Integer
- IEEE754 Floating Point

Values may be entered in:

- Decimal
- Hexadecimal

* * *

## Transmission Modes

Two write methods are available:

### Function 06

Writes each register individually.

This option offers maximum compatibility with older devices.

* * *

### Function 16

Writes both registers in a single Modbus command.

This is the default and recommended option whenever supported by the target device.

* * *

# 64-bit Write Window

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/write_64bits.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/write_64bits.png)

The 64-bit write window allows writing values stored across four consecutive Holding Registers.

Supported formats include:

- Unsigned 64-bit Integer
- Signed 64-bit Integer
- IEEE754 Double Precision

All byte-order options available throughout ScanBus-BR are supported.

* * *

# Automatic Register Simulation

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Auto_Simulation.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Auto_Simulation.png)

The Automatic Simulation tool continuously writes values to selected Holding Registers.

It is especially useful for:

- PLC testing
- HMI development
- SCADA validation
- Embedded firmware testing
- Communication stress testing

* * *

## Simulation Modes

Each configured register may operate independently using one of the following modes:

- Increment
- Decrement
- Random

* * *

## Adjustable Parameters

Each simulated register supports:

- Independent address selection
- Write interval
- Step value
- Minimum value
- Maximum value

Negative values are fully supported.

* * *

## Write Function

The simulator can operate using:

- Function 06 (Write Single Register)
- Function 16 (Write Multiple Registers)

Function 16 is recommended whenever the target device supports it.

* * *

> **Important**
>
> Automatic Simulation is available only while the simulation window remains open.
>
> Registers configured for automatic updates are highlighted in **green** within the main table.

* * *

# Communication Log

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Log_register.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Log_register.png)

The integrated logging system records communication activity for later analysis.

Logs can be generated automatically during communication with the Modbus device.

* * *

## Log Options

- Enable or disable logging
- Select the output filename
- TXT output
- CSV output
- Select comma or semicolon separator

* * *

## Recorded Information

The log may include:

- Date
- Time
- Device ID
- Function Code
- Register Address
- Communication Errors

* * *

## File Location

### Windows

The log is stored in the same directory as the ScanBus-BR executable.

### Linux

Depending on the distribution, the file may be stored either beside the executable or inside the user's Home directory.

* * *

# Universal Tables

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Universal_table.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Universal_table.png)

Universal Tables provide an independent floating window for monitoring additional Modbus registers.

Multiple Universal Tables may be opened simultaneously.

Each table operates independently from the main window.

* * *

## Supported Register Sizes

- 125 × 16-bit Registers
- 64 × 32-bit Values
- 32 × 64-bit Values

* * *

## Supported Numeric Formats

- Binary
- Unsigned Integer
- Signed Integer
- IEEE754 Float
- IEEE754 Double

* * *

## Byte Ordering

Every Universal Table supports:

- Big Endian
- Little Endian
- Big Endian + Byte Swap
- Little Endian + Byte Swap

* * *

## Advantages

Universal Tables are ideal when monitoring several unrelated memory regions simultaneously.

Each window can use different:

- Address
- Format
- Byte Order
- Register Size

This greatly simplifies diagnostics in complex PLCs and embedded devices.

* * *

# Time Graph

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Graphic_time_1.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Graphic_time_1.png)

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Graphic_time_2.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Graphic_time_2.png)

The Time Graph tool plots Modbus register values over time.

It is particularly useful for observing trends, oscillations, and dynamic system behavior.

* * *

## Graph Features

Up to **8 independent traces** may be displayed simultaneously.

Each trace supports:

- Custom caption
- Multiplication factor
- Offset
- Line width
- Line style
- Marker points

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Graphic_time_3.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Graphic_time_3.png)

* * *

## Display Options

The graph appearance can be customized through:

- Background Color
- Grid Color
- Grid Visibility
- Automatic Scale
- Manual Minimum
- Manual Maximum
- Time Scale

These settings allow the graph to be optimized for both slow-changing variables and high-speed signals.

* * *

# Device Library

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Device_Library.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Device_Library.png)

The **Device Library** lets you find the Modbus register map of a device by brand or model.

Instead of entering registers one by one, you pick the device and load a ready-made map to start communicating.

* * *

## Finding a Device

There are two ways to choose a device in the selection box:

- **Select** it from the drop-down list.
- **Type** the brand (or part of the name). The box autocompletes as you type.

> **Note**
>
> The maps are stored in `maps.zip`, located beside the ScanBus-BR executable. Each device is described by a JSON file listed in the `index.json` of the zip.

* * *

## Device Information

Besides the registers, each map carries extra information that is useful for communication. It is shown in the panel beside the register table.

| Section           | Content                                                                   |
|-------------------|---------------------------------------------------------------------------|
| **Vendor**        | Manufacturer and website                                                  |
| **Models**        | Models covered by the map                                                 |
| **Configuration** | Protocol, serial settings, firmware, byte order, Unit ID and map revision |
| **Documentation** | Documentation source and link                                             |
| **Notes**         | Important remarks about the device                                        |

The panel also shows a device description and a **reliability level** for the map:

| Level          | Meaning                                   |
|----------------|-------------------------------------------|
| **Official**   | Based on the manufacturer's documentation |
| **Verified**   | Tested in the field                       |
| **Unofficial** | Not official, use with care               |
| **Unknown**    | No information available                  |

* * *

## Register Table

When a device is selected, the table lists every register in the map:

- Area
- Address (hexadecimal)
- Address (decimal)
- Name
- Type
- Unit
- Access

The search box filters the table while you type. It searches all columns and ignores upper/lower case (for example `voltage`, `0010h`, `float32` or `RW`).

> **Note**
>
> Before using a register or importing the map, check the **Device ID** field. The suggested value comes from the map when it defines one, otherwise it is `1`.

* * *

## Double-Click: a Single Register

**Double-click** a row in the table to open **only that register** in a separate window, ready for communication.

The window is a [Universal Table](#universal-tables). The serial settings of the map are applied and the register name is kept as an alias.

* * *

## Import: All Registers

The **Import** button loads the whole map:

1. Applies the communication settings defined in the map (for example, serial) and the Device ID.
2. Stores each register name as an alias. Bits inside a word receive the bit name.
3. Opens the **Register Window** with every item of the map, **initially all disabled**.

* * *

## Exporting the Register List

The **Save** button of the Device Library exports the register list of the selected device as:

- TXT
- CSV
- RTF

* * *

# Register Window

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Library_Window.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Library_Window.png)

The Register Window shows all registers imported from the Device Library.

Each row has a checkbox in the **Active** column. Only checked rows are read from the device.

* * *

## Selecting Registers

- Check **item by item** to read only what you need.
- Use the **select all** button to enable the entire table.
- Use the **clear all** button to uncheck everything at once.

* * *

## Columns

- Active
- Register (Dec.)
- Register (Hex.)
- Alias
- Function
- Value
- Unit
- Type
- Access

The displayed value already applies the register type (`uint16`, `int32`, `float32`, bit, etc.), scale and offset, and the byte and word order defined in the map.

* * *

## Writing to a Register

Double-click a row to write to that register.

Writing is only available for coils and holding registers with write access, and only while ScanBus-BR is connected to the device.

* * *

## Communication Indicator

The window shows the communication status with an LED and a packet counter.

| LED         | Meaning                                             |
|-------------|-----------------------------------------------------|
| Green blink | The read cycle finished with all responses OK       |
| Red blink   | At least one register had an error during the cycle |
| Off         | No new response                                     |

The **packet counter** counts complete read cycles, meaning one pass over all active registers.

> **Note**
>
> The counter is reset whenever a new device is loaded.

* * *

# Network Scanners

One of the strongest features of ScanBus-BR is its collection of built-in scanners.

Instead of manually testing each Modbus address or communication parameter, the scanners automate the discovery process, significantly reducing commissioning and troubleshooting time.

* * *

# Device / Network Scanner

Automatically discovers valid Modbus devices, supported functions and accessible registers.

[![](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/raw/main/Imagens/Scan_Device.png)](https://github.com/ortegahernandes/ScanBus-BR-Simulator-Modbus/blob/main/Imagens/Scan_Device.png)

The scanner is especially useful when little or no documentation is available for the target equipment.

Typical applications include:

- PLC commissioning
- Reverse engineering
- Industrial maintenance
- Device validation
- Unknown equipment analysis

* * *

## Features

- Automatic Device ID scanning
- Function Code scanning
- Register Address 
