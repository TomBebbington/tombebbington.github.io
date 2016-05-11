---
published: false
title: "Stored Program Concept & the Fetch-Execute Cycle"
---
# Fetch-Execute Cycle

1. Fetch: the processor retrieves the next instruction from memory.
2. Decode: the processor decodes the opcode and operands from the instruction.
3. Execute: the processor runs the instruction.

# CPU Components

## Units

## The Arithmetic Logic Unit

This handles mathematical and logical operations such as:
+ Addition
+ Subtraction
+ Comparisons

## The Control Unit

This acts as the supervisor of the **Fetch-Execute Cycle**, and ensures that data is stored into the correct locations.

## Registers

**Registers** are small areas to store and sort data on the CPU no matter the architecture.

## Other components

+ The **Program Counter** (PC) counts which instructions have been executed and which is next - this information is passed to the **Control Unit**.
+ The **Cache** is a bit of really fast memory, that instructions and data are loaded into from RAM before being ran on the CPU. This a form of volatile memory.
+ The **Bus** is a pathway between CPU components. Data and control signals travel through the bus inside th CPU to the different components.

# Architectures

## Von Neumann
This is where the instructions and data are saved in the same part of the memory.

