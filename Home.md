Introduction
------------

The ARC GNU Eclipse IDE consists of the Eclipse IDE combined with an Eclipse
CDT Managed Build Extension plug-in for the ARC GNU Toolchain and GDB embedded
debugger plug-in for ARC, based on the Zylin Embedded CDT plug-in.  The ARC GNU
IDE supports the development of managed C/C++ applications for ARC processors
using the ARC GNU toolchain for bare metal applications (elf32).

The ARC GNU IDE provides support for the following functionality:

* Support for Windows 7, Ubuntu Linux 14.04 LTS and RedHat Enterprise Linux 6
Development Host Systems
* Support for the ARC EM, ARC HS, ARC 600 and ARC 700 Processors
* Support for little and big endian configurations
* Ability to create C/C++ projects using the ARC elf32 cross-compilation
 toolchain
* Configuration of toolchain parameters per project
* Configuration of individual options (such as preprocessor, optimization,
* warnings, libraries, and debugging levels) for each toolchain component:
	+ GCC Compiler
	+ GDB Debugger
	+ GAS assembler
	+ Size binutils utility, etc.
* Configuration of debug and run configurations for EM Starter Kit and AXS10x
 using OpenOCD.
* Configuration of debug and run configurations for supported FPGA Development
 Systems and debug probes (Digilent HS1/HS2 or Ashling Opella-XD).
* GDB-based debugging using **Debug** perspective providing detailed debug
 information (including breakpoints, variables, registers, and disassembly)

> Before you begin, refer to the EM Starter Kit and ARC GDB Getting Started
> guide and follow the instructions on how to connect the EM Starter Kit to
> your PC. This is required for the Eclipse IDE GDB debugger to successfully
> download and debug programs on the target.


Table of Contents
-----------------

* [Installation](Installation)
* [Building a C Project](Building-a-C-Project)
* [Debugging with OpenOCD](Debugging-with-OpenOCD)
* [Debugging with nSIM](Debugging-with-nSIM)
* [Building and Debugging Linux uClibc applications]
  (Building-and-Debugging-Linux-uClibc-applications)
* [Debugging a big-endian application on EM Starter Kit]
  (Debugging-a-big-endian-Application-on-EM-Starter-Kit)

