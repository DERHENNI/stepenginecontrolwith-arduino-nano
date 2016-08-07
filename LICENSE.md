#include <Stepper.h>

int SPMU = 32;

Stepper M1(SPMU, 2,3,4,5);
Stepper M2(SPMU, 6,7,8,9);
 

void setup()

{

M1.setSpeed(500);
M2.setSpeed(500);

}

 

void loop() {

M1.step(2048);
M2.step(2048);

delay(500);

M1.step(-2048);
M2.step(-2048);

delay(500);

}
