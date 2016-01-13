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
 warnings, libraries, and debugging levels) for each toolchain component:
	+ GCC Compiler
	+ GDB Debugger
	+ GAS assembler
	+ Size binutils utility, etc.
* Support for Synopsys EM Starter Kit and AXS10x.
* Configuration of debug and run configurations for supported FPGA Development
 Systems and debug probes (Digilent HS1/HS2 or Ashling Opella-XD).
* GDB-based debugging using **Debug** perspective providing detailed debug
 information (including breakpoints, variables, registers, and disassembly)

> Before you begin, refer to the EM Starter Kit
> guide and follow the instructions on how to connect EM Starter Kit to
> your PC. This is required for the Eclipse IDE GDB debugger to successfully
> download and debug programs on the target.

ARC GNU IDE 2015.12 supports following components:

* Eclipse version 4.5 "Mars"
* CDT version 8.8
* OpenOCD release 2015.12
* [ARC GNU Toolchain release 2015.12](https://github.com/foss-for-synopsys-dwc-arc-processors/toolchain/releases/tag/arc-2015.12).


Table of Contents
-----------------

* [Installation](Installation)
* [Getting Started with EM Starter Kit](Getting-Started-with-EM-Starter-Kit)
* [Getting Started with nSIM](Getting-Started-with-nSIM)
* [User Guide](User-Guide)

