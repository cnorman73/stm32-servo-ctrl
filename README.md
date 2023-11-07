# stm32-servo-ctrl readme

This code runs on an Nucleo F446RE

The code does several things:
- listens on serial port 2 for commands from a serial terminal running on a seperate computer
- based on commands, PWM will be set on servo motor control line
- toggles an LED immediately after turning on the PWM.

For serial port commands, I use Putty and a DTech USB to Serial cable. The Green and White lines are plugged into the RX/TX pins on the Nucleo board. The port /dev/ttyACM0 on Linux appears when the STM32 board is switched on and the DTech cable is fully connected. Use this with putty and a serial port speed of 115200.

Make sure the grounds are tied together on the power supply and nucleo board and try not to create ground loops by having too much resistance on the ground lines.
