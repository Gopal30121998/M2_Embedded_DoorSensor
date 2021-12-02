# Introduction
## Door Sensor ussing ATmega328p.

Door Sensor acts as a security and indication system.It is avilable in the market in two piece form.One piece attaches on the door frame, and the other attaches parallel to the first piece on the door itself. The two parts create a closed circuit when the door is shut. As the door opens, the magnet and switch separate, breaking the circuit. When the circuit breaks, the sensor signals the central control panel and switch on the LED.

## Research:-
Door Sensor is a mini project which uses microcontroller ATmega328 and work as a indication system. 
 
## SWOT ANALYSIS:-
 -  a) Strengths:- User friendly gadget , easy to understand and implementation.
 -  b) Weaknesses:- Implementation of existing system.
 -  c) Opportunities:-Can be used with other indicators also such as speaker. 
 ## 4W's and 1'H :-
 ## Who:- 
   This tool is a helping hand for the people who have security concerns.
 ## Where:-
   Can be used at home,banks,hostels,organisations to keep a track on unknown entries.
 ## When:-
   Can be used to protect precious things.
 ## Why:-
   Designed for security systems.
 ## How:-
   By using C programming and SimulIDE.
## Detail requirements :-
## High Level Requirements:-
- a)A Door Sensor is connected to bit 1 of Port B.
- b)LED is connected to bit 6 of port C.
- c)LED should be turn ON without changing the state of other pins.
## Low Level Requirements :-
- a)When switch is closed pin B will get 5V and LED will glow.
- b)When switch is open pin B will get 0V and LED will not glow.

# Structural Diagram
![structural](https://user-images.githubusercontent.com/94282308/144406567-ad865cdd-b49e-4fa3-a77c-ca4665046649.png)
# Behavioural Diagrams
![behevioural](https://user-images.githubusercontent.com/94282308/144406537-3505afb8-a26c-49a0-94e3-8ddeee70d9a2.png)
# Simulations
![simulation](https://user-images.githubusercontent.com/94282308/144406564-cfa339c7-d777-47e0-b35d-6cf9c285f6de.png)
# Bill of Materils
![bill of materials](https://user-images.githubusercontent.com/94282308/144406559-f6f68e12-0d6a-4b34-81de-68a656d9ed34.png)

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

# Test Plan


| TEST_ID | Description | Expected Output | Actual Output | PASS/FAIL | 
| ----- | --------------| --------------- | --------------|-----------|
| T01 | To Check whether pinB is assigned as input or not | SUCCESS | SUCCESS | PASS |
| T02 | To Check whether pinC is assigned as input or not | SUCCESS | SUCCESS| PASS |
| T03 | To Check whether given input to pin B1 is high or low | SUCCESS | SUCCESS | PASS |
| T04 | To Check whether output is being generated through pin C6 or bot | SUCCESS | SUCCESS | PASS |
| T05 | To Check whether LED is glowing or not | SUCCESS | SUCCESS | PASS |
