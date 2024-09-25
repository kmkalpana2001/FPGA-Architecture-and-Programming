# FPGA-Architecture-and-Programming
# Contents
 <div class="toc">
  <ul>
    <li><a href="#header-1">Session-1</a></li>
    <ul>
    </div>
  
<div class="toc">
  <ul>
    <li><a href="#header-2">Session-2</a></li>
	<ul>
			
  </div>
  
  <div class="toc">
  <ul>
      <li><a href="#header-3">Session-3</a></li>
	<ul>
   </div>
  
  <div class="toc">
  <ul>
      <li><a href="#header-4">Session-4</a></li>			
        <ul>
      </div>
		
<div class="toc">
  <ul>
    <li><a href="#header-5">Session-5</a></li>
    <ul>
    </div>

  <div class="toc">
  <ul>
    <li><a href="#header-6">Session-6</a></li>
    <ul>
    </div>

  <div class="toc">
  <ul>
    <li><a href="#header-7">Session-7</a></li>
    <ul>
    </div>

  <div class="toc">
  <ul >
    <li><a href="#header-8">Session-8</a></li>
    <ul>
    </div>

  <div class="toc">
  <ul>
    <li><a href="#header-9">Session-9</a></li>
    <ul>
    </div>

  <div class="toc">
  <ul>
    <li><a href="#header-10">Session-10</a></li>
    <ul>
    </div>

<div class="toc">
  <ul>
      <li><a href="#header-11">Session-11</a></li>
	<ul>
   </div>

<div class="toc">
  <ul>
      <li><a href="#header-12">Session-12</a></li>
	<ul>
   </div>

<div class="toc">
  <ul>
      <li><a href="#header-13">Session-13</a></li>
	<ul>
   </div>
     
## <h1 id="header-1">Session-1</h1>	 

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


## <h2 id="header-2">Session-2</h2>	 

**Y- Chart**:- It is a model, which captures the considerations in designing semiconductor devices.

The three domains of the Gajski-Kuhn Y-chart are on radial axes. Each of the domains can be divided into levels of abstraction, using concentric rings.

At the top level (outer ring), we consider the architecture of the chip; at the lower levels (inner rings), we successively refine the design into finer detailed implementation −

Creating a structural description from a behavioral one is achieved through the processes of high-level synthesis or logical synthesis.

Creating a physical description from a structural one is achieved through layout synthesis.

 ![image](https://github.com/user-attachments/assets/09950f6c-15b1-4ab3-a09f-9fb73bcf1bd7)

**Need of HDL(High description language)**:- Hardware Description Language (HDL) is a programming language that is used to describe the structure, behaviour and timing of electronic circuits, and most commonly, digital logic circuits. HDLs are used for designing processors, motherboards, CPUs and various other Digital circuits. In addition to their use in circuit design, HDLs serve the purpose of simulating the circuit and verifying its response. Many HDLs are available, but the most popular HDLs so far are Verilog and VHDL. 

**What is Module**:- Module is the most fundamental block of verilog langauge. It can be a design block or a collection lower-level design blocks. It hides onternal implementation. Through ports provide necessary functionality to other modules. It has lot of input pins and output pins.

**Module Structure**:- Inside the module at the starting of module we have there will be module name(dont stat with a number) portlist, port decclaration, parameters declaration and then we have declaration of wire and reg variables. And then instantiationof other module if required. Module body consist of continuous statements or data flow statement some procedural block, always block andd initial block. andd then we have some task and functions and wee end the module with writing endmudule in the verilog cide language.

**Data Vlaues**:- Verilog supports these data values. 

0,1,z,x which has the meaning low/zero/false,highone/true,high impedence and uninitialized or unknown respectively.

**Number in Verilog**:- Syntax: <Size>'<Base><Value>

8'hax= 1010xxxx

12'o3zx7= 011zzzxxx111

If no base is specified then by default decimal will be considered as base to that particular number.

**Strings**:- Strings are enclosed in double quotes andd must be specified on one line. 

eg: ""This is string"

String variable declaration uses one byte per string character.

**Port types**:- 

![image](https://github.com/user-attachments/assets/ad3e718b-efcb-4212-9928-e31614307d23)

**Bsic Data Types**:- 

1) Net data type:- Represents physical interconnect between processes(activity flows)

![image](https://github.com/user-attachments/assets/2ae45431-0e9b-41c1-829e-646197fbd8b2)

2) Register ddata type:- Represent variable to store data temporarily. It ddoes not represent a physical(hardware) register.

![image](https://github.com/user-attachments/assets/4c85ce82-95cd-42b1-8925-bdc2197925da)

**Operators in Verilog**:- 

![image](https://github.com/user-attachments/assets/ad5268a0-6e77-4209-94fd-7f101491ba27)

**Vectora & Arrays**:- Vector represents bus where left number in MS bit and Vector assignment by position.

Array is a collection of the same data type.

![image](https://github.com/user-attachments/assets/130fce95-2bf8-4908-bc6e-02b182da9ff5)

**Memories**:- Memories can be modeledd as array of registers where each element in the array representa a word and each word can be one bit or multiple bits wide.

![image](https://github.com/user-attachments/assets/f4aa876a-1740-4b85-90dc-dc379d080af1)

**Parameters**:- Allows constant to be define in a module by the keyword parameter and it can not be used as variables. Paramete for each module instance can be overriddden individually at compile time.

Module definitions may be written in terms of parameters where gardcoded numbers should be avoied and parameters can be changed at module instantiations or by using the defparam statement.

**Levels of design abstraction**:- 

1) Behavioral level

2) Data flow level

3) Gate level

4) Switch level

**System task**:- 1)Monitoring and printing

