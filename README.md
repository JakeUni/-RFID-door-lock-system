# -RFID-door-lock-system
Developed with Tom Lancaster (TinkerTavern)

A Prototype for a high-security RFID door lock system that would be used in an area 
where multi factor authentication is necessary. 

The program involves 2 Arduinos, a primary and a secondary. The primary runs all the hardware components, including an RFID 
scanner, 2 buttons, a piezo speaker, a screen and a servo (to represent the door lock mechanism). The 
secondary Arduino controls the security represented as a bubble machine, and does all the verification. 
They’re both connected through Bluetooth serial, using HC-05 modules.
Once a face is detected, a timer is started, and the Arduino prompts the user to scan an RFID card. If 
correct they are then asked to input an answer to the question “What is the answer to the universe?” 
in binary, if correct again a door will open, this is displayed as a servo. If they scan 3 wrong RFID cards, 
input the answer to the question wrong 3 times, or run out of time then an alarm is sounded, and the 
bubble machine turns on. We needed communication in this project because one Arduino is designed 
for validation of information and one is designed for the input of information. 
