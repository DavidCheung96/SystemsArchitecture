# Computer Types
* Embedded Computers: are integrated into al larger device or system in order to automatically monitor or control it.
  - They are used for spesific purposes.
  - Typical applications *(Industrial, home automation, telecommunuciaton products)*
* Personal Computers: primarily for dedicated individual use.
  - Desktops computers, Workstation computers, Portable and Notebook computers.
* Servers *and* Enterprise Systems: are large computers that are meant to be shared by a potentially large number of users who access them  	from some personal computer over a network.
* Supercomputers *and* Grid Computers:
  - Most expansive and physically largest computers.
  - Mostly used for weather, engineering simuation and design
  - Grid computers provide a more cost-effective alternative. Which uses large number of personal computers and disk storage units in a high-speed network, called a grid, which is managed as a coordinated computing resouce.
  
# Functional Units
A computer consists of five functionally independent main parts:
- I/O
  - input
  - output
- momory
- Processor
  - arithmetic and logic    
  - control units

![onezero](images/onezero.png)
  
## Input Unit
Computers accept coded information through input units such as keyboards and things like that.
## Memory Unit
The function of the memory unit is to store programs and data.
1. __Primary Memory__
Also called *main memory*, is a fast memory that operates at electronic speeds. Programs must be stored in this memory while they are being executed. The memory consists of large number of storage cells, each capable of storing one bit of information and they work in group of fixed size called *words (typical word lengths are 16,32,64 bit)*. A memory in which any location can be accessed in a short and fixed amount of time after specifying its address is called a *random-access memory (RAM)*. The teime required to access one word is *memory access time*.
2. __Cache Memory__
Cache basically is a small and faster version of ram. Its used to hold sections of program that are currently executed.
3. __Second Storage__
The secondary storage can hold more data and keep them even after it turned off. *Exp= HDD, DVD, CD, USB*

## Arithmetic And Logic Unit
Most computer operations are executed in the *arithmetic and logic unit (ALU)* of the processor. Any arithmetic or logic operation is initiated by bringing the required operands into the processor, where the opration is performed by the *ALU*. Example: if two numbers located in the momery are to be added, they are brought into the processor, and the addition is carried out by the ALU. The sum may then be stored in the momory or retained in the processor for immediate use.
1. __Output Unit__
The output unit is the counterpart of the input unit. Basically it prints stuff.
2. __Control Unit__
The control unit carries the signals from one unit to another and senses their states. The control circuits are responsible for generating the *timing signals* that govern the transfers *(I/O Transfers, Data transfers between the processor and the memory)* and determine when a given action is to take place.

* The computer accepts information in the form of programs and data through an input unit and stores it in the momory.
* Information stored in the memory is fetched under program control into an arithmetic and logic unit, where it is processed.
* Processed information leaves the computer thourgh an output unit.
* All activities in the computer are directed by the control unit.

# Basic Operational Concepts
To perofrm a given task, an appropiate program consisting of a list of instructions is stored in the memory. Individual ınstructions a re brought from the memory into the processor, which executes the specifed operatins. Data to besed as instruction operands are also stored in the memory.

> Load R2, LOC

This instruction reads the contents of a memory location whose address is represented by the label *LOC* and loads them into processor register *R2*. The original contents of location *LOC* are preserved, whereas those of register *R2* are **overwritten**. Steps of executing this instruction.
1. The operation to be performed is determined by the *control unit.*
2. The operand at *LOC* is then fetched from the memory into the processor.
3. The operand is stored in register *R2*

After operands have been loaded from memory into processor registers youcen perform operations on them.

> Add R4, R2, R3

adds the contents of registers R2 and R3, then places their sum into register *R4*. The operands in *R2* and *R3* are not altered, but the previous value in *R4* is **overwritten** by the sum.

After completing desired operations we need to transfer it to the memory using.

> Store R4, LOC

This instruction copies the operand in register *R4* to memory location LOC. The original contents of location *LOC* are **overwritten**, but those of *R4* are preserved.

![oneone](images/oneone.png)

In addition to the *ALU* and the *control circuitry*, the processor contains a number of registers used for several different purposes. The *instruction register (IR)* holds the instruction that is currently being executed. The *program counter (PC)* is another specialized register. It contains the memory address of the next instruction to be fetched and executed. During the execution of an instruction, the contents of the *PC* are updated to correspond to the addres of the next instruciton to be executed.

### Details
If a word is to be read from the memory, the interface sends the address of that word to the memory along with a Read control       signal. The interface waits for the word to be retrieved, then transfers it to the appropriate processor register. If a word is to       be written into memory, the interface transfers both the address and the word to the memory along with a write control signal. </li>
* **Operating Steps**
    1. A program must be in the main memory in order for it to be executed (It is often transferred there from secondary storage thorught the input unit)
    2. Execution of the program begins when the PC is set to point to the first instruction of the program. The contents of the PC are transferred to the memory along with a Read control signal
    3. When the addressed word has been fetched from the memory it is loaded into register IR. At this point, the instruciton is ready to be interpreted and executed.   
    
In some cases to respond immediately, execution of the current program must be suspended. To cause this, the device raises an *interrupt* signal, which is a request for service by the processor The processor provides the requested service by executing a program called an *interrupt-service routine*. The processor saves its current state to the memory so that it can continue after the *interrupt-service routine* is completed.

# Number Representation And Arithmetic Operations
The most natural way to represent a number in a computer system is by a string of bits,
called a binary number.

![onetwo](images/onetwo.png)

## Integers
Consider an *b*-bit vector
> B = bn−1 ... b1b0

