```$display```:- For displaying values of variables or strings or expressions.

```$monitor```:- For continuously monitoring changes in the values of the variables in its sensitivity list.

![image](https://github.com/user-attachments/assets/b11ffec4-5a67-403d-bad6-29a8776e1343)

2)Stopping and Finishing

```$stop```:- To stop the current simulation and to put the compiler in debug mode.

```$finish```:- To terminate the simulation and to quit the compiler.


![image](https://github.com/user-attachments/assets/461b4b35-9bbe-43f4-a568-13b3a68850ab)


## <h3 id="header-3">Session-3</h3>

**Behavioral Modeling -Aconceptual view**:- 

1) Only the functionality of the circuit, no structure.

2) Synthesis tool creates correcte logic.

3) For the purpose of synthesis, as well as simulation.

![image](https://github.com/user-attachments/assets/168ba4e5-1db8-47da-b1b2-a0e9d65d2a69)

**Structural Modeling**:-  

1) Functionallity ansd structure of the circuit.

2) Call out the specific hardware.

3) For the purpose of synthesis.

![image](https://github.com/user-attachments/assets/d0b2422c-acbb-4195-87e2-92f7593bf7d3)

**2:1 MUX data flow using behavioral modeling**:-  

```
1) module mux2x1(a,b,s,out);
   input a,b,s,
   ouput out;
   wire sbar;
   assign sbar = ~s;
   assign out = (a&sbar) | (b&s);
   endmodule
   

2) Using conditional operator:-

   module mux2x1(a,b,s,out);
   input a,b,s,
   ouput out;
   assign out = s ? b: a;
   endmodule

3) Using if else:-

   module mux2x1(a,b,s,out);
   input a,b,s;
   ouput reg out;
   always@(a,b,s)
     begin
       if(s) out = b;
       else  out = a;
       end
     endmodule

4) Using case statement:-

   module mux2x1(a,b,s,out);
   input a,b,s;
   ouput reg out;
   always@(a,b,s)
     begin
       case(s)
        1'b0: out = a;
        1'b1: out = b;
        default: out = 1'bx;
        endcase
        end
     endmodule
```


## <h4 id="header-4">Session-4</h4>

**Design methodology**:-

1) **Top-Down**:- Define final(top) module then identify the sub module to be be added and then describe sub module and establish connections.

2) **Bottom-Up**:- Design the basic module(leaf cells) then assemble (instantiate ) sub moddules to the describe top module.

