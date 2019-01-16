# stm32f4-bare-metal

Bare metal STM32F4 projects. CMSIS is added for a a general support.
Some of the STM32F4xx family based processor headers are added in the `include` folder.

## Installation

* Clone the project using `git clone --recurse-submodules https://github.com/fcayci/stm32f4-bare-metal`
with the added CMSIS repo.

* Install a compiler. You can get one free from [GNU ARM Embedded Toolchain](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads)
* Install programmer from [stlink](https://github.com/texane/stlink)
* Install the make utility for Windows only from [MinGW and MSYS](http://www.mingw.org/)
* Add these to your `PATH`

## Usage

Browse into any directory from terminal and run `make`.
```
cd blinky
make
```

If everything is setup correctly, you should see the completed message.
```
Cleaning blinky
Building blinky.c
   text    data     bss     dec     hex filename
    374       0       0     374     176 blinky.elf
Successfully finished...
```

## Program

Run `make burn` from the project directory after `make`
```
...
.. Flash written and verified! jolly good!
```

## Projects

* [blinky](blinky/) - Good old blink LEDs example
* [math](math/) - A simple sine function to test math library operation
* [systick](systick/) - Blinks LEDs using systick timer. Processor clock is set to max (168 Mhz)
* [pwm](pwm/) - Fades an LED using pwm functionality using Timer module