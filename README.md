this font with 10 caracters best for show the gauge in color lcd .
Download the last vertion of Library 
https://github.com/telamon/utft 
copy font_gauge_144x96_v05.c in library utft folder
in your project insert this code
extern uint8_t font_gauge_144x96_v05[];
ofther config your lcd
----------------------------
----------------------------
to active font use this code

myGLCD.setFont(SmallFont);

To use this font, the information must be converted to numbers between 0 and 9

Like the code below :

const int light_pin = A10;

int sensorValue = analogRead(light_pin);

Light_data = map(sensorValue, 0, 1023, 0, 9);

myGLCD.setColor(255, 255, 255);

myGLCD.print(String(Light_data), CENTER, 10);
