# Design and Implementation of a Security CI/CD Pipeline for Multi-Architecture Container Images

## Chapter 1. Introduction to Microprocessors and Historical Background

### 1.1 What is a microprocessor?

It is an integrated circuit that executes instructions stored in memory and performs arithmetic and logical operations by processing binary data. All the operations are executed through machine language instructions, and the microprocessor acts as the brain of a computer, controlling its operations. The physical structure is based on millions or billions of tiny transistors assembled on a semiconductor material to create the key components.

The main workflow that describes the processes of a CPU is the following. First, the instructions are fetched from memory. The instructions are then decoded, the requested operations being interpreted, and finally, the operations are executed and the results are stored in registers or computer memory [1], [2].

One of the first commercially available microprocessors was created in 1971, called Intel 4004, developed by Intel, and was able to process 4-bit data and perform logical and arithmetic operations. Over the decades, microprocessor architectures have evolved to support 8, 16, 32 and 64-bit processing, nowadays allowing microprocessors to perform increasingly complex operations [1], [2].

### 1.2 Inside the Microprocessor Structure

Every microprocessor has a particular architecture that allows it to perform operations. In simple words, the process can be described as follows: the Control Unit (CU) takes the instructions from memory, interprets them and orchestrates the operations. Now that the operation instructions are clear, the operations are executed by the Arithmetic Logic Unit (ALU), which is responsible for calculations and logical operations orchestrated by the instructions received from the CU.

The input and output data used by the microprocessor can be temporarily stored in registers, offering high-speed access to data required for the operations. With the purpose of optimizing calculations and retrieving information faster, the processor uses cache memory to store frequently accessed instructions and data. Cache memory has a larger capacity than registers, but registers provide faster data access [3].

### 1.3 RISC and CISC Instruction Sets

As previously described, microprocessors shares a similar basic structure and follow a straightforward logic. However, over the years, different approaches have been developed regarding how instructions are defined and organized, based on similar fundamental components. In this way, different processor design approaches were introduced, with different ways of handling instructions. These architectures can achieve the same results, but using different sequences or types of instructions. The set of instructions and rules that defines how software interacts with a processor is described by the term Instruction Set Architecture (ISA). By definition, it represents the interface between software and hardware and defines the instructions, registers and other rules that software must follow to execute operations on a processor [4].

Following these different approaches, two major **instruction set design** approaches have had a significant impact on modern computers: Reduced Instruction Set Computer (RISC) and Complex Instruction Set Computer (CISC). The main difference between these two approaches is the way their instruction sets are designed. RISC architectures use a set of relatively simple and more straightforward instructions, which are designed to be decoded and executed efficiently. On the other hand, CISC is an approach that supports a wider variety of instructions, including more complex operations, where a single instruction can perform multiple internal operations, potentially requiring more time to execute. However, this does not necessarily mean that CISC processors are slower. These two approaches bring advantages and disadvantages, depending on the final product or system they are designed for [4],[5].

### 1.4 Advantages and Disadvantages of RISC and CISC

Depending on the purpose of the processor, both approaches have advantages and disadvantages. RISC architectures use simpler and more regular instructions, making the decoding process less complex and allowing an efficient execution of instructions. However, some tasks may require a larger number of instructions to achieve the same result, which can increase the program size. On the other hand, CISC architectures can perform more complex operations using fewer instructions, potentially reducing the program size and the number of instructions required for a task. The main disadvantage is the more complex instruction decoding process, which can require additional hardware resources. In terms of performance and power consumption, neither approach is automatically better than the other, as these characteristics depend on the processor's internal design and implementation.

### 1.5 Advantages and Disadvantages of RISC and CISC Architectures

The advantages and disadvantages of these two approaches can be compared based on hardware complexity, program size and resource usage. RISC architectures generally benefit from simpler instruction decoding, which can reduce hardware complexity. However, certain tasks may require more instructions, potentially increasing the program size. In comparison, CISC architectures can achieve better code density by performing certain operations using fewer instructions, but this comes with a more complex decoding process and potentially higher hardware requirements.

In terms of performance, RISC can benefit from simpler and more efficient instruction decoding, but executing more instructions for certain tasks may increase processing work. On the other hand, CISC can reduce the number of instructions and improve instruction cache usage through more compact code, but complex instructions may require additional decoding resources and internal operations. Neither approach guarantees faster execution or lower power consumption, as these characteristics also depend on the processor's clock speed, cache efficiency, internal optimizations and the type of workload being executed [6],[7].

### 1.6 Evolution to the modern 64-bits arhitectures

In respect to the historical timeline, the first computers were developed using complex instruction sets, later associated with the CISC approach. Over the following years, Intel introduced one of the first commercial microprocessors, the Intel 4004, capable of processing 4-bit data. As technology evolved, researchers started exploring different ways of designing processors, introducing the RISC approach, based on simpler and more regular instructions.

Following these developments, two important processor families emerged. Intel developed the x86 architecture, based on CISC principles, while AMD later introduced its 64-bit extension, known as AMD64. On the other hand, the ARM architecture was developed following RISC principles, initially focusing on efficient processing and low power consumption. Over time, ARM also evolved to support 64-bit computing, introducing ARM64.

Nowadays, AMD64 and ARM64 are widely used in modern computers, servers and cloud environments. Although both can perform similar tasks, they use different instruction sets, which influence software compatibility, execution and certain aspects of system security.

## Chapter 2. AMD64 and ARM64 Architectures

As previous mentioned, AMD64 and ARM64 arhitectures, each one following different ISA set of instructions, shaped the nowadays computing industry. 
---
[1]: https://www.ibm.com/think/topics/microprocessor
[2]: https://www.geeksforgeeks.org/electronics-engineering/introduction-of-microprocessor/
[3]: https://conclusive.tech/glossary/what-is-a-microprocessor-architecture-and-types/
[4]: https://conclusive.tech/glossary/what-is-risc-and-cisc-architecture-their-differences/
[5]: https://www.ibm.com/history/risc
[6]: Arm Limited. What Is RISC? https://www.arm.com/glossary/risc
[7]: https://cs.stanford.edu/people/eroberts/courses/soco/projects/risc/risccisc/
