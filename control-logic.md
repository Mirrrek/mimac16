# Control logic

## Flags

| Flag            | Description                                    |
| :-------------- | :--------------------------------------------- |
| Zero            | Set if the result of an operation is zero      |
| Carry           | Set if result of an operation overflows 8 bits |
| Memory overflow | Set if the memory address overflows            |

## Inputs
| Length (bits) | Name                 | Description                         |
| :------------ | :------------------- | :---------------------------------- |
| 8             | Opcode               | Instruction opcode                  |
| 1             | Memory overflow flag | Set if the memory address overflows |
| 5             | Step                 | Microinstruction step               |

## Outputs (control signals)
| Sector | Signal | Supports `BANK` | Description                                                        |
| :----- | :----- | :-------------- | :----------------------------------------------------------------- |
| -      | `BANK` | -               | Enable `BANK` (access high byte of sectors)                        |
| CLK    | `RST`  | Yes             | Reset or halt (`BANK` low = reset, `BANK` high = halt)             |
| CL     | `SR`   | No              | Reset step                                                         |
| CL     | `SRZ`  | No              | Reset step if zero flag is set                                     |
| CL     | `SRC`  | No              | Reset step if carry flag is set                                    |
| CL     | `SRNZ` | No              | Reset step if zero flag is not set                                 |
| CL     | `SRNC` | No              | Reset step if carry flag is not set                                |
| IR     | `IRi`  | No              | Write to IR                                                        |
| SPR    | `SPRi` | Yes             | Write to SPR                                                       |
| SPR    | `SPRo` | Yes             | Read from SPR                                                      |
| PC     | `PCi`  | Yes             | Write to PC                                                        |
| PC     | `PCo`  | Yes             | Read from PC                                                       |
| PC     | `PC+`  | No              | Increment PC                                                       |
| MAR    | `MARi` | Yes             | Write to MAR                                                       |
| MAR    | `MAR+` | No              | Increment MAR                                                      |
| MEM    | `ROMi` | Yes             | Write to ROM and increment it                                      |
| MEM    | `ROMo` | Yes             | Read from ROM and increment it                                     |
| MEM    | `RAMi` | Yes             | Write to RAM and increment it                                      |
| MEM    | `RAMo` | Yes             | Read from RAM and increment it                                     |
| A      | `Ai`   | No              | Write to A                                                         |
| A      | `Ao`   | No              | Read from A                                                        |
| AU     | `AUo`  | Yes             | Read from AU (`BANK` low = add, `BANK` high = subtract)            |
| AU     | `AUCo` | Yes             | Read from AU with carry (`BANK` low = add, `BANK` high = subtract) |
| B      | `Bi`   | No              | Write to B                                                         |
| B      | `Bo`   | No              | Read from B                                                        |
| C      | `Ci`   | No              | Write to C                                                         |
| C      | `Co`   | No              | Read from C                                                        |
| LU     | `LUo`  | Yes             | Read from LU (`BANK` low = OR, `BANK` high = NAND)                 |
| D      | `Di`   | No              | Write to D                                                         |
| D      | `Do`   | No              | Read from D                                                        |
| I      | `Ii`   | No              | Write to I                                                         |
| I      | `Io`   | No              | Read from I                                                        |
| J      | `Ji`   | No              | Write to J                                                         |
| J      | `Jo`   | No              | Read from J                                                        |
| X      | `Xi`   | No              | Write to X                                                         |
| X      | `Xo`   | No              | Read from X                                                        |
| X      | `X+`   | No              | Increment X                                                        |
| X      | `X-`   | No              | Decrement X                                                        |
| Y      | `Yi`   | No              | Write to Y                                                         |
| Y      | `Yo`   | No              | Read from Y                                                        |
| Y      | `Y+`   | No              | Increment Y                                                        |
| Y      | `Y-`   | No              | Decrement Y                                                        |
| DSP    | `DSPi` | No              | Write to DSP                                                       |
| IN     | `INo`  | No              | Read from IN                                                       |
| IN     | `INs`  | No              | Read IN status                                                     |
| OUT    | `OUTi` | No              | Write to OUT and advance cursor                                    |
| OUT    | `OUTa` | Yes             | Set OUT address                                                    |
