# Sectors

Sectors are parts of the hardware responsible for a specific task, interconnected via an 8-bit bus.  
A specific operation is requested by setting the control signals on each sector.

## Sector list

| Sector  | Name                      | Description                                                  |
| :------ | :------------------------ | :----------------------------------------------------------- |
| **CLK** | *Clock*                   | Provides a global clock signal                               |
| **CL**  | *Control Logic*           | Activates control signals based on data stored in the IR     |
| **IR**  | *Instruction Register*    | Stores the currently executing instruction                   |
| **SPR** | *Stack Pointer Register*  | Stores the current stack base address                        |
| **PC**  | *Program Counter*         | Stores the program counter                                   |
| **MAR** | *Memory Address Register* | Stores the address of the currently accessed memory location |
| **MEM** | *Memory*                  | Stores program (ROM) and runtime data (RAM)                  |
| **A**   | *A Register*              | Stores primary operand for arithmetic operations             |
| **AU**  | *Arithmetic Unit*         | Performs arithmetic operations                               |
| **B**   | *B Register*              | Stores secondary operand for arithmetic operations           |
| **C**   | *C Register*              | Stores primary operand for logic operations                  |
| **LU**  | *Logic Unit*              | Performs logic operations                                    |
| **D**   | *D Register*              | Stores secondary operand for logic operations                |
| **I**   | *I Register*              | Stores the hold value during sequential arithmetic and logic |
| **J**   | *J Register*              | Stores the hold value during sequential arithmetic and logic |
| **Y**   | *Y Register*              | Stores operand for increments/decrements                     |
| **X**   | *X Register*              | Stores operand for increments/decrements                     |
| **DSP** | *Display*                 | Provides interface to 7 segment display                      |
| **IN**  | *Input*                   | Provides interface to PS/2 keyboard                          |
| **OUT** | *Output*                  | Provides interface to VGA monitor                            |
