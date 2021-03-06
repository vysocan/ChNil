#### ChNil - ChibiOS/Nil Arduino Library

This is the initial release of a much improved version of ChibiOS/Nil.
I am starting a new repository since this version is not backward
compatible with the NilRTOS library.

https://github.com/greiman/NilRTOS-Arduino

I have done some testing with an Uno and a little with a Mega but
more bugs are likely since I needed to modify core parts of the RTOS.

ChNil is a tiny RTOS library for AVR Arduino boards.

The base code for ChNil was written by Giovanni Di Sirio, the author
of ChibiOS/Nil and ChibiOS/RT.

http://www.chibios.org/dokuwiki/doku.php

The code is version 2.0.0 from a recent, Jan 2017, trunk version of ChibiOS.
The API is considerably different than the original version of Nil.  It is
now very much like ChibiOS/RT.

If you are installing from GitHub repo zips, rename the folder ChNil
before copying it to your Arduino/libraries folder.

Please read ChNil.htlm for more information.  See the Examples section
of the html documentation.

Start with the ChNilBlink example which is traditional for almost every RTOS.

ChibiOS/Nil now has event flags, mailboxes, memory pools and other new features.
Try the examples that illustrate these features.

I have added chAnalogRead(), a version of analogRead() that sleeps while 
the AVR ADC is busy.

You can check stack use with chFillStacks(), chPrintStackSizes(), 
and chPrintUnusedStack().

chTimer1Start(), chTimer1Wait(), and chTimer1Stop() allow a thread to
run at microsecond intervals. See the ChNilSdLogger.ino for an example.

ChNilSerial is a very small unbuffered replacement for Arduino Serial.

The TwiMaster library, in the extras folder, is a I2C library that
sleeps while an I2C transfer takes place.
