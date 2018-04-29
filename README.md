# Arduino-StepperWithIdle
Update to the stepper library that includes the method idle() to power down the stepper motor.

I've added the method idle() to the stepper library (library source attached to this message). This method powers down the stepper motor for power saving or allow it to be freely rotated manually.

This library allows you to control unipolar or bipolar stepper motors. To use it you will need a stepper motor, and the appropriate hardware to control it.

sample code:  
#include <StepperWidle.h>

StepperWidle myStepper(2048, 5, 3, 4, 2);
myStepper.setSpeed(15);
myStepper.step(50);

myStepper.idle();   //Power down stepper
delay(5000);

myStepper.step(50); //step another 50 steps


== License ==

Copyright (c) Arduino LLC. All right reserved.
Copyright (c) Sebastian Gassner. All right reserved.
Copyright (c) Noah Shibley. All right reserved.

This library is free software; you can redistribute it and/or
modify it under the terms of the GNU Lesser General Public
License as published by the Free Software Foundation; either
version 2.1 of the License, or (at your option) any later version.

This library is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
Lesser General Public License for more details.

You should have received a copy of the GNU Lesser General Public
License along with this library; if not, write to the Free Software
Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301 USA
