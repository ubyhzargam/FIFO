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



This is technology mapped netlist done using yosys and 45 nm cmos pdk.
This mapping is too long, I will upload it in bits and pieces of images - 
<br>
<img width="1470" alt="Screenshot 2024-11-19 at 1 38 20 AM" src="https://github.com/user-attachments/assets/6096b890-f998-438f-b70d-39bd00a2091b">

<br>

The overall image looks like this - 
<br>

<img width="56" alt="Screenshot 2024-11-17 at 1 15 20 AM" src="https://github.com/user-attachments/assets/bcd754ef-9b81-469f-9b9e-873f1b503993">
<br>

To analyse this it will be easier if I add dot file, I will upload it in the above with .dot extension, please download it and analyse if you want to.
<br>
<br>

Using stat -liberty command we can also get or estimate the area of the chip - <br>
<img width="491" alt="Screenshot 2024-11-17 at 1 27 45 AM" src="https://github.com/user-attachments/assets/f45d2fbd-1386-4e99-bf0e-0532e48a6811">
<br>
<br>

We can also perform logic optimiztion using yosys by running the following commands on terminal - <br>
opt <br>
share -aggressive <br>
After running these commands , the generic netlist which was different above looks like this after optimisation - <br>
<img width="1470" alt="Screenshot 2024-11-17 at 1 32 37 AM" src="https://github.com/user-attachments/assets/add299c1-8c41-4c27-9291-79cda60d3d8b">





