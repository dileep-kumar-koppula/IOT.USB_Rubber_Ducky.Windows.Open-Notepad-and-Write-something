# Notepad Automation with DigiKeyboard

This Arduino sketch is designed to open Notepad and write a message. It uses the DigiKeyboard library for simulating keyboard inputs.

## Code

```cpp
// This is for Educational purpose only

#include "DigiKeyboard.h"

void setup() {
  DigiKeyboard.sendKeyStroke(0); // Focus on the desktop
  DigiKeyboard.delay(1000);
  DigiKeyboard.sendKeyStroke(KEY_R, MOD_GUI_LEFT); // Open Run dialog
  DigiKeyboard.delay(2000);
  DigiKeyboard.println("notepad.exe"); // Type "notepad.exe" to open Notepad
  DigiKeyboard.delay(5000);
  DigiKeyboard.sendKeyStroke(KEY_ENTER); // Press Enter to open Notepad
  DigiKeyboard.delay(1000);
  DigiKeyboard.println("Hello, This is a BIA - Cyber Security & Ethical Hacking"); // Write a message
  
  // Turn ON LED when code execution finishes
  digitalWrite(1, HIGH); // Turn on the LED
}

void loop() {
  // No loop needed
}
