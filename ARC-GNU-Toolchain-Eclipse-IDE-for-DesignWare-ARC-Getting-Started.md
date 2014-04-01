# Introduction

The ARC GNU Eclipse IDE consists of the Eclipse IDE combined with an Eclipse CDT Managed Build Extension plug-in for the ARC GNU Toolchain and GDB embedded debugger plug-in for ARC, based on the Zylin Embedded CDT plug-in. 
The ARC GNU IDE supports the development of managed C/C++ applications for ARC processors using the ARC GNU toolchain for bare metal applications (elf32).  

The ARC GNU IDE provides support for the following functionality: 
* 	Support for Windows Development Host Systems
* 	Support for the ARC EM Processor development target
* 	Ability to create C/C++ projects using the ARC elf32 cross-compilation toolchain
* 	Configuration of toolchain parameters per project
* 	Configuration of individual options (such as preprocessor, optimization, warnings, libraries, and debugging levels) for each toolchain component:
	* arc-elf32-gcc
	* arc-elf32-gdb
	* arc-elf32-as
	* arc-elf32-size
* 	Configuration of debug and run configurations for EM Starter Kit using OpenOCD. 
* 	Configuration of debug and run configurations for supported FPGA Development Systems and debug probes (Digilent HS1 or Ashling Opella-XD).
* 	GDB-based debugging using **Debug **perspective providing detailed debug information (including breakpoints, variables, registers, and disassembly)

Note: Before you begin, refer to the EM Starter Kit and ARC GDB Getting Started guide and follow the instructions on how to connect the EM Starter Kit to your PC.  This is required for the Eclipse IDE GDB debugger to successfully download and debug programs on the target.

# Installation
## Prerequisites
ARC GNU plugins for Eclipse have following requirements to the system:
* 	Eclipse version 4.3 (Kepler)
* 	CDT version 8.2.1
* 	OS: RHEL 6 or Windows 7
* 	On Linux both 32bit and 64-bit versions of Eclipse are supported, on Windows only 32-bit Eclipse installations are supported.  Eclipse 64-bit installation is not supported, so it is required to run 32-bit version of Eclipse on 64-bit Windows versions, to overcome this limitation.
* 	Java VM version >= 1.6 is required
## 2.1 Downloading latest plugins
User can get this plug-in from website URL https://github.com/foss-for-synopsys-dwc-arc-processors/arc_gnu_eclipse/releases, this is an archived version of the GNU ARC Eclipse plug-in update site, the file name is arc_gnu_plugins.zip

To run ARC_GNU_IDE plugins, you need to install Target Terminal plugin. The url for Kepler’s update site is http://download.eclipse.org/releases/kepler
***
, then select: Mobile and Device Development, especially Target Management Terminal which is "An ANSI (vt102) compatible Terminal including plug-ins for Serial, SSH and Telnet connections."
