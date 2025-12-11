

**AIM:**

To implement down counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**
~~~
1.A down counter is a sequential circuit that decreases its count value by one on every clock pulse.
2.It consists of a series of flip-flops connected in such a way that the output represents a binary count in descending order.
3.In a down counter, the most significant bit changes only when all lower bits have reached their minimum state.
4.On every clock pulse, the output of the flip-flops updates to form the next lower binary value.
5.The counting sequence continues downward (like 7, 6, 5…0 in a 3-bit counter) and then rolls over to the maximum value again.
6.The behavior of the counter depends on how the flip-flops are triggered—either synchronously or asynchronously.
7.In a synchronous down counter, all flip-flops receive the clock signal at the same time, ensuring proper timing.
8.Down counters are used in timers, frequency dividers, event counting, and digital clocks.
9.Since the counting depends on clock pulses, the circuit operates as a synchronous sequential system.

~~~
**PROGRAM**
~~~
DOWN COUNTER
module ex12(out,clk,rst);
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
~~~
~~~

 Developed by:Manusiya R  RegisterNumber:25016729
~~~


**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="2560" height="1333" alt="ex12(1)" src="https://github.com/user-attachments/assets/0e223fef-c366-42e0-8203-3fd72f8f128f" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="2550" height="1343" alt="ex12(2)" src="https://github.com/user-attachments/assets/7d6c8d1b-49d8-460e-ad07-da3a167955db" />

**RESULTS**
The synchronous down counter was successfully designed, implemented, and its operation was verified.
The output was observed to count in a decreasing binary sequence on each clock pulse, confirming the correct working of the down counter circuit.
