# Third-Party Software and Licenses

The "ScanBus-BR" software is distributed under a Freeware (commercial use allowed) license.

This document lists the third-party components used by ScanBus-BR and their respective licenses.

## Third-Party Components

| Component                           | License                                                                                                               |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Lazarus LCL                         | LGPL v2.1 with Static Linking Exception                                                                               |
| Free Pascal Runtime Library (RTL)   | LGPL v2.1 with Static Linking Exception                                                                               |
| Free Pascal Component Library (FCL) | LGPL v2.1 with Static Linking Exception                                                                               |
| Qt 5 (Open Source Edition)          | LGPL v3                                                                                                               |
| Qt5Pas                              | LGPL v3 or later with Linking Exception                                                                               |
| [PascalSCADA](https://github.com/fluisgirardi/pascalscada/blob/master/LICENSE.modifiedLGPL.txt) | Modified LGPL (LGPL with Linking Exception) |
| [DataPort](https://github.com/serbod/dataport/blob/master/LICENSE.md)                           | MIT License                                 |
| [Synapse](https://www.ararat.cz/synapse/doku.php/license)                                       | BSD License                                 |
| [Indy for Lazarus](https://www.indyproject.org/license/bsd/)                                    | Modified BSD / MPL 1.1 (dual license)       |
| [mbmap-library](https://github.com/nobrega8/mbmap-library/blob/main/LICENSE)                    | CC0 1.0 Universal (Public Domain)           |
| Liberation Fonts                    | SIL Open Font License 1.1 (OFL 1.1)                                                                                   |
| XCB Utility Libraries               | MIT/X11 License                                                                                                       |

Other libraries used are native to Lazarus: https://www.lazarus-ide.org/index.php?page=features

ScanBus-BR is developed with Lazarus / Free Pascal.

---

## Project Notes

### Qt Framework

ScanBus-BR uses the Open Source edition of Qt 5 through the Lazarus Qt5 interface (Qt5Pas).

Qt libraries are distributed in accordance with their respective Open Source licenses (LGPL v3).

### PascalSCADA

ScanBus-BR uses a modified version of PascalSCADA.

Some modifications were developed specifically to meet the requirements of this project.

These modifications were shared with the original PascalSCADA author. They were not incorporated into the upstream project because they did not align with the project's design goals, although they were received as a useful technical reference.

PascalSCADA remains copyrighted by its original authors and continues to be distributed under its original license.

### mbmap-library

ScanBus-BR uses mbmap-library, an open JSON format and community-driven library of Modbus device register maps, released under CC0 1.0 Universal (public domain dedication).

### Fonts

This application includes Liberation Fonts, distributed under the SIL Open Font License 1.1.

---

## License Compliance

The ScanBus-BR project respects the licenses of all third-party software used during development and distribution.

Whenever required by the corresponding licenses:

- Original copyright notices are preserved.
- License texts are distributed with the application.
- Third-party components remain the property of their respective copyright holders.

No ownership is claimed over any third-party software included or referenced by this project.

---

## Copyright

Copyright © 2021–2026 Rodrigo Hernandes.

ScanBus-BR is an independent software project.

All trademarks, product names and company names mentioned in this software or documentation are the property of their respective owners.
