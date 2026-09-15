# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
module exp5(clk,clear,si,so);
input clk,si,clear;
output so;
reg so;
reg [3:0] tmp;
always @(posedge clk )
begin
if (clear)
tmp <= 4'b0000;
else
tmp <= tmp << 1;
tmp[0] <= si;
so = tmp[3];
end
endmodule
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming.
```
Developed by:yugeshwartann S 
RegisterNumber: 212225040502

*/
```
**RTL LOGIC FOR SISO Shift Register**

<img width="1917" height="1078" alt="646262378-61be2daf-446f-4431-abec-2fb50556a70c" src="https://github.com/user-attachments/assets/314ecfe2-6053-4e68-9f35-4f48e648d09b" />

**TIMING DIGRAMS FOR SISO Shift Register**
<img width="1022" height="515" alt="646948741-1dc799af-5039-4ff0-8d69-3782271b0e41" src="https://github.com/user-attachments/assets/fc451b19-1b05-444d-9a2f-d5197d7edd31" />
