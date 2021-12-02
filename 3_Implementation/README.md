# Steps to build the code
- Including required libraries.
- Then in main function assign pinB1 as input to do this we have to set logic = 0.
- To assign logic 0 in port B, we have to use DDRB (Data Direct Register) and to not disturb other pins we are using masking technique by assigning 1 to other pins by using -DDRB=DDRB&0b11111101 command which is binary representation of HEX value which represents second bit as low and others as high.
- To assign pinC6 as output to do this we have to set logic = 1.
- To assign logic 1 in port C ,we have to use DDRC (Data Direct Register) and to not disturb other pins we are using masking technique by assigning 0 to other pins by using DDRC=DDRC|0b01000000 command which is binary representation of HEX value which represents sixth bit as high and others as low.
- Then in while loop we have to continuosly monitor and compare value of pinB with given input and if switch is open the pinB will receive 0b00000010 input thus making the LED connected to port C high and glowing it.
- if switch is closed the pinB will not receive any input thus LED connected to port C gets low and it will not glow.
# Steps to run the simulation and Steps to verify the working of code.
- After wrinting the code in any interpreter in any language we have to compile that code file.
- After compiling code we have to generate and burn that file to a HEX file as microcontroller only understands values in 1 and 0.
- Then designing our circuit in an simulator and load that HEX file into our microcontroller and check/compare the generated output with expected one.
# Schematic circuits
![simulation](https://user-images.githubusercontent.com/94282308/144425091-7160dbec-ff50-4ff4-8e49-d45a3459d7e1.png)
