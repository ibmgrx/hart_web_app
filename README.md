HART Serial Debugger
====================

A lightweight, browser-based tool for debugging and configuring HART field devices via serial communication using the Web Serial API (Chrome/Edge only).

![HART Serial Debugger Screenshot](screenshot.jpg)

**Key Features**
- Connects to serial ports at 1200 baud, 8-O-1 (standard HART)
- Preset buttons for common universal commands:
  - Cmd 0 – Initialize
  - Cmd 1 – Read Primary Variable (PV)
  - Cmd 2 – Read Loop Current & Percent of Range
  - Cmd 3 – Read All Dynamic Variables (PV, SV, TV, QV)
  - Cmd 18 – Write Tag, Descriptor, Date (packed ASCII format)
  - Cmd 22 – Write Long Tag (32 Latin-1 characters, direct byte mapping)
- Manual raw hex mode – send any byte sequence, response shown as-is (no forced HART parsing)
- Automatic response decoding for preset commands (PV values with units, status, Tag/Long Tag echo)
- Clean, timestamped log with color coding (sent, received, decoded, error)
- Responsive grid UI for quick access in the field

**Requirements**
- Browser: Google Chrome or Microsoft Edge (Web Serial API support)
- OS: Windows 10/11, macOS, Linux
- Hardware: USB-serial adapter + HART-compatible device

**How to Use**
1. Open `index.html` directly in Chrome/Edge
2. Click "Connect (1200, 8-O-1)" and select your serial port
3. Use preset buttons for standard HART commands
4. Or type raw hex in the manual input and send freely
5. Command 18 & 22 prompt for Tag/Descriptor/Date or Long Tag input

**License**
MIT License – feel free to fork, modify, and use in production.

**Author**
© 2026 ibmgrx (@ibmgrx)

Built with pure HTML/CSS/JS – no frameworks, no build tools, no server required.

Happy HART debugging in the field!
