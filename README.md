## Adafruit TMC2209 Stepper Motor Driver Breakout Board PCB

<a href="http://www.adafruit.com/products/6121"><img src="assets/6120.jpg?raw=true" width="500px"><br/>
Click here to purchase one from the Adafruit shop</a>

PCB files for the Adafruit TMC2209 Stepper Motor Driver Breakout Board. 

Format is EagleCAD schematic and board layout
* https://www.adafruit.com/product/6121

### Description

Stepper motors are used for CNC machines, 3D printers, and whenever else one needs precise, powerful motion. But to get good behavior from steppers you need a motor driver chip that can provide high bursts of current, and for smooth motion, be able to PWM that current for microstepping support. You can DIY this with a lot of timers, a microcontroller and an  H-Bridge chip - or you could take the easy way out and use an Adafruit TMC2209 Stepper Motor Driver Breakout Board which makes controlling stepper motors easy-breezy and super-silent. 

All you need is two output pins, no timers, PWM or real-time microcontroller. Set the DIRection pin high or low to set the spin orientation. Then toggle the STEP pin to take one microstep at a time. You can set whether you want to go faster with 1/8 microsteps, or increase the precision to 1/16, 1/32 or 1/64 microsteps per STEP toggle. If you want more control, say to single-step or up to 1/256 microsteps, you can do so via the UART interface (more on that later). By default the driver is set to 1/8 microstep mode, you can change it by tying the MS1/MS2 pins high, either with jumpers or with 2 more output pins. The step/microstep mode can even be adjusted on the fly! LEDs on the DIR and STEP pins let you get visual feedback of your motor signal.

The Trinamic drivers are often known as "silent" or "stealth" chips - compared to the A4988 they are unbelievably quiet, you can barely tell they are running thanks to the microstepping techniques used. This reduces noise and wear, to make users happy. There's also a lot of niceties like index output which will pulse when the microstepping counter cycles back to 'zero', and a diagnostic output to quickly alert the microcontroller of a big error like short or open circuits. It can also do 'sensor-less stop detection' with a feature called StallGuard - but for that you will need to use the UART interface.

The UART interface is a single-pin serial port with auto-baud detection that allows more precise communication, diagnostics and control. You can do things like set microsteps from 1 to 256, or set the speed with a single command. You can also configure settings like current limiting, over-heat temperature limit, PWM frequency, etc. You'll need a microcontroller library to use UART and it's an 'extra' - not essential for basic motion control! 

The Trinamic TMC2209 is a popular driver chip, with small breakout boards used in many 3D printers. Those breakouts are great for plugging into motherboards, but are a little tough to use for prototyping. Our version comes with terminal blocks for the motor power and stepper wires, plus nicely labeled pins for control and mounting holes.

We fabricated the board with 2 oz copper to give it a hand with the 2A-max current that this driver can handle. To use the current limiting capability, twist the onboard potentiometer: when all the way to the right we can get to up to 2A max. Note that the higher the currents will heat up both the motor driver and stepper so you may need to add heatsinking to the chip. We don't include a heatsink but you can get a tall ~80ºC/W or short ~90ºC/W heatsink to attach on top.

Features:

* Trinamic TMC2209 silent "Stealth Chopper" DMOS microstepping driver with translator and overcurrent protection
* Motor voltage from 5V to 29VDC
* Vdd/Logic voltage from 3V to 5V, use with anything from an Arduino-compatible or ESP32 to Raspberry Pi other Single Board Computer
* Terminal screw block connections for easy VMotor power and 4-wire bi-polar stepper motor connection with 26-20AWG slots, 2.54mm / 0.1" spacing
* Control steppers using only two pins: DIRection and STEP
* Defaults to 1/8 microstep mode, change by pulling MS1/MS2 high (see TMC2209 datasheet for pin configuration) or via UART
* Red and Green LEDs on DIR signal to let you know forward or backward motion
* Yellow LED on STEP to let you know that motor driver is being moved
* Enable control line for low power / deactivation
* Index output will toggle when passing through the 'zero point' of the microsteps
* Diagnostic output will trigger on errors like shorted output or with "stall detection" (which requires UART configuration)
* Potentiometer to set current limiting, up to 2A
* 22uF 35V electrolytic capacitor on motor power
* 2 Oz copper for better current carrying and heatsinking
* Four mounting holes

Comes as one assembled and tested breakout plus a small strip of header. You'll need to do some light soldering to attach the header onto the breakout PCB. Microcontroller, motors, and power supply not included. You will need some sort of driver board that will toggle the DIR/STEP pins for you.

### License

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from [Adafruit](https://www.adafruit.com)!

Designed by Limor Fried/Ladyada for Adafruit Industries.

Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution. 
See license.txt for additional details.
