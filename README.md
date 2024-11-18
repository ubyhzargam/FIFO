The above is the code for FIFO of depth 16. <br>

Now , let us perform logic senthesis on this RTL code. <br>
There are several steps in logic synthesis - <br>
1. RTL Synthesis : Converts RTL (verilog) code to Generic Netlist. This is further subdivided into Parsing + Elaboration + Translation and optimization <br>
2. Logic Optimization : Peforms logic Optimization on Generic Netlist to get Optimized netlist of generic gates.<br>
3. Technology mapping : The generic netlist is mapped to standard cells through a Process design kit(PDK) which contains information about standard cells <br>
4. Technology dependendent logic Optimization : We get optimized netlist mapped to a particular technology.<br>
<br>
<br>

   
This is the Internal model representation of Verilog code i.e. Syntax tree <br> 
This is performed using the commands - <br> 
read_verilog top.v<br> 
show <br> 

<img width="1468" alt="Screenshot 2024-11-17 at 12 46 07 AM" src="https://github.com/user-attachments/assets/6a23c46e-d157-4255-98fd-daedab8c00a2">

<br>
<br>

This is the generic gate netlist <br> 
<img width="1463" alt="Screenshot 2024-11-19 at 2 55 19 AM" src="https://github.com/user-attachments/assets/4c3ac7e4-c4c6-4310-8d5c-a739282bdebd">

<br>
<br>
This is the optimized generic gate netlist <br> 
<img width="1463" alt="Screenshot 2024-11-19 at 2 59 38 AM" src="https://github.com/user-attachments/assets/c6adcc75-6197-43a4-bd9d-1e65f94d63b4">

<br>
<br>


This is technology mapped netlist done using yosys and 45 nm cmos pdk.
<br>
<img width="1470" alt="Screenshot 2024-11-19 at 1 38 20 AM" src="https://github.com/user-attachments/assets/6096b890-f998-438f-b70d-39bd00a2091b">

<br>
<br>

This is the optimized technology mapped netlist <br> 
<img width="1463" alt="Screenshot 2024-11-19 at 2 56 08 AM" src="https://github.com/user-attachments/assets/bd9951ab-bcd1-4d1f-910a-0a17fcf6b2a6">

<br>

<br>
<br>

Using stat -liberty command we can also get or estimate the area of the chip - <br>
<img width="491" alt="Screenshot 2024-11-17 at 1 27 45 AM" src="https://github.com/user-attachments/assets/f45d2fbd-1386-4e99-bf0e-0532e48a6811">
<br>
<br>







