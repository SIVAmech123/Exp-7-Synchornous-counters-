## Name:R.Sivakumar
## Reg: 23013501


## Exp-6-Synchornous-counters - up counter and down counter 
## AIM:
To implement 4 bit up and down counters and validate  functionality.
## HARDWARE REQUIRED:  
– PC, Cyclone II , USB flasher
## SOFTWARE REQUIRED:  
Quartus prime
## THEORY 

## UP COUNTER :
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



## DOWN COUNTER :

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
## Procedure:
/* write all the steps invloved */



## PROGRAM :
## up counter:
<img width="173" alt="Screenshot 2023-12-21 183833" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/05008d32-ab10-49e5-804b-be1fd96a2656">

## down counter:

<img width="215" alt="Screenshot 2023-12-21 183853" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/5f1b0b22-d446-465e-a751-d0a5e94819fc">




## RTL LOGIC UP COUNTER AND DOWN COUNTER  

## UP COUNTER:

<img width="468" alt="Screenshot 2023-12-21 183956" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/f40a6e40-ae01-475f-96e8-c616a5983425">

## DOWN COUNTER:

<img width="475" alt="Screenshot 2023-12-21 184012" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/3ee54001-5d8d-4672-968e-7ca7c3b49b28">



## TIMING DIGRAMS FOR COUNTER  

## UP COUNTER:

<img width="533" alt="Screenshot 2023-12-21 184040" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/e0f876c4-9a4c-4c56-808e-292700416659">

## DOWN COUNTER:

<img width="533" alt="Screenshot 2023-12-21 184134" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/16ef7887-070e-4a93-83a8-ade7ce1b905e">

## TRUTH TABLE 

## UP COUNTER:
<img width="398" alt="Screenshot 2023-12-21 185541" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/2eaad904-bbd7-4ee9-ab93-f0f9909bf801">


## DOWN COUNTER:

<img width="481" alt="Screenshot 2023-12-21 185607" src="https://github.com/SIVAmech123/Exp-7-Synchornous-counters-/assets/151629067/c5d92171-bbfa-4edf-bf3c-52303fd1274d">


### RESULTS 
By this we have verified the truth table of 4-bit up-counter using verilog.
