# Secure-Lock-System-with-OTP-Verification

**Description:**
This Arduino sketch implements a secure lock system with a one-time password (OTP) verification mechanism. The system consists of an Arduino board connected to a servo motor for locking/unlocking, and two LEDs serving as status indicators. Communication with the Arduino board is established through a serial interface, enabling remote control and verification of passwords.

**Components:**
- Arduino Board: Utilizes an Arduino board (e.g., Arduino Uno) as the main microcontroller.
- Servo Motor: Controls the physical locking mechanism.
- LEDs: Two LEDs serve as indicators for system status.
- Serial Interface: Facilitates communication between the Arduino board and an external device (e.g., computer or another microcontroller).

**Setup:**
 - Hardware Setup:
    - Connect the servo motor to pin 9 of the Arduino board.
    - Connect two LEDs to digital pins 12 and 13 of the Arduino board, serving as status indicators.
- Software Setup:
  - Install the Arduino IDE on your computer.
  - Copy and paste the provided Arduino sketch (.ino file) into the Arduino IDE.
  - Upload the sketch to the Arduino board.

**Usage:**
  - Power On:
    - Ensure the Arduino board is properly powered.
  - Serial Communication:
    - Establish a serial communication interface with the Arduino board (e.g., via USB connection).

**Operation:**
- Send the predefined code "asdfg" through the serial interface to trigger OTP generation and activate the lock mechanism.
- Upon receiving the OTP, the system generates a random OTP combining alphabets and numbers.
- Input the generated OTP through the serial interface.
- If the input matches the generated OTP, the system unlocks and activates the servo motor to open the lock, accompanied by LED indicators.
- If the input OTP does not match, the system resets, and the user can try again.

**Code Structure:**
- Global Variables:
    - Declaration of variables for OTP generation and storage.
  
- Setup Function:
    - Initialization of serial communication and pin modes.

- Loop Function:
  - Main loop for continuous operation.
  - Waits for input from the serial interface triggering OTP generation.
  - Calls functions to generate OTP and verify the input OTP.

- OTP Generation Function:
  - Generates a random OTP combining predefined alphabets and numbers.

- OTP Verification Function:
  - Verifies the input OTP against the generated OTP.
  - Controls servo motor and LED indicators based on verification result.

**Notes:**
- Ensure the hardware connections are correctly set up according to the provided pin configurations.
- Customize the code as needed for specific applications or additional functionalities.
- Exercise caution when interfacing with physical components such as servo motors.
