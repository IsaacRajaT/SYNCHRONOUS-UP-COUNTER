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

Open Quartus Prime software.

Create a new project and include a Verilog file for the counters.

Write the Verilog code for both counters.

Compile the project to check for errors.

Simulate the design to observe the waveform outputs.

Compare the outputs against the truth table to verify functionality.

Generate the RTL schematics and timing diagrams.

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:T Isaac Raja 

RegisterNumber:24900178
*/

![image](https://github.com/user-attachments/assets/a8cc5c79-b102-4140-b89e-0941587dd9ed)


**RTL LOGIC UP COUNTER**

![image](https://github.com/user-attachments/assets/8bd05e40-b04b-4c5c-8103-75ab8916c0dd)


**TIMING DIAGRAM FOR IP COUNTER**

![image](https://github.com/user-attachments/assets/b56aa44e-a8e3-4598-aa5f-ba049747dbde)


**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/93c7002c-1171-4a0c-aecf-2f856cdfa0a5)


**RESULTS**
Both the 4-bit ripple counter and the 4-bit synchronous up counter were successfully implemented in Verilog, and their functionality was validated using simulation results
