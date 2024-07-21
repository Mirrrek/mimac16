# Instruction set

|    Opcode     | Instruction |           Name           |    Parameters     | Flags updated | Description                                                                    |
| :-----------: | :---------: | :----------------------: | :---------------: | :-----------: | :----------------------------------------------------------------------------- |
|    `0x00`     |    `NOP`    |       No operation       |         -         |       -       | No operation                                                                   |
|    `0x01`     |    `SET`    |           Set            |    `<s>` `<c>`    |       -       | Assign constant value to stack variable                                        |
|    `0x02`     |    `SET`    |           Set            |    `<s>` `<s>`    |       -       | Assign stack variable to stack variable                                        |
|    `0x03`     |    `SET`    |           Set            |    `<s>` `<h>`    |       -       | Assign heap variable to stack variable                                         |
|    `0x04`     |    `SET`    |           Set            |    `<s>` `<g>`    |       -       | Assign global variable to stack variable                                       |
|    `0x05`     |    `SET`    |           Set            |    `<h>` `<c>`    |       -       | Assign constant value to heap variable                                         |
|    `0x06`     |    `SET`    |           Set            |    `<h>` `<s>`    |       -       | Assign stack variable to heap variable                                         |
|    `0x07`     |    `SET`    |           Set            |    `<h>` `<h>`    |       -       | Assign heap variable to heap variable                                          |
|    `0x08`     |    `SET`    |           Set            |    `<h>` `<g>`    |       -       | Assign global variable to heap variable                                        |
|    `0x09`     |    `SET`    |           Set            |    `<g>` `<c>`    |       -       | Assign constant value to global variable                                       |
|    `0x0a`     |    `SET`    |           Set            |    `<g>` `<s>`    |       -       | Assign stack variable to global variable                                       |
|    `0x0b`     |    `SET`    |           Set            |    `<g>` `<h>`    |       -       | Assign heap variable to global variable                                        |
|    `0x0c`     |    `SET`    |           Set            |    `<g>` `<g>`    |       -       | Assign global variable to global variable                                      |
|    `0x0d`     |   `SET16`   |          Set 16          |    `<s>` `<c>`    |       -       | Assign constant value to stack variable (16 bit)                               |
|    `0x0e`     |   `SET16`   |          Set 16          |    `<s>` `<s>`    |       -       | Assign stack variable to stack variable (16 bit)                               |
|    `0x0f`     |   `SET16`   |          Set 16          |    `<s>` `<h>`    |       -       | Assign heap variable to stack variable (16 bit)                                |
|    `0x10`     |   `SET16`   |          Set 16          |    `<s>` `<g>`    |       -       | Assign global variable to stack variable (16 bit)                              |
|    `0x11`     |   `SET16`   |          Set 16          |    `<h>` `<c>`    |       -       | Assign constant value to heap variable (16 bit)                                |
|    `0x12`     |   `SET16`   |          Set 16          |    `<h>` `<s>`    |       -       | Assign stack variable to heap variable (16 bit)                                |
|    `0x13`     |   `SET16`   |          Set 16          |    `<h>` `<h>`    |       -       | Assign heap variable to heap variable (16 bit)                                 |
|    `0x14`     |   `SET16`   |          Set 16          |    `<h>` `<g>`    |       -       | Assign global variable to heap variable (16 bit)                               |
|    `0x15`     |   `SET16`   |          Set 16          |    `<g>` `<c>`    |       -       | Assign constant value to global variable (16 bit)                              |
|    `0x16`     |   `SET16`   |          Set 16          |    `<g>` `<s>`    |       -       | Assign stack variable to global variable (16 bit)                              |
|    `0x17`     |   `SET16`   |          Set 16          |    `<g>` `<h>`    |       -       | Assign heap variable to global variable (16 bit)                               |
|    `0x18`     |   `SET16`   |          Set 16          |    `<g>` `<g>`    |       -       | Assign global variable to global variable (16 bit)                             |
|    `0x19`     |    `ADD`    |        Direct add        | `<c>` `<s>` `<s>` |    `Z` `C`    | Add constant to stack variable and store result in stack                       |
|    `0x1a`     |    `ADD`    |        Direct add        | `<c>` `<s>` `<h>` |    `Z` `C`    | Add constant to stack variable and store result in heap                        |
|    `0x1b`     |    `ADD`    |        Direct add        | `<c>` `<h>` `<s>` |    `Z` `C`    | Add constant to heap variable and store result in stack                        |
|    `0x1c`     |    `ADD`    |        Direct add        | `<c>` `<h>` `<h>` |    `Z` `C`    | Add constant to heap variable and store result in heap                         |
|    `0x1d`     |    `ADD`    |        Direct add        | `<s>` `<s>` `<s>` |    `Z` `C`    | Add stack variable to stack variable and store result in stack                 |
|    `0x1e`     |    `ADD`    |        Direct add        | `<s>` `<s>` `<h>` |    `Z` `C`    | Add stack variable to stack variable and store result in heap                  |
|    `0x1f`     |    `ADD`    |        Direct add        | `<s>` `<h>` `<s>` |    `Z` `C`    | Add stack variable to heap variable and store result in stack                  |
|    `0x20`     |    `ADD`    |        Direct add        | `<s>` `<h>` `<h>` |    `Z` `C`    | Add stack variable to heap variable and store result in heap                   |
|    `0x21`     |    `ADD`    |        Direct add        | `<h>` `<s>` `<s>` |    `Z` `C`    | Add heap variable to stack variable and store result in stack                  |
|    `0x22`     |    `ADD`    |        Direct add        | `<h>` `<s>` `<h>` |    `Z` `C`    | Add heap variable to stack variable and store result in heap                   |
|    `0x23`     |    `ADD`    |        Direct add        | `<h>` `<h>` `<s>` |    `Z` `C`    | Add heap variable to heap variable and store result in stack                   |
|    `0x24`     |    `ADD`    |        Direct add        | `<h>` `<h>` `<h>` |    `Z` `C`    | Add heap variable to heap variable and store result in heap                    |
|    `0x25`     |   `ADD16`   |      Direct add 16       | `<c>` `<s>` `<s>` |    `Z` `C`    | Add constant to stack variable and store result in stack (16 bit)              |
|    `0x26`     |   `ADD16`   |      Direct add 16       | `<c>` `<s>` `<h>` |    `Z` `C`    | Add constant to stack variable and store result in heap (16 bit)               |
|    `0x27`     |   `ADD16`   |      Direct add 16       | `<c>` `<h>` `<s>` |    `Z` `C`    | Add constant to heap variable and store result in stack (16 bit)               |
|    `0x28`     |   `ADD16`   |      Direct add 16       | `<c>` `<h>` `<h>` |    `Z` `C`    | Add constant to heap variable and store result in heap (16 bit)                |
|    `0x29`     |   `ADD16`   |      Direct add 16       | `<s>` `<s>` `<s>` |    `Z` `C`    | Add stack variable to stack variable and store result in stack (16 bit)        |
|    `0x2a`     |   `ADD16`   |      Direct add 16       | `<s>` `<s>` `<h>` |    `Z` `C`    | Add stack variable to stack variable and store result in heap (16 bit)         |
|    `0x2b`     |   `ADD16`   |      Direct add 16       | `<s>` `<h>` `<s>` |    `Z` `C`    | Add stack variable to heap variable and store result in stack (16 bit)         |
|    `0x2c`     |   `ADD16`   |      Direct add 16       | `<s>` `<h>` `<h>` |    `Z` `C`    | Add stack variable to heap variable and store result in heap (16 bit)          |
|    `0x2d`     |   `ADD16`   |      Direct add 16       | `<h>` `<s>` `<s>` |    `Z` `C`    | Add heap variable to stack variable and store result in stack (16 bit)         |
|    `0x2e`     |   `ADD16`   |      Direct add 16       | `<h>` `<s>` `<h>` |    `Z` `C`    | Add heap variable to stack variable and store result in heap (16 bit)          |
|    `0x2f`     |   `ADD16`   |      Direct add 16       | `<h>` `<h>` `<s>` |    `Z` `C`    | Add heap variable to heap variable and store result in stack (16 bit)          |
|    `0x30`     |   `ADD16`   |      Direct add 16       | `<h>` `<h>` `<h>` |    `Z` `C`    | Add heap variable to heap variable and store result in heap (16 bit)           |
|    `0x31`     |    `SUB`    |     Direct subtract      | `<c>` `<s>` `<s>` |    `Z` `C`    | Subtract stack variable from constant and store result in stack                |
|    `0x32`     |    `SUB`    |     Direct subtract      | `<c>` `<s>` `<h>` |    `Z` `C`    | Subtract stack variable from constant and store result in heap                 |
|    `0x33`     |    `SUB`    |     Direct subtract      | `<c>` `<h>` `<s>` |    `Z` `C`    | Subtract heap variable from constant and store result in stack                 |
|    `0x34`     |    `SUB`    |     Direct subtract      | `<c>` `<h>` `<h>` |    `Z` `C`    | Subtract heap variable from constant and store result in heap                  |
|    `0x35`     |    `SUB`    |     Direct subtract      | `<s>` `<s>` `<s>` |    `Z` `C`    | Subtract stack variable from stack variable and store result in stack          |
|    `0x36`     |    `SUB`    |     Direct subtract      | `<s>` `<s>` `<h>` |    `Z` `C`    | Subtract stack variable from stack variable and store result in heap           |
|    `0x37`     |    `SUB`    |     Direct subtract      | `<s>` `<h>` `<s>` |    `Z` `C`    | Subtract heap variable from stack variable and store result in stack           |
|    `0x38`     |    `SUB`    |     Direct subtract      | `<s>` `<h>` `<h>` |    `Z` `C`    | Subtract heap variable from stack variable and store result in heap            |
|    `0x39`     |    `SUB`    |     Direct subtract      | `<h>` `<s>` `<s>` |    `Z` `C`    | Subtract stack variable from heap variable and store result in stack           |
|    `0x3a`     |    `SUB`    |     Direct subtract      | `<h>` `<s>` `<h>` |    `Z` `C`    | Subtract stack variable from heap variable and store result in heap            |
|    `0x3b`     |    `SUB`    |     Direct subtract      | `<h>` `<h>` `<s>` |    `Z` `C`    | Subtract heap variable from heap variable and store result in stack            |
|    `0x3c`     |    `SUB`    |     Direct subtract      | `<h>` `<h>` `<h>` |    `Z` `C`    | Subtract heap variable from heap variable and store result in heap             |
|    `0x3d`     |   `SUB16`   |    Direct subtract 16    | `<c>` `<s>` `<s>` |    `Z` `C`    | Subtract stack variable from constant and store result in stack (16 bit)       |
|    `0x3e`     |   `SUB16`   |    Direct subtract 16    | `<c>` `<s>` `<h>` |    `Z` `C`    | Subtract stack variable from constant and store result in heap (16 bit)        |
|    `0x3f`     |   `SUB16`   |    Direct subtract 16    | `<c>` `<h>` `<s>` |    `Z` `C`    | Subtract heap variable from constant and store result in stack (16 bit)        |
|    `0x40`     |   `SUB16`   |    Direct subtract 16    | `<c>` `<h>` `<h>` |    `Z` `C`    | Subtract heap variable from constant and store result in heap (16 bit)         |
|    `0x41`     |   `SUB16`   |    Direct subtract 16    | `<s>` `<s>` `<s>` |    `Z` `C`    | Subtract stack variable from stack variable and store result in stack (16 bit) |
|    `0x42`     |   `SUB16`   |    Direct subtract 16    | `<s>` `<s>` `<h>` |    `Z` `C`    | Subtract stack variable from stack variable and store result in heap (16 bit)  |
|    `0x43`     |   `SUB16`   |    Direct subtract 16    | `<s>` `<h>` `<s>` |    `Z` `C`    | Subtract heap variable from stack variable and store result in stack (16 bit)  |
|    `0x44`     |   `SUB16`   |    Direct subtract 16    | `<s>` `<h>` `<h>` |    `Z` `C`    | Subtract heap variable from stack variable and store result in heap (16 bit)   |
|    `0x45`     |   `SUB16`   |    Direct subtract 16    | `<h>` `<s>` `<s>` |    `Z` `C`    | Subtract stack variable from heap variable and store result in stack (16 bit)  |
|    `0x46`     |   `SUB16`   |    Direct subtract 16    | `<h>` `<s>` `<h>` |    `Z` `C`    | Subtract stack variable from heap variable and store result in heap (16 bit)   |
|    `0x47`     |   `SUB16`   |    Direct subtract 16    | `<h>` `<h>` `<s>` |    `Z` `C`    | Subtract heap variable from heap variable and store result in stack (16 bit)   |
|    `0x48`     |   `SUB16`   |    Direct subtract 16    | `<h>` `<h>` `<h>` |    `Z` `C`    | Subtract heap variable from heap variable and store result in heap (16 bit)    |
|    `0x49`     |    `OR`     |        Direct OR         | `<c>` `<s>` `<s>` |      `Z`      | OR constant with stack variable and store result in stack                      |
|    `0x4a`     |    `OR`     |        Direct OR         | `<c>` `<s>` `<h>` |      `Z`      | OR constant with stack variable and store result in heap                       |
|    `0x4b`     |    `OR`     |        Direct OR         | `<c>` `<h>` `<s>` |      `Z`      | OR constant with heap variable and store result in stack                       |
|    `0x4c`     |    `OR`     |        Direct OR         | `<c>` `<h>` `<h>` |      `Z`      | OR constant with heap variable and store result in heap                        |
|    `0x4d`     |    `OR`     |        Direct OR         | `<s>` `<s>` `<s>` |      `Z`      | OR stack variable with stack variable and store result in stack                |
|    `0x4e`     |    `OR`     |        Direct OR         | `<s>` `<s>` `<h>` |      `Z`      | OR stack variable with stack variable and store result in heap                 |
|    `0x4f`     |    `OR`     |        Direct OR         | `<s>` `<h>` `<s>` |      `Z`      | OR stack variable with heap variable and store result in stack                 |
|    `0x50`     |    `OR`     |        Direct OR         | `<s>` `<h>` `<h>` |      `Z`      | OR stack variable with heap variable and store result in heap                  |
|    `0x51`     |    `OR`     |        Direct OR         | `<h>` `<s>` `<s>` |      `Z`      | OR heap variable with stack variable and store result in stack                 |
|    `0x52`     |    `OR`     |        Direct OR         | `<h>` `<s>` `<h>` |      `Z`      | OR heap variable with stack variable and store result in heap                  |
|    `0x53`     |    `OR`     |        Direct OR         | `<h>` `<h>` `<s>` |      `Z`      | OR heap variable with heap variable and store result in stack                  |
|    `0x54`     |    `OR`     |        Direct OR         | `<h>` `<h>` `<h>` |      `Z`      | OR heap variable with heap variable and store result in heap                   |
|    `0x55`     |   `OR16`    |       Direct OR 16       | `<c>` `<s>` `<s>` |      `Z`      | OR constant with stack variable and store result in stack (16 bit)             |
|    `0x56`     |   `OR16`    |       Direct OR 16       | `<c>` `<s>` `<h>` |      `Z`      | OR constant with stack variable and store result in heap (16 bit)              |
|    `0x57`     |   `OR16`    |       Direct OR 16       | `<c>` `<h>` `<s>` |      `Z`      | OR constant with heap variable and store result in stack (16 bit)              |
|    `0x58`     |   `OR16`    |       Direct OR 16       | `<c>` `<h>` `<h>` |      `Z`      | OR constant with heap variable and store result in heap (16 bit)               |
|    `0x59`     |   `OR16`    |       Direct OR 16       | `<s>` `<s>` `<s>` |      `Z`      | OR stack variable with stack variable and store result in stack (16 bit)       |
|    `0x5a`     |   `OR16`    |       Direct OR 16       | `<s>` `<s>` `<h>` |      `Z`      | OR stack variable with stack variable and store result in heap (16 bit)        |
|    `0x5b`     |   `OR16`    |       Direct OR 16       | `<s>` `<h>` `<s>` |      `Z`      | OR stack variable with heap variable and store result in stack (16 bit)        |
|    `0x5c`     |   `OR16`    |       Direct OR 16       | `<s>` `<h>` `<h>` |      `Z`      | OR stack variable with heap variable and store result in heap (16 bit)         |
|    `0x5d`     |   `OR16`    |       Direct OR 16       | `<h>` `<s>` `<s>` |      `Z`      | OR heap variable with stack variable and store result in stack (16 bit)        |
|    `0x5e`     |   `OR16`    |       Direct OR 16       | `<h>` `<s>` `<h>` |      `Z`      | OR heap variable with stack variable and store result in heap (16 bit)         |
|    `0x5f`     |   `OR16`    |       Direct OR 16       | `<h>` `<h>` `<s>` |      `Z`      | OR heap variable with heap variable and store result in stack (16 bit)         |
|    `0x60`     |   `OR16`    |       Direct OR 16       | `<h>` `<h>` `<h>` |      `Z`      | OR heap variable with heap variable and store result in heap (16 bit)          |
|    `0x61`     |   `NAND`    |       Direct NAND        | `<c>` `<s>` `<s>` |      `Z`      | NAND constant with stack variable and store result in stack                    |
|    `0x62`     |   `NAND`    |       Direct NAND        | `<c>` `<s>` `<h>` |      `Z`      | NAND constant with stack variable and store result in heap                     |
|    `0x63`     |   `NAND`    |       Direct NAND        | `<c>` `<h>` `<s>` |      `Z`      | NAND constant with heap variable and store result in stack                     |
|    `0x64`     |   `NAND`    |       Direct NAND        | `<c>` `<h>` `<h>` |      `Z`      | NAND constant with heap variable and store result in heap                      |
|    `0x65`     |   `NAND`    |       Direct NAND        | `<s>` `<s>` `<s>` |      `Z`      | NAND stack variable with stack variable and store result in stack              |
|    `0x66`     |   `NAND`    |       Direct NAND        | `<s>` `<s>` `<h>` |      `Z`      | NAND stack variable with stack variable and store result in heap               |
|    `0x67`     |   `NAND`    |       Direct NAND        | `<s>` `<h>` `<s>` |      `Z`      | NAND stack variable with heap variable and store result in stack               |
|    `0x68`     |   `NAND`    |       Direct NAND        | `<s>` `<h>` `<h>` |      `Z`      | NAND stack variable with heap variable and store result in heap                |
|    `0x69`     |   `NAND`    |       Direct NAND        | `<h>` `<s>` `<s>` |      `Z`      | NAND heap variable with stack variable and store result in stack               |
|    `0x6a`     |   `NAND`    |       Direct NAND        | `<h>` `<s>` `<h>` |      `Z`      | NAND heap variable with stack variable and store result in heap                |
|    `0x6b`     |   `NAND`    |       Direct NAND        | `<h>` `<h>` `<s>` |      `Z`      | NAND heap variable with heap variable and store result in stack                |
|    `0x6c`     |   `NAND`    |       Direct NAND        | `<h>` `<h>` `<h>` |      `Z`      | NAND heap variable with heap variable and store result in heap                 |
|    `0x6d`     |  `NAND16`   |      Direct NAND 16      | `<c>` `<s>` `<s>` |      `Z`      | NAND constant with stack variable and store result in stack (16 bit)           |
|    `0x6e`     |  `NAND16`   |      Direct NAND 16      | `<c>` `<s>` `<h>` |      `Z`      | NAND constant with stack variable and store result in heap (16 bit)            |
|    `0x6f`     |  `NAND16`   |      Direct NAND 16      | `<c>` `<h>` `<s>` |      `Z`      | NAND constant with heap variable and store result in stack (16 bit)            |
|    `0x70`     |  `NAND16`   |      Direct NAND 16      | `<c>` `<h>` `<h>` |      `Z`      | NAND constant with heap variable and store result in heap (16 bit)             |
|    `0x71`     |  `NAND16`   |      Direct NAND 16      | `<s>` `<s>` `<s>` |      `Z`      | NAND stack variable with stack variable and store result in stack (16 bit)     |
|    `0x72`     |  `NAND16`   |      Direct NAND 16      | `<s>` `<s>` `<h>` |      `Z`      | NAND stack variable with stack variable and store result in heap (16 bit)      |
|    `0x73`     |  `NAND16`   |      Direct NAND 16      | `<s>` `<h>` `<s>` |      `Z`      | NAND stack variable with heap variable and store result in stack (16 bit)      |
|    `0x74`     |  `NAND16`   |      Direct NAND 16      | `<s>` `<h>` `<h>` |      `Z`      | NAND stack variable with heap variable and store result in heap (16 bit)       |
|    `0x75`     |  `NAND16`   |      Direct NAND 16      | `<h>` `<s>` `<s>` |      `Z`      | NAND heap variable with stack variable and store result in stack (16 bit)      |
|    `0x76`     |  `NAND16`   |      Direct NAND 16      | `<h>` `<s>` `<h>` |      `Z`      | NAND heap variable with stack variable and store result in heap (16 bit)       |
|    `0x77`     |  `NAND16`   |      Direct NAND 16      | `<h>` `<h>` `<s>` |      `Z`      | NAND heap variable with heap variable and store result in stack (16 bit)       |
|    `0x78`     |  `NAND16`   |      Direct NAND 16      | `<h>` `<h>` `<h>` |      `Z`      | NAND heap variable with heap variable and store result in heap (16 bit)        |
|    `0x79`     |    `CMP`    |      Direct compare      |    `<c>` `<s>`    |    `Z` `C`    | Subtract stack variable from constant and discard result                       |
|    `0x7a`     |    `CMP`    |      Direct compare      |    `<c>` `<h>`    |    `Z` `C`    | Subtract heap variable from constant and discard result                        |
|    `0x7b`     |    `CMP`    |      Direct compare      |    `<s>` `<s>`    |    `Z` `C`    | Subtract stack variable from stack variable and discard result                 |
|    `0x7c`     |    `CMP`    |      Direct compare      |    `<s>` `<h>`    |    `Z` `C`    | Subtract heap variable from stack variable and discard result                  |
|    `0x7d`     |    `CMP`    |      Direct compare      |    `<h>` `<s>`    |    `Z` `C`    | Subtract stack variable from heap variable and discard result                  |
|    `0x7e`     |    `CMP`    |      Direct compare      |    `<h>` `<h>`    |    `Z` `C`    | Subtract heap variable from heap variable and discard result                   |
|    `0x7f`     |   `CMP16`   |    Direct compare 16     |    `<c>` `<s>`    |    `Z` `C`    | Subtract stack variable from constant and discard result (16 bit)              |
|    `0x80`     |   `CMP16`   |    Direct compare 16     |    `<c>` `<h>`    |    `Z` `C`    | Subtract heap variable from constant and discard result (16 bit)               |
|    `0x81`     |   `CMP16`   |    Direct compare 16     |    `<s>` `<s>`    |    `Z` `C`    | Subtract stack variable from stack variable and discard result (16 bit)        |
|    `0x82`     |   `CMP16`   |    Direct compare 16     |    `<s>` `<h>`    |    `Z` `C`    | Subtract heap variable from stack variable and discard result (16 bit)         |
|    `0x83`     |   `CMP16`   |    Direct compare 16     |    `<h>` `<s>`    |    `Z` `C`    | Subtract stack variable from heap variable and discard result (16 bit)         |
|    `0x84`     |   `CMP16`   |    Direct compare 16     |    `<h>` `<h>`    |    `Z` `C`    | Subtract heap variable from heap variable and discard result (16 bit)          |
|    `0x85`     |  `SLOADA`   |    Sequential load A     |       `<c>`       |       -       | Load constant into A operand                                                   |
|    `0x86`     |  `SLOADA`   |    Sequential load A     |       `<s>`       |       -       | Load stack variable into A operand                                             |
|    `0x87`     |  `SLOADA`   |    Sequential load A     |       `<h>`       |       -       | Load heap variable into A operand                                              |
|    `0x88`     |  `SLOADA`   |    Sequential load A     |       `<g>`       |       -       | Load global variable into A operand                                            |
|    `0x89`     | `SLOADA16`  |   Sequential load A 16   |       `<c>`       |       -       | Load constant into A operand (16 bit)                                          |
|    `0x8a`     | `SLOADA16`  |   Sequential load A 16   |       `<s>`       |       -       | Load stack variable into A operand (16 bit)                                    |
|    `0x8b`     | `SLOADA16`  |   Sequential load A 16   |       `<h>`       |       -       | Load heap variable into A operand (16 bit)                                     |
|    `0x8c`     | `SLOADA16`  |   Sequential load A 16   |       `<g>`       |       -       | Load global variable into A operand (16 bit)                                   |
|    `0x8d`     |  `SLOADB`   |    Sequential load B     |       `<c>`       |       -       | Load constant into B operand                                                   |
|    `0x8e`     |  `SLOADB`   |    Sequential load B     |       `<s>`       |       -       | Load stack variable into B operand                                             |
|    `0x8f`     |  `SLOADB`   |    Sequential load B     |       `<h>`       |       -       | Load heap variable into B operand                                              |
|    `0x90`     |  `SLOADB`   |    Sequential load B     |       `<g>`       |       -       | Load global variable into B operand                                            |
|    `0x91`     | `SLOADB16`  |   Sequential load B 16   |       `<c>`       |       -       | Load constant into B operand (16 bit)                                          |
|    `0x92`     | `SLOADB16`  |   Sequential load B 16   |       `<s>`       |       -       | Load stack variable into B operand (16 bit)                                    |
|    `0x93`     | `SLOADB16`  |   Sequential load B 16   |       `<h>`       |       -       | Load heap variable into B operand (16 bit)                                     |
|    `0x94`     | `SLOADB16`  |   Sequential load B 16   |       `<g>`       |       -       | Load global variable into B operand (16 bit)                                   |
|    `0x95`     |   `SADDA`   |     Sequential add A     |         -         |    `Z` `C`    | Add A operand to B operand and store result in A operand                       |
|    `0x96`     |  `SADDA16`  |   Sequential add A 16    |         -         |    `Z` `C`    | Add A operand to B operand and store result in A operand (16 bit)              |
|    `0x97`     |   `SADDB`   |     Sequential add B     |         -         |    `Z` `C`    | Add A operand to B operand and store result in B operand                       |
|    `0x98`     |  `SADDB16`  |   Sequential add B 16    |         -         |    `Z` `C`    | Add A operand to B operand and store result in B operand (16 bit)              |
|    `0x99`     |   `SSUBA`   |  Sequential subtract A   |         -         |    `Z` `C`    | Subtract B operand from A operand and store result in A operand                |
|    `0x9a`     |  `SSUBA16`  | Sequential subtract A 16 |         -         |    `Z` `C`    | Subtract B operand from A operand and store result in A operand (16 bit)       |
|    `0x9b`     |   `SSUBB`   |  Sequential subtract B   |         -         |    `Z` `C`    | Subtract B operand from A operand and store result in B operand                |
|    `0x9c`     |  `SSUBB16`  | Sequential subtract B 16 |         -         |    `Z` `C`    | Subtract B operand from A operand and store result in B operand (16 bit)       |
|    `0x9d`     |   `SORA`    |     Sequential OR A      |         -         |      `Z`      | OR A operand with B operand and store result in A operand                      |
|    `0x9e`     |  `SORA16`   |    Sequential OR A 16    |         -         |      `Z`      | OR A operand with B operand and store result in A operand (16 bit)             |
|    `0x9f`     |   `SORB`    |     Sequential OR B      |         -         |      `Z`      | OR A operand with B operand and store result in B operand                      |
|    `0xa0`     |  `SORB16`   |    Sequential OR B 16    |         -         |      `Z`      | OR A operand with B operand and store result in B operand (16 bit)             |
|    `0xa1`     |  `SNANDB`   |    Sequential NAND A     |         -         |      `Z`      | NAND A operand with B operand and store result in A operand                    |
|    `0xa2`     | `SNANDB16`  |   Sequential NAND A 16   |         -         |      `Z`      | NAND A operand with B operand and store result in A operand (16 bit)           |
|    `0xa3`     |  `SNANDB`   |    Sequential NAND B     |         -         |      `Z`      | NAND A operand with B operand and store result in B operand                    |
|    `0xa4`     | `SNANDB16`  |   Sequential NAND B 16   |         -         |      `Z`      | NAND A operand with B operand and store result in B operand (16 bit)           |
|    `0xa5`     |   `SCMP`    |    Sequential compare    |         -         |    `Z` `C`    | Subtract B operand from A operand and discard result                           |
|    `0xa6`     |  `SCMP16`   |  Sequential compare 16   |         -         |    `Z` `C`    | Subtract B operand from A operand and discard result (16 bit)                  |
|    `0xa7`     |  `SSTOREA`  |    Sequential store A    |       `<s>`       |       -       | Store A operand in stack                                                       |
|    `0xa8`     |  `SSTOREA`  |    Sequential store A    |       `<h>`       |       -       | Store A operand in heap                                                        |
|    `0xa9`     |  `SSTOREA`  |    Sequential store A    |       `<g>`       |       -       | Store A operand in global variable                                             |
|    `0xaa`     | `SSTOREA16` |  Sequential store A 16   |       `<s>`       |       -       | Store A operand in stack (16 bit)                                              |
|    `0xab`     | `SSTOREA16` |  Sequential store A 16   |       `<h>`       |       -       | Store A operand in heap (16 bit)                                               |
|    `0xac`     | `SSTOREA16` |  Sequential store A 16   |       `<g>`       |       -       | Store A operand in global variable (16 bit)                                    |
|    `0xad`     |  `SSTOREB`  |    Sequential store B    |       `<s>`       |       -       | Store B operand in stack                                                       |
|    `0xae`     |  `SSTOREB`  |    Sequential store B    |       `<h>`       |       -       | Store B operand in heap                                                        |
|    `0xaf`     |  `SSTOREB`  |    Sequential store B    |       `<g>`       |       -       | Store B operand in global variable                                             |
|    `0xb0`     | `SSTOREB16` |  Sequential store B 16   |       `<s>`       |       -       | Store B operand in stack (16 bit)                                              |
|    `0xb1`     | `SSTOREB16` |  Sequential store B 16   |       `<h>`       |       -       | Store B operand in heap (16 bit)                                               |
|    `0xb2`     | `SSTOREB16` |  Sequential store B 16   |       `<g>`       |       -       | Store B operand in global variable (16 bit)                                    |
|    `0xb3`     |    `INC`    |        Increment         |       `<s>`       |    `Z` `C`    | Increment stack variable                                                       |
|    `0xb4`     |    `INC`    |        Increment         |       `<h>`       |    `Z` `C`    | Increment heap variable                                                        |
|    `0xb5`     |    `INC`    |        Increment         |       `<g>`       |    `Z` `C`    | Increment global variable                                                      |
|    `0xb6`     |   `INC16`   |       Increment 16       |       `<s>`       |    `Z` `C`    | Increment stack variable (16 bit)                                              |
|    `0xb7`     |   `INC16`   |       Increment 16       |       `<h>`       |    `Z` `C`    | Increment heap variable (16 bit)                                               |
|    `0xb8`     |   `INC16`   |       Increment 16       |       `<g>`       |    `Z` `C`    | Increment global variable (16 bit)                                             |
|    `0xb9`     |    `DEC`    |        Decrement         |       `<s>`       |    `Z` `C`    | Decrement stack variable                                                       |
|    `0xba`     |    `DEC`    |        Decrement         |       `<h>`       |    `Z` `C`    | Decrement heap variable                                                        |
|    `0xbb`     |    `DEC`    |        Decrement         |       `<g>`       |    `Z` `C`    | Decrement global variable                                                      |
|    `0xbc`     |   `DEC16`   |       Decrement 16       |       `<s>`       |    `Z` `C`    | Decrement stack variable (16 bit)                                              |
|    `0xbd`     |   `DEC16`   |       Decrement 16       |       `<h>`       |    `Z` `C`    | Decrement heap variable (16 bit)                                               |
|    `0xbe`     |   `DEC16`   |       Decrement 16       |       `<g>`       |    `Z` `C`    | Decrement global variable (16 bit)                                             |
|    `0xbf`     |   `PUSH`    |           Push           |       `<c>`       |       -       | Increase stack base pointer by constant                                        |
|    `0xc0`     |    `POP`    |           Pop            |       `<c>`       |       -       | Decrease stack base pointer by constant                                        |
|    `0xc1`     |    `JMP`    |           Jump           |       `<c>`       |       -       | Jump to constant address                                                       |
|    `0xc2`     |    `JIZ`    |       Jump if zero       |       `<c>`       |       -       | Jump to constant address if zero flag is set                                   |
|    `0xc3`     |    `JIC`    |      Jump if carry       |       `<c>`       |       -       | Jump to constant address if carry flag is set                                  |
|    `0xc4`     |    `JNZ`    |     Jump if not zero     |       `<c>`       |       -       | Jump to constant address if zero flag is not set                               |
|    `0xc5`     |    `JNC`    |    Jump if not carry     |       `<c>`       |       -       | Jump to constant address if carry flag is not set                              |
|    `0xc6`     |   `CALL`    |           Call           |       `<c>`       |       -       | Write return address to stack base and jump to constant address                |
|    `0xc7`     |   `CALL`    |           Call           |       `<s>`       |       -       | Write return address to stack base and jump to stack variable address          |
|    `0xc8`     |   `CALL`    |           Call           |       `<h>`       |       -       | Write return address to stack base and jump to heap variable address           |
|    `0xc9`     |   `CALL`    |           Call           |       `<g>`       |       -       | Write return address to stack base and jump to global variable address         |
|    `0xca`     |  `RETURN`   |          Return          |         -         |       -       | Jump to return address at stack base                                           |
|    `0xcb`     |   `ROMR`    |         ROM read         |    `<g>` `<s>`    |       -       | Read global ROM variable into stack variable                                   |
|    `0xcc`     |   `ROMR`    |         ROM read         |    `<g>` `<h>`    |       -       | Read global ROM variable into heap variable                                    |
|    `0xcd`     |   `ROMR`    |         ROM read         |    `<g>` `<g>`    |       -       | Read global ROM variable into global variable                                  |
|    `0xce`     |  `ROMR16`   |       ROM read 16        |    `<g>` `<s>`    |       -       | Read global ROM variable into stack variable (16 bit)                          |
|    `0xcf`     |  `ROMR16`   |       ROM read 16        |    `<g>` `<h>`    |       -       | Read global ROM variable into heap variable (16 bit)                           |
|    `0xd0`     |  `ROMR16`   |       ROM read 16        |    `<g>` `<g>`    |       -       | Read global ROM variable into global variable (16 bit)                         |
| `0xd1`-`0xeb` |      -      |            -             |         -         |       -       | Reserved                                                                       |
|    `0xec`     |  `INSTAT`   |       Input status       |       `<s>`       |       -       | Read input status into stack variable                                          |
|    `0xed`     |  `INSTAT`   |       Input status       |       `<h>`       |       -       | Read input status into heap variable                                           |
|    `0xee`     |  `INSTAT`   |       Input status       |       `<g>`       |       -       | Read input status into global variable                                         |
|    `0xef`     |    `IN`     |          Input           |       `<s>`       |       -       | Read input into stack variable                                                 |
|    `0xf0`     |    `IN`     |          Input           |       `<h>`       |       -       | Read input into heap variable                                                  |
|    `0xf1`     |    `IN`     |          Input           |       `<g>`       |       -       | Read input into global variable                                                |
|    `0xf2`     |    `CUR`    |          Cursor          |       `<c>`       |       -       | Set cursor to constant value                                                   |
|    `0xf3`     |    `CUR`    |          Cursor          |       `<s>`       |       -       | Set cursor to stack variable                                                   |
|    `0xf4`     |    `CUR`    |          Cursor          |       `<h>`       |       -       | Set cursor to heap variable                                                    |
|    `0xf5`     |    `CUR`    |          Cursor          |       `<g>`       |       -       | Set cursor to global variable                                                  |
|    `0xf6`     |    `OUT`    |          Output          |       `<c>`       |       -       | Write constant to output and increment cursor                                  |
|    `0xf7`     |    `OUT`    |          Output          |       `<s>`       |       -       | Write stack variable to output and increment cursor                            |
|    `0xf8`     |    `OUT`    |          Output          |       `<h>`       |       -       | Write heap variable to output and increment cursor                             |
|    `0xf9`     |    `OUT`    |          Output          |       `<g>`       |       -       | Write global variable to output and increment cursor                           |
|    `0xfa`     |   `DISP`    |         Display          |       `<c>`       |       -       | Write constant to display                                                      |
|    `0xfb`     |   `DISP`    |         Display          |       `<s>`       |       -       | Write stack variable to display                                                |
|    `0xfc`     |   `DISP`    |         Display          |       `<h>`       |       -       | Write heap variable to display                                                 |
|    `0xfd`     |   `DISP`    |         Display          |       `<g>`       |       -       | Write global variable to display                                               |
|    `0xfe`     |   `RESET`   |          Reset           |         -         |       -       | Reset system                                                                   |
|    `0xff`     |   `HALT`    |           Halt           |         -         |       -       | Halt system clock                                                              |
