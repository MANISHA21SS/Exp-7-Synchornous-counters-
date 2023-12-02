# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: MANISHA SELVAKUMARI S S
RegisterNumber: 23012275 
*/
Code:
Upcounter:
![upcounter code](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/07cfb6fe-2ec4-4608-aaf3-9cd790e7a372)
Downcounter:
![downcounter code](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/2165da3a-7393-4414-9985-046aab3bfb85)

### RTL LOGIC UP COUNTER AND DOWN COUNTER  
Upcounter:
![upcounter rtl](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/37c6cea4-1fa8-438b-8938-f1dc407feeeb)
Downcounter:
![downcounter rtl](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/26ee5c2d-62cd-45ad-9c29-ce5e3c7307d0)

### TIMING DIGRAMS FOR COUNTER  
Upcounter:
![upcounter timing diagram](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/4728c8f1-8fc2-4884-b11b-33624097ca4c)
Downcounter:
![downcounter timing diagram (2)](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/c863f4e0-51ca-4c1b-b9c9-371911debd84)

### TRUTH TABLE
Upcounter:
![upcounter truth table](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/d22e96d4-4504-4b46-96e1-4d9a0e2906a6)
Downcounter:
![downcounter truthtable](https://github.com/MANISHA21SS/Exp-7-Synchornous-counters-/assets/147474298/83ba6588-44db-4b46-a434-8dae355d5166)

### RESULTS 
To implement 4 bit up and down counters and validate functionality is executed successfully.
