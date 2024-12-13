### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**
1.Type the program in Quartus software
2.Compile and run the program
3.Generate the RTL schematic and save the logic diagram
4.create nodes for inputs and outputs to generate the timing diagram
5. generate the timing diagram



/* write all the steps invloved */

**PROGRAM**
module counter(clk,rst,q);
input clk,rst;
output[3:0]q;
reg[3:0]q;
always@(posedge clk)
if(~rst==0)
    q<=3'b0;
else
    q<=q+1'b1;
endmodule 

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:praveena d RegisterNumber:24003392
*/

**RTL LOGIC UP COUNTER**
![image](https://github.com/user-attachments/assets/466fff20-0d75-4f2c-935b-3e6e23471c41)


**TIMING DIAGRAM FOR IP COUNTER**

![image](https://github.com/user-attachments/assets/b065874d-925e-4eab-bac4-6613cf37de5a)


**TRUTH TABLE**
![image](https://github.com/user-attachments/assets/619934bb-b104-4257-a679-9c0934f2a26a)



**RESULTS**
Thus the implementation of 4 bit synchronous up counter and validate functionality is successfull
