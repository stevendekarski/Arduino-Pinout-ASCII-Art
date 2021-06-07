# Arduino Pinout ASCII Art

When coding Arduino projects for other people (and myself) I find having ASCII art pinouts of the hardware very helpful. It allows me to  very quickly see the pin assignments and pins used.

Please feel free to copy, update and add to and use where you see fit.

I use the “Wiring diagram:” to link the sensor hardware to the Arduino pin. For the pin used, place an asterisk between the brackets like so ```[*]```.  I find using a header definitely helps keep track of the details.

**This is a list of the ASCII art:**

- [Adafruit Feather HUZZAH ESP8266](https://github.com/stevendekarski/Arduino-ASCII-Art/blob/main/Adafruit-Feather-HUZZAH-ESP8266.txt)
- Arduino Mega 2560 R3
- Arduino Nano 33 BLE Sense
- Arduino Pro Mini 168
- Arduino Pro Mini 328P
- Arduino UNO R3
- Wemos D1 mini ESP8266
- Wemos D1 mini Pro ESP8266
- ESP-32 CAM

## Example:
```cpp
/*
  Project Name: The Most Amazing Arduino Project In The World
  Hardware:     Pro Mini Atmega168 3.3v 8MHz,
  Created:      2021/01/01
  Modified:     2021/01/01
  Language:     C++/Arduino
  Version:      12.3.1
  Author/s:     Miss Smith, Mr Smith
  Licensing:    Please see licensing.md doc file/Proprietary/CC-BY cite

  Notes:        


  Pro Mini Atmega168 3.3v 8MHz

           VCC -------+  +------- RDX/0         
           GRD ----+  |  |  +---- TXD/1
           GRD -+  |  |  |  |  +- DTR
                |  |  |  |  |  |
             +-[ ][ ][ ][ ][ ][ ]-+
             |                    |    
       TXD/1 | [ ]            [ ] | RAW/3V3 to 12V in
       RXD/0 | [ ]            [ ] | GRD
         RST | [ ]  Atmega168 [ ] | RST
         GRD | [ ]     /\     [ ] | VCC/3V3
      INT0/2 | [ ]    /  \    [ ] | 17/A3/ACD3
  PWM/INT1/3 | [ ]    \  /    [ ] | 16/A2/ACD2
           4 | [ ]     \/     [ ] | 15/A1/ACD1
           5 | [ ]            [ ] | 14/A0/ACD0
           6 | [ ]  [8.0MHz]  [*] | 13/SCK/LED
           7 | [ ]       [LED][ ] | 12/MISO
           8 | [ ]   [REST]   [ ] | 11/MOSI/PWM
           9 | [ ][ ][ ][ ][ ][ ] | 10/SS/PWM
             +--------------------+
                   |  |  |  | 
   19/SDA/A4/ADC4 -+  |  |  +- A7
   18/SCL/A5/ADC5 ----+  +---- A6
         
  Pin Function/IDE Pin Number, * = Pin is being used.

  Wiring diagram:

  LED_BUILTIN  -->  13/SCK/LED

*/

// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
```
