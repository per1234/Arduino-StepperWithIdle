# Arduino-StepperWithIdle
Update to the stepper library that includes the method idle() to power down the stepper motor.

I've added the method idle() to the stepper library (library source attached to this message). This method powers down the stepper motor for power saving or allow it to be freely rotated manually.

sample code:  
#include <StepperWidle.h>

StepperWidle myStepper(2048, 5, 3, 4, 2);
myStepper.setSpeed(15);
myStepper.step(50);

myStepper.idle();   /Power down stepper
delay(5000);

myStepper.step(50); /step another 50 steps
