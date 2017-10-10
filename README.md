1. avr-gcc -g -Os -Wall -mcall-prologues -mmcu=atmega328p -fno-exceptions -o main.obj main.c
2. avr-objcopy -R .eeprom -O ihex main.obj main.hex
3. avrdude -b 19200 -c usbtiny -p m328p -U flash:w:main.hex para gravar no atmega
