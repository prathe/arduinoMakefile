# This fork is a port for Mac OSX and Arduino 1.0

It should works out of the box if you are using the UNO. Just edit your sketch filename in the Makefile and type `make` to compile and upload your sketch.

## Install

* Download the [IDE for Mac OSX](http://arduino.cc/en/Main/Software)
* Add the following dir to your PATH environment variable

        /Applications/Arduino.app/Contents/Resources/Java/hardware/tools/avr/bin

* Copy the avrdude.conf file to /usr/local/etc

        $ cp /Applications/Arduino.app/Contents/Resources/Java/hardware/tools/avr/etc/avrdude.conf /usr/local/etc

## Usage

Compile only

    $ make compile

Compile and upload

    $ make

Reset

    $ make reset

# arduinoMakefile

This project is just a simple Makefile for Arduino. There are some Makefiles in the Web but all of them are complicated and some does not work properly for newer versions of Arduino. This Makefile is simple and just works!

It does:

- Compiles your sketch, including the standard Arduino library required
- Merge all files into a .elf and them translate it to a .hex file
- Upload the .hex to Arduino's flash memory


**WARNING[0]:** it was tested only in Ubuntu GNU/Linux with Arduino Uno. Probably it'll work well in any GNU/Linux distribution or Mac OS with Arduino Duemilanove. Windows users: sorry, please use a better OS.

**WARNING[1]:** by now the feature of compiling external libraries (even standard libraries and third-party libraries) is not implemented. So, if you have some `#include` in your project, probably it won't work -- but don't be afraid, I'm working on this.


## Why another Makefile?

The question was answered in the section above -- but I'm studying all the Makefiles for Arduino that I found in the Web and trying to implement the simplest way of doing it right. I've created a [**comprehensive list of Makefiles**](https://github.com/turicas/arduinoMakefile/blob/master/resources.markdown) and I'm categorizing them.
