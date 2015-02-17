MEEPROMMER
==========

(E)EPROM programmer based on Arduino hardware


The MEEPROMMER is a combination of hardware and software that lets you read and write 
data from (and to) 28Cxxx EEPROMS. Maybe later there will be enhancements to use it
also for 27Cxxx EPROMS. 

At the moment we have an working prototype on a PCB that uses an Arduino Nano and an 
Arduino-shield that can directly plugged to an Arduino Uno. 

The Arduino firmware provides a serial interface with simple commands to transfer data 
between a host computer and an eeprom.

Uses a simple python3 script to read/write to the EEPROM

Example syntax :
----

    Meepromer Command Line Interface

    optional arguments:
      -h, --help            show this help message and exit
      -V, --version         Request and display device version
      -w, --write           Write to EEPROM
      -W, --write_paged     Fast paged write to EEPROM
      -r, --read            Read from EEPROM as ascii
      -d, --dump            Dump EEPROM to binary file
      -v, --verify          Compare EEPROM with file
      -u, --unlock          Unlock EEPROM
      -l, --list            List serial ports
      -a ADDRESS, --address ADDRESS
          Starting eeprom address (as hex), default 0
      -o OFFSET, --offset OFFSET
          Input file offset (as hex), default 0
      -b BYTES, --bytes BYTES
          Number of kBytes to r/w, default 8
      -p PAGE_SIZE, --page_size PAGE_SIZE
          Number of bytes per EEPROM page e.g.:CAT28C*=32,
          AT28C*=64, X28C*=64, default 32
      -f FILE, --file FILE  Name of data file
      -c COM, --com COM     Com/tty port address
      -s SPEED, --speed SPEED
          com port baud, default 115200