![image](https://github.com/user-attachments/assets/2ae76090-3266-4bfa-9dbc-2a6e36edcfc8)

**Module Instances**:- Module serves as template for creating actual new objects. Once invoked verilog creates a unique object from the template.

**Module Instantiation**:- The process of creting unique objects from the module template. The create ddobjects are called moddule instances. Each object has its own name, variables, parameters and I/O interfaces.

**Port connection Rules**:- 

Input ports should be of net ata type(wire) and can be connected to net as well as register to the external world.

Output ports may be register or a net internally but should be connected to net to the external world.

Width matching is illegal to connect an internal and external items of different sizes while making inter-moddule port connections.

![image](https://github.com/user-attachments/assets/07c59ea2-2c56-4941-9d96-75bda2d0cfb6)


**Module instantiation**:- 

**By port name: syntax**

![image](https://github.com/user-attachments/assets/94cf75f8-51d9-4a94-8f05-f746743eb101)

**Module name**:- name of the moddule to be instantiated (DUT)

**Instance Name**:- Specific name for this particular instantiation of DUT 

**a**"- Port of the module to be instantiated(sub module/DUT)

**v_a**:- Name of the corresponing port of the top level block 

Port connection list controls how this instantiation connects to the ports in the top level block. same module can be instantiated multiple time, but each with unique name.


**4-bit full adder : hierarchical view**:- 

![image](https://github.com/user-attachments/assets/3405e48a-72e0-4e98-aa47-46bc4577356f)

![image](https://github.com/user-attachments/assets/25144126-afe4-4d60-a6ff-23d72bfca609)

```
module ripple_carry_adder (
    input  [3:0] A,     
    input  [3:0] B,      
    input  Cin,   
    output [3:0] Sum,    
    output Cout    
);

    wire C1, C2, C3;

    full_adder FA0 (.A   (A[0]),.B   (B[0]),.Cin (Cin),.Sum (Sum[0]),.Cout(C1));
    full_adder FA1 (.A   (A[1]),.B   (B[1]),.Cin (C1),.Sum (Sum[1]),.Cout(C2));
    full_adder FA2 (.A   (A[2]),.B   (B[2]),.Cin (C2),.Sum (Sum[2]),.Cout(C3));
    full_adder FA3 (.A   (A[3]),.B   (B[3]),.Cin (C3),.Sum (Sum[3]),.Cout(Cout));

endmodule

module full_adder (
    input  A,        
    input  B,        
    input  Cin,      
    output Sum,    
    output Cout      
);

    assign Sum  = A ^ B ^ Cin;     
    assign Cout = (A & B) | (Cin & (A ^ B));  

endmodule
   ```

**Components of a Simulation**:- Once design is completed it must be varified.

![image](https://github.com/user-attachments/assets/2b4ce8e6-53cd-4fd6-b2b1-84de6d8f0ff7)

**Test bench example**:- 2-input AND gate

![image](https://github.com/user-attachments/assets/8ae25062-302c-47de-8c9a-87a6df898ca3)

```
   module and2(a,d,out);
    input a,b,
    output out;
    wire a,b,out;
    assign out =  a&b;
    endmodule


  module tb_and2;
    reg A;        
    reg B;         
    wire OUT;       

    and2 uut (.a(A),.b(B),.out(OUT));

    initial begin
        $monitor("Simtime=%g, A = %b, B = %b, OUT = %b", $time, A, B, OUT);
    end
    initial begin
        #5 A=0;B=0;    #5 A=0;B=1;    #5 A=1;B=0;    #5 A=1;B=1;
     end 
endmodule
```

## <h5 id="header-5">Session-5</h5>	 

**Finite state machine(FSM)**:- Finte state machine can be viewed as an abstract representative of a ddigital logic with limited of finite states. It is a mathemetical model of computation. FSM is defined by a list of its states, its initial states, and the inputs that trigger reach transition. The machine states are represented by a collection of states variables. Particularly useful in modeling behavior of controllers.

**Finite state machine types**:- 

1) Moore FSM- Outputs depend solely on state vector.

2) Mealy FSM- Ouputs depend on inputs and state vector.

![image](https://github.com/user-attachments/assets/fd21d854-fa6b-49d0-87d7-19cb4a811291)

**Components of FSM**:- Three basic components namely

1) combinational logic(that efines next state assignment)

2) Sequential logic(stores states)

3) Output logic(Moore or mealy)

4) Different encoding styles(Binary,gray,johnson,onehot,custom)


## <h6 id="header-6">Session-6</h6>	 

**Introduction to FPGA**:- 

In digital electronics systems there are mainly processing elements like ALU,processor cores, Memories , control logic, microprogram , FSM based control.

Control logic perform many functions including device to device interfacing, data communication control, timing and control etc.

![image](https://github.com/user-attachments/assets/c8b575ef-91eb-4e12-af22-4bc885c069cf)

**Logic Devices**:- A logic device is one which can perform any logic function. logic device are broadly classified into fixed and programmable logic devices.

Once manufactured logic in a fixed device cannot be changed. Programmable devices can be changed at any time to implement various logic functions.

**Programmable logic devices(PLD)**:- With PLD designers use inexpensive software tools to quickly develop, simulate and test the designs. Designs can be programmed and tested in a live circuit. PLD used for testing can be used for production. Fast completion of final design/fast prototyping of system. 

PLD is an integrated circuit with internal logic gates and interconnects. Gates can be connected to achieve the required logic function. The term programmable means changing the hardware configuration of internal logic and interconnects. Configuration of the internal logic is done by the user. PROM, PAL, PLA, GAL etc  are few examples of PLDs.

**Types of PLDs**:- 

PROM- Programmable OR array

PAL-Programmmable AND array

PLA- Programmable OR & AND array 

CPLDs- Multiple combination of PLAs/PALs and complex logic functions can be implemented and supports in circuit programming

FPGAs- Supports implementation of relatively large logic circuits. and supports ISP.

![image](https://github.com/user-attachments/assets/d8c6a40a-bd59-4428-97f7-cba414e17ff3)

**Field Programmable Gate Array(FPGA)**:-  FPGA contains programmable logic components and programmable interconnects. It can program FPGA to perform any digital logic. It also includes memory blocks, Io controllers, hard IPs to perform specific functions, embedded processors.

**FPGA Design Flow**:- 

1) **Full-Custom Design Flow**:- Full-custom design provides the highest level of design flexibility and optimization by allowing designers to customize every aspect of the IC. This approach is typically used for high-performance or specialized applications where standard cells or gate arrays do not meet the design requirements.

2) **Semi-Custom Design Flow**:- Semi-custom design involves using pre-designed and pre-tested building blocks or components to create a custom IC. This approach is less time-consuming than full-custom design and is generally used for faster and more cost-effective designs.

![image](https://github.com/user-attachments/assets/ce799831-2f11-487f-b40d-56d1ac18c619)


## <h7 id="header-7">Session-7</h7>	

**FPGA Architecture**:- An FPGA (Field-Programmable Gate Array) is a type of integrated circuit that is designed to be configured by a user after manufacturing, allowing for flexible and custom digital logic designs. The architecture of an FPGA consists of various building blocks that make it highly adaptable to a wide range of applications, including signal processing, telecommunications, and embedded systems.

**Key Components of FPGA Architecture:**

![image](https://github.com/user-attachments/assets/4d090595-42f9-4280-b1cb-15ea94babece)

**1) Configurable Logic Blocks (CLBs) or Logic Array Blocks (LABs):**

These are the fundamental building blocks of an FPGA, where the user-defined logic is implemented.Each CLB contains a combination of look-up tables (LUTs), flip-flops, and multiplexers.The LUTs perform combinational logic (truth table-based logic), while flip-flops handle sequential logic (storing data, clocked operations).Typically, a CLB/LAB can implement small logic functions, like AND, OR, and XOR.

![image](https://github.com/user-attachments/assets/8ebba2b4-85c9-467c-a50e-8e56d31e1f35)


**2) Interconnects (Routing):**

The routing network connects the CLBs to one another and to input/output blocks.
The routing is flexible and allows users to define how CLBs are interconnected.
Switches and programmable interconnect points (PIPs) are used to dynamically route signals between different CLBs, memory blocks, and I/O blocks.

![image](https://github.com/user-attachments/assets/3563c22c-b260-4c9b-a81c-c8154b1017ba)

![Screenshot 2024-09-19 111437](https://github.com/user-attachments/assets/65210fa8-42b2-4afe-9e47-d6f8797d169a)


**3) Input/Output Blocks (IOBs):**

These are special blocks that manage communication between the FPGA and external devices.
IOBs provide bidirectional communication, meaning they can act as both input and output channels.They support various signal standards (LVTTL, LVDS, etc.) and protocols depending on the application requirements.

![image](https://github.com/user-attachments/assets/884b019c-2fb9-4058-a802-57c2b7c02750)

**4) Block RAM (BRAM):**

Block RAM is on-chip memory that allows for the storage of large amounts of data.
It can be used for implementing buffers, caches, or other memory-intensive components.
BRAM blocks are distributed throughout the FPGA and can be accessed quickly by the logic blocks.

**5) Digital Signal Processing (DSP) Blocks:**

These specialized blocks are optimized for high-performance mathematical operations, particularly those involving multiplication and addition.
DSP blocks are commonly used in applications like image processing, audio processing, and communications.

**6) Clock Management Blocks (CMTs):**

Clock management is crucial in FPGA designs to ensure that various parts of the circuit work synchronously. FPGAs typically include phase-locked loops (PLLs) and delay-locked loops (DLLs) for clock generation, distribution, and frequency scaling.

**7) Global and Local Clock Networks:**

FPGAs contain global and local clock networks to efficiently distribute clock signals across the chip. These clock networks allow multiple clock domains to exist in a design, ensuring that the circuit can work reliably at different clock frequencies.

**8) Hard Macros or IP Cores:**

