# Binary-Gray-Converter

## Project Specifications

Implement an 8-bit Binary-to-Gray code converter for the value applied to the input port A. The result C will be displayed through the LEDs on the BASYS 3 development board. The description of the converter will be done in VHDL in the behavioral model.

<p align ="center">
    <img src="https://github.com/user-attachments/assets/f0f59ef8-b60f-4096-a83b-3d89a7f524dc" alt="Block diagram of the converter">
    <p align ="center">Block diagram of the converter</p> 
</p>


## Features
- The Gray code is a reflected binary code, which has the property that two adjacent numbers differ by the value of a single bit.
- In the input port A, signals representing numbers in binary code are introduced.
- Any numbers up to 8 bits can be entered.
- The input signals, representing numbers in binary code, are converted to output signals representing numbers in Gray code.
- In the output port C, signals representing numbers in Gray code are displayed through the LEDs on the development board.

## Implementation Method
To implement this module, the Vivado synthesis tool and VHDL language were used.

- The entity Converter was designed.
- In this, an input variable was declared, representing the number in binary code, and an output variable, representing the number transformed into Gray code.
- The conversion algorithm was created using the following method:
    - The most significant bit of the Gray code is equal to the most significant bit of the binary code.
    - The other bits of the Gray code are obtained by the XOR operation between the bit from the binary code at index i and the bit at index i-1 from the binary code.

The bitstream file created by the Vivado tool was tested using the BASYS 3 Artix-7 xc7a35tcpg236-1 development board.

## Description of the BASYS 3 development system

The BASYS 3 development board is a complete, ready-to-use development circuit based on the latest Artix-7 Field Programmable Gate Arrays (FPGAs) produced by Xilinx. With a large FPGA capacity and a collection of USB, VGA, and other ports, the BASYS 3 development board allows for the design of a wide variety of projects, from introductory combinational circuits to complex sequential circuits such as processors and embedded controllers.

## Development board images
![20230118_175744](https://github.com/user-attachments/assets/94306aa5-82e1-4e56-add6-3bfaaf1d762f)
![20230118_175741](https://github.com/user-attachments/assets/d197bc75-57e3-4fb2-b266-4e5f5fee4cc5)
