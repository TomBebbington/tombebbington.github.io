---
published: true
title: "Stored Program Concept & the Fetch-Execute Cycle"
category: computing
---
# Fetch-Execute Cycle

1. Fetch: the processor retrieves the next instruction from memory.
2. Decode: the processor decodes the opcode and operands from the instruction.
3. Execute: the processor runs the instruction.

## Fetch
The value at PC is the address of the next instruction.

1. This is sent through the address bus to main memory.
2. The contents of the memory location at the address are sent through the data bus to the CIR.
3. The value at **PC** is incremented.
4. Address details are loaded into the **MAR** then later copied to the **MBR**.

## Decode

The processor reads the instruction held in the **CIR** and decides how to handle it from the instruction set.

## Execute

The processor handles the instruction using its instruction set to decide what each instruction does.

# CPU Components

## Units

## The Arithmetic Logic Unit

This handles mathematical and logical operations such as:

+ Addition
+ Subtraction
+ Comparisons (less / greater than / or equal to)

## The Control Unit

This acts as the supervisor of the **Fetch-Execute Cycle**, and ensures that data is stored into the correct locations at the correct time.

## Cache
The **Cache** is a bit of really fast memory, that instructions and data are loaded into from RAM before being ran on the CPU. This a form of volatile memory.

## Bus
The **Bus** is a pathway between CPU components. Data and control signals travel through the bus inside th CPU to the different components.

## Clock
This generates a signal in order to synchronise the operations of the computer to a specific frequency, measured in *Hertz*.

## Registers

**Registers** are small areas of memory to store and sort data on the CPU that are usually 32 or 64-bit.

### Current Instruction Register
The **CIR** holds the instruction that is being executed by the processor.

### Program Counter
The **PC** register counts which instructions have been executed and which is next - this information is passed to the **Control Unit**.

### Status Register
The **SR** tracks the status of different parts of the computer.
### Memory Buffer Register
The **MBR** holds data that is about to be written or has been read from memory.
### Memory Address Register
The **MAR** stores the memory location that the **MBR** data is about to be written to or read from.

# Architectures

## Von Neumann
This is where the instructions and data are saved in the same part of the memory.

