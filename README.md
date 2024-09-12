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
	
   </div>
  
  <div class="toc">
  <ul>
      <li><a href="#header-4">Session-4</a></li>			
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
    input  [3:0] A,      // 4-bit input A
    input  [3:0] B,      // 4-bit input B
    input        Cin,    // Carry-in for the least significant bit
    output [3:0] Sum,    // 4-bit output Sum
    output       Cout    // Carry-out from the most significant bit
);

    // Intermediate carry signals
    wire C1, C2, C3;

    // Full Adder for the least significant bit (LSB)
    full_adder FA0 (
        .A   (A[0]),
        .B   (B[0]),
        .Cin (Cin),
        .Sum (Sum[0]),
        .Cout(C1)
    );

    // Full Adder for the second bit
    full_adder FA1 (
        .A   (A[1]),
        .B   (B[1]),
        .Cin (C1),
        .Sum (Sum[1]),
        .Cout(C2)
    );

    // Full Adder for the third bit
    full_adder FA2 (
        .A   (A[2]),
        .B   (B[2]),
        .Cin (C2),
        .Sum (Sum[2]),
        .Cout(C3)
    );

    // Full Adder for the most significant bit (MSB)
    full_adder FA3 (
        .A   (A[3]),
        .B   (B[3]),
        .Cin (C3),
        .Sum (Sum[3]),
        .Cout(Cout)
    );

endmodule

// Full Adder Module
module full_adder (
    input  A,        // Input A
    input  B,        // Input B
    input  Cin,      // Carry-in
    output Sum,      // Sum output
    output Cout      // Carry-out
);

    assign Sum  = A ^ B ^ Cin;      // Sum calculation
    assign Cout = (A & B) | (Cin & (A ^ B));  // Carry-out calculation

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

## <h5 id="header-5">Session-5</h1>	 




