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

/* write all the steps invloved */
1. Open Quartus Prime and create a New Project using the New Project Wizard.


2. Create a Verilog/VHDL file and write the synchronous up–down counter code.


3. Assign clock, reset, and up/down control inputs in the code.


4. Set the file as Top-Level Entity and compile the design.


5. Simulate using ModelSim to verify counting in up and down modes.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
```
UP COUNTER
module up(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule

DOWN COUNTER
module down(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule
```

Developed by: JESSIE J

RegisterNumber: 25017372
*/

**RTL LOGIC UP COUNTER**
     <img width="1920" height="1080" alt="Screenshot 2025-12-15 135523" src="https://github.com/user-attachments/assets/e17e9b22-27b7-4a0c-8e59-9799d56366ea" />
     <img width="1920" height="1080" alt="Screenshot 2025-12-15 140421" src="https://github.com/user-attachments/assets/223844b1-aebf-4898-a418-7350ab1dd9a9" />

**TIMING DIAGRAM FOR IP COUNTER**
     <img width="1920" height="1080" alt="Screenshot 2025-12-15 135714" src="https://github.com/user-attachments/assets/0540148b-58ec-4ce7-8945-6afd715e0c5c" />
     <img width="1920" height="1080" alt="Screenshot 2025-12-15 140706" src="https://github.com/user-attachments/assets/ba961dd2-86ef-44be-ac97-6556e64223df" />



**RESULTS**

   Thus,To implement 4 bit synchronous up counter and validate functionality is verified.
