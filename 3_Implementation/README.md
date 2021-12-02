# Steps to build the code
1)Including required libraries.
2)Then in main function assign pinB1 as input to do this we have to set logic = 0.
3)To assign logic 0 in port B, we have to use DDRB (Data Direct Register) and to not disturb other pins we are using masking technique by assigning 1 to other pins by using DDRB=DDRB&0b11111101 command which is binary representation of HEX value which represents second bit as low and others as high.
4)To assign pinC6 as output to do this we have to set logic = 1.
5)To assign logic 1 in port C ,we have to use DDRC (Data Direct Register) and to not disturb other pins we are using masking technique by assigning 0 to other pins by using DDRC=DDRC|0b01000000 command which is binary representation of HEX value which represents sixth bit as high and others as low.
6)Then in while loop we have to continuosly monitor and compare value of pinB with given input and if switch is open the pinB will receive 0b00000010 input thus making the LED connected to port C high and glowing it.
7)if switch is closed the pinB will not receive any input thus LED connected to port C gets low and it will not glow.
