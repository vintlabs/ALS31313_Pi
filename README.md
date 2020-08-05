# ALS31313_Pi
## Read an ALS31313 3D Hall Effect Sensor - Designed for Raspberry Pi but should function fine for other SBCs

Reference: [ALS31313 Datasheet](https://www.allegromicro.com/~/media/Files/Datasheets/ALS31313-Datasheet.ashx)

### Usage Example:
```
$ ./als31313 -a 0x60 -b 1 -d 200
```

### Options:
**-a** *address* (example: -a 0x65)

**-b** *bus* (Example, for /dev/i2c-1 use -b 1)

**-d** *delay* in ms (Example, to display temperature to STDOUT every 200 ms use -d 200) To display once and exit omit or set to 0.

**-f** *filter* value. Set the ALS31313's internal filter from 0 (none) to 7 (max)

**-r** *resolution*  Set the ADC resolution. 0-3, where 0 is 18bit, and 3 is 12bit)

**-q** Suppress normal output, read temperature and exit returning the temperature (as integer)

### Dependencies/Prerequisites
```
$ sudo -i
$ apt update
$ apt install git build-essential cmake
```

### Compiling
```
$ git clone https://github.com/vintlabs/ALS31313_Pi.git
$ cd ALS31313_Pi
$ mkdir build && cd build
$ cmake ..
$ make
```
