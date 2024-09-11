# FPGA-Architecture-and-Programming
# Contents
 <div class="toc">
  <ul>
    <li><a href="#header-1">Session-1</a></li>
    <ul>
    <li><a href="#header-1_1">Lecture 1-Video-Intro to VLSI Design Flow</a></li>
		<ul>
    </div>
  
<div class="toc">
  <ul>
    <li><a href="#header-2">Session-2</a></li>
	<ul>
        <li><a href="#header-2_1"> Lecture 2-Verilog HDL- Lexical Conventions</a></li>
		<ul>
       <li><a href="#header-2_1_1"> Lab1- of Modelsim Simulation</a></li>
		<ul></ul>
       <li><a href="#header-2_1_2">Lab2- Simulation using ICARUSFile</a></li>
		<ul></ul>
       <li><a href="#header-2_1_3">Lab3-Simulation using Xilinx VivadoFile</a></li>
		<ul></ul>
       <li><a href="#header-2_1_4">Lab 3A-EDA Playground </a></li>
		<ul></ul>
			
  </div>
  
  <div class="toc">
  <ul>
      <li><a href="#header-3">Session-3</a></li>
	<ul>
        <li><a href="#header-3_1"> Lecture 3-Verilog HDL - Design Abstractions</a></li>
		<ul>
	<li><a href="#header-3_2"> Lab Exercise- LE01 </a></li>
		<ul></ul>
   </div>
  
  <div class="toc">
  <ul>
      <li><a href="#header-3">Session-4</a></li>			
        <ul>




























# <h1 id="header-1">Session-1</h1>	 
## <h1 id="header-1_1">Lecture 1-Video-Intro to VLSI Design Flow</h1> 

**Design logic Implementation: Categories**:- 