Many FPGAs contain predefined hardware modules like memory controllers, PCIe interfaces, Ethernet controllers, etc., which are known as IP cores. These hard macros are optimized for specific tasks and reduce the amount of custom logic that needs to be implemented.


## <h8 id="header-8">Session-8</h8>

**FPGA Configuration**:- An FPGA can be into two states

1) Configuration mode

2) User mode

Configuration of an FPGA means downloading a stream of 0's and 1's into it through some special pins. Once the FPGA is configured it goes into user mode and become active, performing accordingly to your programmed logic function.

Theere are three ways to configure FPGA:

1) Use a cable from a PC to hte FPGA and run a software on the PC ro send data through the cable.

2) Use a microcontroller on the board, with an adequate firmware to ssend data to the FPGA.

3) Use a boot-PROM/Flash on the board, connected to the FPGA, that configures the FPGA automatically at power-up.

**FPGA Programming**:- 
The behavior of the FPGA(logic function) canbe defined by HDL or a schematic design.

Compile the logic function on the PC using the software provided by the FPGA vendor that will create a binary file.

Connect a cable from the PC to the FPGA and download the binary file.

FPGA are volatile.

![Screenshot 2024-09-19 112606](https://github.com/user-attachments/assets/e00e6744-1451-46bb-9f97-34281aecd64e)

**FPGA Configurational Interfaces**:- 

1) Master(Serial or parallel)-  FPGA retrives configurational from ROM at initial power-up.

