# Design and Implementation of a Security CI/CD Pipeline for Multi-Architecture Container Images

1. Introduction to Microprocessors and Historical Background

### What is a microprocessor?

It is an integrated circuit that executes instructions stored in memory and performs arithmetic and logical operations by processing binary data. All the operations are executed through machine language instructions, and the microprocessor acts as the brain of a computer, controlling its operations. The physical structure is based on millions or billions of tiny transistors assembled on a semiconductor material to create the key components.

The main workflow that describes the processes of a CPU is the following. First, the instructions are fetched from memory. The instructions are then decoded, the requested operations being interpreted, and finally, the operations are executed and the results are stored in registers or computer memory [1], [2].

One of the first commercially available microprocessors was created in 1971, called Intel 4004, developed by Intel, and was able to process 4-bit data and perform logical and arithmetic operations. Over the decades, microprocessor architectures have evolved to support 8, 16, 32 and 64-bit processing, nowadays allowing microprocessors to perform increasingly complex operations [1], [2].

### Inside the Microprocessor Structure

Every microprocessor has a particular architecture that allows it to perform operations. In simple words, the process can be described as follows: the Control Unit (CU) takes the instructions from memory, interprets them and orchestrates the operations. Now that the operation instructions are clear, the operations are executed by the Arithmetic Logic Unit (ALU), which is responsible for calculations and logical operations orchestrated by the instructions received from the CU.

The input and output data used by the microprocessor can be temporarily stored in registers, offering high-speed access to data required for the operations. With the purpose of optimizing calculations and retrieving information faster, the processor uses cache memory to store frequently accessed instructions and data. Cache memory has a larger capacity than registers, but registers provide faster data access [3].

### RISC and CISC Architectures

As previously described, microprocessors shares a similar basic structure and follow a straightforward logic. However, over the years, different approaches have been developed regarding how instructions are defined and organized, based on similar fundamental components. In this way, different processor design approaches were introduced, with different ways of handling instructions. These architectures can achieve the same results, but using different sequences or types of instructions. The set of instructions and rules that defines how software interacts with a processor is described by the term Instruction Set Architecture (ISA). By definition, it represents the interface between software and hardware and defines the instructions, registers and other rules that software must follow to execute operations on a processor [4].

Follow this different aproches, two major arhitectures had a big impact on the modern computers: RISC and CISC.


# Bibliography:
- [1]: https://www.ibm.com/think/topics/microprocessor
- [2]: https://www.geeksforgeeks.org/electronics-engineering/introduction-of-microprocessor/
- [3]: https://conclusive.tech/glossary/what-is-a-microprocessor-architecture-and-types/
- [4]: https://conclusive.tech/glossary/what-is-risc-and-cisc-architecture-their-differences/