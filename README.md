Keylogger using Python and pynput
Overview
This project is a simple keylogger built using Python and the pynput library. It listens for keyboard events and logs each key press to a text file. The program demonstrates how to monitor keyboard input in real time and handle both character keys and special keys.
Features
 Captures all key presses, including letters, numbers, symbols, and special keys.
 Logs keystrokes to a file named key_log.txt.
  Uses exception handling to differentiate between printable characters and special keys.
 Runs continuously until manually stopped.
Requirements
 Python 3.x
 pynput library
To install pynput, run:
pip install pynput
How It Works
 The script defines a function on_press that is triggered whenever a key is pressed.
 If the key has a printable character (key.char), it is written directly to the log file.
 If the key is a special key (like Enter, Shift, Ctrl), it is logged in square brackets using its string representation.
 A keyboard.Listener is started to monitor key presses and call on_press.
 The listener runs in the foreground and blocks further execution with listener.join().
Usage
To run the keylogger:
python keylogger.py
The program will start logging keystrokes to key_log.txt in the same directory.