2) Slve(Serial or parallel)- FPGA configured by an external source like microprocessor or other FPGA.

3) Boundary Scan- 4-wire IEEE standard serial interface used for testing then write and read access to configure memory then interfaces to FPGA core internal routing network. And that will dveloped to test interconnect between chips on PCB and used to scan every Flops in a chip. FPGA bit steam can be written into configuration memory via JTAG interface.

![Screenshot 2024-09-19 113206](https://github.com/user-attachments/assets/4fd33b3a-7344-4bc0-97ec-aba6aa6d77a9)


## <h9 id="header-9">Session-9</h9>

**Digital Logic Synthesis**:- Synthesis is translation,optimization and mapping in which transtion from verilog/VHDL RTL to gate level circuits and then optimization in terms of timing, area and power then we do mapping.

![image](https://github.com/user-attachments/assets/52677dba-a652-4a97-ac7a-305e248f1adc)

**RTL Coding for synthesis**:- 

1) Infer registers

2) Avoid latches

3) Avoid combinational feedback

4) Specify complete sensitivity lists

5) In verilog, always use non-blocking assignments in always@(*edge clk)

6) Use case over if-then-else whenever priority structure not required.

7) Use separate always for sequential state register and combinational logic

8) Register all outputs


**Synthesis Optimization**:- 

