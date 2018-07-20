# SoftwareSerialFix
This is a modification of the SoftwareSerial library for Arduino to create software serial ports and still allow for software interrupt pins. The original library is included with the Arduino IDE
Different ports in SoftwareSerialFix.cpp on lines 227 to 253 can be commented or uncommented to adjust where the serial ports and interrupt pins are. For the SoftwareSerial file, the ports correspond to the Arduino pins as follows: 
PCint0_vect is Port B or digital pins 8 to 13
PCint1_vect is Port C or analog pins 0 to 5
PCint2_vect is Port D or digital pins 0 to 7
Each port that is left in the SoftwareSerialFix.cpp file, a line of the form #define NO_PORTX_PINCHANGES where X is replaced with the port letter as listed above must be put before the library inclusions in the Arduino code. The pin change interrupt library  that works with this code can be found at https://github.com/GreyGnome/PinChangeInt.
