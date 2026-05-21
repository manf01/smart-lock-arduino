# smart-lock-arduino
An Arduino-based smart lock system that controls secure door access using keypad PIN and RFID card authentication — built as part of a Computer Engineering course at CUNY New York City College of Technology (Fall 2025).

-----

📸 Project Overview

This project simulates a real-world access control system. An authorized user can unlock a door by entering a correct PIN via keypad or scanning a registered RFID card. Unauthorized attempts trigger an error state with visual feedback, and repeated failures engage a lockout mechanism.

-----

⚙️ Hardware Components

|Component                 |Purpose                  |
|--------------------------|-------------------------|
|Arduino Uno               |Main microcontroller     |
|4x4 Keypad                |PIN input                |
|RFID Reader (RC522)       |Card-based authentication|
|Servo Motor               |Physical lock actuation  |
|16x2 LCD Display          |Real-time status messages|
|LED Indicators (Red/Green)|Visual access feedback   |
|Breadboard & Jumper Wires |Circuit assembly         |

-----

💻 Software & Tools

- Language: Embedded C/C++
- IDE: Arduino IDE
- Libraries: `MFRC522` (RFID), `LiquidCrystal_I2C` (LCD), `Servo`

-----

🔧 Features

- Dual authentication: keypad PIN entry and RFID card scan
- Real-time LCD feedback (“Access Granted” / “Access Denied”)
- Green/Red LED indicators for immediate visual status
- Servo motor drives physical lock open/close
- Invalid entry lockout after 3 failed attempts
- Modular, well-commented C/C++ codebase

-----

🧠 How It Works

1. System initializes and displays “Enter PIN or Scan Card” on LCD
2. User inputs a 4-digit PIN via keypad **or** scans an RFID card
3. Firmware compares input against stored credentials
4. On success → servo rotates to unlock position, green LED lights, LCD shows “Access Granted”
5. On failure → red LED flashes, LCD shows “Access Denied”, failure counter increments
6. After 3 failures → system locks out for 30 seconds

-----

📐 Circuit Diagram

><img width="504" height="197" alt="Screenshot 2026-05-21 at 11 12 54 AM" src="https://github.com/user-attachments/assets/3a3df442-9c3a-43e1-ae72-747b74a85f3d" />


-----

🚀 What I Learned

- Embedded C/C++ firmware development for real-world authentication logic
- Hardware-software integration across multiple components simultaneously
- Real-time I/O handling with microcontrollers
- Debugging embedded systems using serial monitor and LED diagnostics
- Designing for reliability: error handling, edge cases, and system recovery

-----

🏫 Academic Context

Institution: CUNY – New York City College of Technology, Brooklyn, NY  
Program: B.S. Computer Engineering  
Semester: Fall 2025