**Time**- Top-most optimization criteria is time after that Power. 

**Power**- Power optimization is not enabled by default. Optimizes power constraints for leakage power and dynamic power set by the attributes. max_leakage_power & max_dynami_power.

**Area**- Smallest design that satisfies the timing constraints by default. Logic in the non-critical oaths is automatically downsized to save area.


## <h10 id="header-10">Session-10</h10>

**Hazards in combinational circuits**:- A hazard in a combo circuit may produce a glitch.A glitch is an unwanted spike. Glitches will generate unwanted high frequency components and spoil the circuit behaviour.


**Static zero hazard**:- A static zero hazard occurs when a circuit's output is supposed to remain at logic 0, but due to a delay in signal propagation, a brief unwanted 1 occurs.

**Static one hazard**:- A static one hazard occurs when a circuit's output is supposed to remain at logic 1, but due to signal delays, a brief unwanted 0 appears.

**Dynamic hazard**:- A dynamic hazard happens when the output transitions from one state to another (e.g., from 0 to 1 or 1 to 0), but instead of making a smooth transition, the output oscillates briefly between the two states.

![image](https://github.com/user-attachments/assets/b6975cdf-ed7d-4141-9b80-4ae28e2d62a1)

![image](https://github.com/user-attachments/assets/279e0a81-6528-4559-bdcd-57b9b5c91958)

**To remove the static hazard we need to add one extra redundant logic or gates to the given expression.** 

![image](https://github.com/user-attachments/assets/1dd38218-0d8e-4fbf-a3f9-02a91e6e6a97)

![image](https://github.com/user-attachments/assets/8493a19a-aefa-4a51-a5a9-757b69a53ada)

![image](https://github.com/user-attachments/assets/4e285ea0-7984-4b70-8c3b-6feeddee29c7)

![image](https://github.com/user-attachments/assets/55e7fa2a-e2c0-4eb6-9012-26fc0b07d50a)


**Timing in flip flops**:- 

**1) Propagation delay(tpd)**:- With respect to posedge input will be sampled and after tpd the outpup will be changed.

**2) Setup time(tst)**:- Before the posedge input should be stabilize that is called setup time.

**3) Hold time(tht)**:- After the possedge the input should not change it should be steady for certain time that is called hold time.

![image](https://github.com/user-attachments/assets/f6f06bba-124e-4f1b-a855-19a331cbaf3a)

**Slack**:- It is the diffrence between actual/achieved time and the desired time.

**How to set these timing violations?**

1) Fixing setup violations- Reduce the frequency of operation. Optimize the combo path. Use technique like pipe-lining, retiming etc.

2) Fixing hold violations- We need to add the delay in the data path. We can ddo this by adding buffer or latches in between the flip flops.

3) Fixing timing violation using clock skew- Changing clock network to improve timing. Positive skew improves setup time and Negative skew improves hold time.


**Techniques to improve timing performance**:-

**1) Retiming:-** Changing the flop locations to improve the timing.
   
![image](https://github.com/user-attachments/assets/227a9e27-bb42-472c-86f8-d17292a3215e)

**2) Pipelining:-** Break the combo path by adding flops in between Adds latency at the o/p. Improves the through put.

![image](https://github.com/user-attachments/assets/dc070b41-71fa-46f6-9588-e9abe5ee4d8b)

**3) Clock domain transfer(CDC):**- Lower clock domain to higher clock domain

