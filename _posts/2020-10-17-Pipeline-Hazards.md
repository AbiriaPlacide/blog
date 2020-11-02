---
title: Pipeline Hazards
tags: Computer-architecture
---

Terminology used:

	5 Stage pipeline

	IF  - Instruction fetch

	ID  - Instruction decode

	Ex  - Execute

	MEM - Memory access

	WB  - Memory write-back


#### Three Pipeline Hazards
	1. Structural Hazards - resource conflics where two different instructions try to access the same hardware

	2. Data Hazards - data dependancy where results are needed before they are ready

	3. Control Hazards - instructions such as jump or branch that change the program counter

#### Structural Hazards
With a 5-stage pipeline there are no structural hazards. But an example is two instructions attempting to use the ALU at the same time.

#### Three Data Hazards
	Consider two instructions A and B, where A occurs before B, and where both are  using register: Reg.

	1. Read after write  (RAW) -> B reads Reg before A writes to Reg

	2. Write after read  (WAR) -> A reads Reg before B write to Reg

	3. Write after write(WAW) -> A writes to Reg after B writes to Reg

Due to pipelining, the order in which instructions are processed is not sequencial as it would be in an unpipelined processor.
This means that a register may read an instruction before it is updated by the previous instruction running in parallel.

Some ways of handling hazards includes avoiding them or stalling the pipeline until the required information is updated.

Stalling is necessary when the an instruction has to wait for an earlier instruction to finish.

#### Minimizing Data Hazard Stalls
<b>Data forwarding </b> is a way for pipelined CPUs to limit effects on performance due to pipeline stalls.

Reordering code is another way to avoid stalling. This method is often used by modern compilers. 

#### Control Hazards

Flow of control in a program is determined by the branch instruction. The next instruction is determined by the results of the
branch. The issue is that the pipeline can't always fetch the correct instruction 

The basic way of handing control hazards is to stall. That is to wait for the results of a branch instruction before fetching the next instruction

Another method is to assume the branch is always not taken. if it happens to be taken ( this is determined in the EX stage ), the pipeline is flushed and the correct path is taken. 

You can also assume the branch is always taken.
