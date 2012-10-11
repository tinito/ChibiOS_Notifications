Chibios C++ notifications framework
===================================

A C++ templated class for creating and passing messages between processes.

Features
-----

* Many clients (Listeners) can listen to each server (Notifier)
* Each client brings its own statically allocated memory
* A client can take as long as it wants to handle its received data without impeeding other clients
* Messages are passed via the Chibios Mailbox API
* Clients can listen to more sources (up to the size of ChibiOS Event mask)

Demo
----

A demo for the STM32F4 Discovery is included. It has a sample message LEDData that specifies the LED states.
One notifier specifies the states of LED3 and LED4, another specifies the states of LED5 and LED6.
Two listeners turn on and off the respective LEDs.
Another listener prints this information over serial, receiving messages from both notifiers.