![image](https://github.com/user-attachments/assets/a2bf6bb3-768a-413c-bbce-2e486ab10966)


## <h11 id="header-11">Session-11</h11>  

**System On Chip(SOC):-**  An SOC is an integrated circuit that package basic components into a single chip. An SOC has most of the components to power a computer. SoCs combine various processing units, memory, input/output ports, and other specialized hardware into a compact, power-efficient form. They are commonly used in mobile devices, embedded systems, IoT devices, and other areas where space, power, and cost savings are crucial.

**What is inside SoC**:- 

![image](https://github.com/user-attachments/assets/0457ec9d-3d2e-43d0-a24d-a7fb8508c07c)

![image](https://github.com/user-attachments/assets/ae996f60-1b10-4d7d-9de6-782d09ff0b12)

**Advantages of SoC**:- 

1) Low cost

2) Higher performonace

3) Higher reliability

4) Lighter footprint

5) Power efficiency

**Limitations of SoC**:- 

1) Less flexibility

2) Application specific

3) Complexity

![image](https://github.com/user-attachments/assets/e4808a65-6625-4b97-bc04-322eac32309a)


## <h12 id="header-12">Session-12</h12>  

**FPGA based SoC design:**- A typical digital system design involves 

Custom logic circuitry Processors, Memory units, Various types of input/output(I/O)interfaces

<li> Traditional approach to designsuch system is</li>

  1) A new integrated circuit(IC) chip may be created for the custom logic circuits.

  2) Each pre-designed component is included as a seperate chip.

<li> Different approach for realizing digital system called embedded system design.</li>

<li> It leverages the advance capabilities of todays IC technology by implementing many of the components of the system within a simple chip.</li>

  Such as field programmable gate array(FPGA).

**Why FPGA for SoC Design:**- 

<li>Offer large logic capacity, exceeding several million equivalent logic gates.</li>

<li>Dedicated memory resources.</li>

<li>Include special hardware circuitry that is often neede in digital systems.</li>

1) DSP blocks(with multiply and accumulate functionality)

2) Phase-locked loops(PLLs) or delay-locked loops(DLLs) that support complex clocking schemes.

<li>Support a wide range of interface standards- DDR SRAM memory, PCI and high serial protocols.</li>

<li>Embedded logic analyzers</li>

**FPGA based SoC design- Processors:**- 

Two types of processors are available to use in FPGA 

 <li>Hard Processors</li>

 <li>Soft processors</li>

**Hard processors:**- A pre designed circuit that is fabrictaed within the FPGA chip.

**Soft processors:**- The processor exists as code written in a hardware descriptoon language(HDL).

![image](https://github.com/user-attachments/assets/0f8441d8-006c-4367-86b3-f87bc8185b81)

**Example:**- 

<li>System consist of soft processor core</li>

<li>Peripherals are added to processor local bus / On chip peripheral bus </li>

<li>External memory interfaces.</li>

<li>The whole system can be used to develop SOC based applications.</li>

![image](https://github.com/user-attachments/assets/49fd560b-a3ff-4230-afb7-4eaefe7faf12)

![image](https://github.com/user-attachments/assets/957b16ff-35cc-4d92-9c94-e44f21f28f8e)

**Software tools for SoC:**-

<li>Two main aspects of the software tools</li>

1) The creation of the system hardware.

2) The development of the software that runs on the processors included in the system.

<li>For creating the hardware circuitry the tools allow the user to build a system by making use of pre-designed building blocks for processors, memory controllers, digital signal; processing circuits and various communiction mmodules(such as UARTs).</li>

<li>The software allows easy instantiation of these sub-circuits and can automatically interconnect them on the FPGA chip.</li>

<li>The Electronic desing automation tools generate memory maps for the system, allowing the processors to access systems hardware resources.</li>


**Conclusions**:- 

<li>FPGA is a reconfigurable hardware.</li>

<li>Complex digital system can be realized in an FPGA.</li>

<li>FPGAs can be used for fast product development/prototyping of electronics system.</li>

<li>FPGA based SoC ddesign proveds more flexibility to develop embedded applications.</li>


## <h13 id="header-13">Session-13</h13>  













