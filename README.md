# mimac16

## What is this?

_mimac16_ is a simple 16-bit computer architecture inspired by [Ben Eater's 8-bit computer](https://eater.net/8bit). It contains an arithmetic unit (addition and subtraction) as well as a separate logic unit (ORing and NANDing). A dedicated 16-bit stack base pointer register serves as a base offset to memory fetches and stores. The instruction set describes 256 instructions optimized for compiled high-level languages.

This repository contains documentation regarding the architecture itself.  
Code for flashing the EEPROM with microcode can be found in the [mimac16-microcode](https://github.com/Mirrrek/mimac16-microcode) repository.  
Code for an emulator written in TypeScript can be found in the [mimac16-emulator](https://github.com/Mirrrek/mimac16-emulator) repository.  
The architecture is designed to execute the [Nitrogen](https://github.com/Mirrrek/nitrogen) programming language.

## Table of Contents

This repository contains the following documentation:

| File                                         | Description                                                           |
| :------------------------------------------- | :-------------------------------------------------------------------- |
| [`sectors.md`](./sectors.md)                 | Description of all the hardware sectors present on the processor      |
| [`control-logic.md`](./control-logic.md)     | Description of the control logic inputs and outputs, including flags  |
| [`instruction-set.md`](./instruction-set.md) | Description of the instruction set and details about each instruction |
