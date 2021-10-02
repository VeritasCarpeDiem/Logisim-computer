# Logisim-computer
## A RISC (reduced instruction set computer) computer implemented in Logisim.
- Key digital logic concepts: multiplexers, demultiplexers, logic gates, bit splitters, etc. 
- Key componenets: RAM, ROM, ALU, program counter, registers, instruction decoder, JMPinstruction, and MEMinsntruction.  
## How to Run:
1. Install ![Logisim](http://www.cburch.com/logisim/). 
2. Download computer.circ
3. Open the file. 
 
## What does it do?
In a single clock cycle (fetch -> decode -> execute)...
1. The program counter increments
2. The ROM (read only memory) sends 0xbeef values to the register and the opcode to either JmpInstruction, MemoryInstruction, or the ALU (arithmetic logic unit). 
- JmpInstruction: Handles any "``goto``" type opcodes. ``if`` statements that need to jump to a particular memory address of the program memory need to be processed through this unit. 
- MemInstruction: Handles Push, pop, load, store assembly instructions
- ALU: Handles add, subtract, multiply, divide operations
4. The instructiondecoder decodes the opcode, icnrements the stack pointer, and the outputs a outval.
5. The outval is sent to the RAM, which simply displays the value, which is 0xBEEF. 