![image](https://github.com/user-attachments/assets/cf88adb9-cdca-426a-8642-0a9f44234e83)


**Full Custom Design**:- All the logics, circuits and layouts are designed specifically for that particular ASIC(Application specific integrated ciruits)from the ground up. It requires high power consumption.

**Advantages**:- Delivers the highest possible performance at  the smallest possible die size.

**Disadvantages**:- High performance and small size comes at a price of increased design time, complex design and overall cost of the IC itself.

**Examples**:- Microprocessors, memories, sensors, transducers, Analog,digital communications.

**Semi-Custom Design : Gate Array**:- In gate array based ASIC's, p and n type transistor are predefined on a wafer as arrays. Based on the costumer requirements the base wafer is ptepared. Gate arrays are devided into two parts- Chnneled array and channeless gate array.

**Channeled array**:- Here the interconnections between the logic cell are performed within the predefined channels between the rows of the logic cells.

**Channel-less array**:- Here the connections are made on an upper metal layer on top of the logic cells.

![image](https://github.com/user-attachments/assets/6571866a-3f8f-4763-afbc-6dd650909753)

**Standard Cell based ASIC**:- A Standard Cell based ASIC uses predesigned logic cells like Gates, Multiplexers, Flip-flops, Adders etc. These logic cells are known as Standard Cells that are already designed and stored in a library. Standard Cell based designs are organized as rows of constant height cells on the chip, just like a row of bricks. When combined with logic-level components, standard cell-based designs can be used to implement complex functions like Multipliers and Memory Arrays. 

![image](https://github.com/user-attachments/assets/b5e08df0-7280-4ff8-8529-f91cb3bc4670)

**Comparison between Full Custom and Semi-Custom design**:-

![image](https://github.com/user-attachments/assets/35b23b1e-0bf8-49e1-8c2c-12e926677675)


**ASIC Design Flow**:- The following image shows a typical design flow involved in designing a semicustom ASIC.

![image](https://github.com/user-attachments/assets/f9c6faa7-fa3e-4ace-a503-13771cd2351e)

**specifications**:-
             Day by day the technology is increasing and customer also expecting new features(like low power consumption,high speed) in the device.In this stage the features information which is expecting from the customer is collected by some marketing people.

**Architecture design**:-
             The architecture team will design an architecture based on the specifications.The architecture is like a block diagram we can find the all the details which are using in the design(like processors,memories) and how the are connected.This architecture team will estimate the block area,how much power is required and cost for the design.

**RTL design**:-
            Register transfer level(RTL) constructing a digital design using combinational and sequential circuit in hardware description language like verilog or VHDL.The above architecture is converted into verilog or VHDL code.This code describes how data is transformed as it is passed from register to register

**RTL verification**:-
                It is a functional verification of RTL design.After the RTL design by applying test cases we verify the design in verification stage.If any mistakes are found then the design is re send to the RTL designing department.The verification stage will take nearly 60% of the total time.Performing this verification at this stage is most advantageous because correcting the faults at routing stage is difficult and takes more time.

**Synthesis**:-
               It is a process of converting the RTL code into gate level netlist.Up to RTL verification the design is technology independent.In synthesys process the design is converted into technology dependent.
It is 3 stage process.

1.**Translation**:- The RTL code is converted in to Boolean expression.

2.**Optimization**:- In this stage Boolean expression is optimized by SOP and POS optimization method.

3.**Mapping**:- In this technology independent Boolean expression is converted into technology dependent and generates the gate level net list.

The inputs for synthesis are RTL code, .SDC and .LIB.after the synthesis the generated outputs are gate level netlist and .SDC.

**DFT(Design for testability)**:-
                    It is a technique which facilitates a design to become testable after production.In this stage we put extra logic along with the design logic during implementation process which helps post production process.The DFT will make the testing easy at post production process.At this stage an ATPG(automatic test pattern generator) file will generated.

**Floorplan**:-
              The floorplan is the process of determining the macro placement,power grid generation and i/o placement.It is the process of placing blocks/macros in the chip/core area there by determining routing areas between them.It determines the size of the die and creates wire tracks for placement of standard cells.It creates power straps and specifies pg connection.It also determine the i/o ,pin/pad placement information.

**Placement**:-
          Placement is the process of automatically assigning correct position to standard cells on the chip with no overlapping.By global placement outside of standard cells will placed inside roughly.By the detailed placement the standard cells will place in site rows(legalize placement).In placement stage we check the congestion value by GRC map.


**CTS(clock tree synthesis)**:-
               In this stage we built the clock tree by using inverters and buffers.In the chip clock signal is essential to the flip flops,to give the clock signal from clock source we built the clock tree.It is the process of balancing the clock skew and minimizing insertion delay in order to meet timing and power.

	
**Routing**:-
               Before the routing stage the connection between the macros,standard cells,clock,i/o port are logical connections.In this stage we connect all the cells physically with the metal straps.
	       
Routing is divided into two parts.

1)global routing.

2)detailed routing.

The global routing will tell for which signal which metal layer is used.Before the detailed routing all are the logical connections.In detailed routing the physical connections are done.

**Signoff**:-
        After the routing the physical layout of chip is completed.In signoff stage all the tests are done to check the quality and performance of the layout before tapeout.After this the design is converted into GDS II file.

**Fabrication**:-
                By the GDS II file  information we fabricate the chip.The total design is converted into chip by the manufacturing process.

**Packaging and testing**:-
             After the fabrication process we test the chip.If there is any fault in the design then we modifies the design by repeating the steps.If there are no faults then chip will go to packaging.

**ASIC Vs FPGA**:-

![image](https://github.com/user-attachments/assets/322aa95f-73f9-450c-b252-6d40cd8c0bb7)

![image](https://github.com/user-attachments/assets/16152d9f-2990-48b1-8e55-762c901e1dcb)

**FPGA- A Conceptual View**:- An FPGA is like an electrical breadboard that is wired together by an automated synthesis tool. Built in components are caklles macros.

![Screenshot 2024-09-11 131447](https://github.com/user-attachments/assets/21370964-28c2-4d36-a4b7-791de765c7a1)

**FPGA- An inside look**:- Inside FPGA there are three building blocks.

1) Conficural liogic blocks(CLB)

2) I/O blocks

3) Programmable Routing or interconnects

![image](https://github.com/user-attachments/assets/ccae4b44-ac6b-40d4-a69b-a56b5f3d11a4)



**FPGA based design flow**:- 

![image](https://github.com/user-attachments/assets/02787787-5907-4240-beed-7136dfef1f75)

![image](https://github.com/user-attachments/assets/461b422a-e41b-48b7-aa45-b0a6825c71e8)


   
