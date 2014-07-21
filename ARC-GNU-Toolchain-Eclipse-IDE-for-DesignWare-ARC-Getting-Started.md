TOC
===

* [Installation](Installation)
* [Debugging with nSIM](Debugging-with-nSIM)
* [Building and Debugging Linux uClibc applications]
  (Building-and-Debugging-Linux-uClibc-applications.md)
* [Debugging a big-endian application on EM Starter Kit]
  (Debugging-a-big-endian-Application-on-EM-Starter-Kit)


# Introduction

The ARC GNU Eclipse IDE consists of the Eclipse IDE combined with an Eclipse CDT Managed Build Extension plug-in for the ARC GNU Toolchain and GDB embedded debugger plug-in for ARC, based on the Zylin Embedded CDT plug-in. 
The ARC GNU IDE supports the development of managed C/C++ applications for ARC processors using the ARC GNU toolchain for bare metal applications (elf32).  

The ARC GNU IDE provides support for the following functionality: 
* 	Support for Windows 7, Ubuntu Linux 12.04 LTS and RedHat Enterprise Linux 6.0 Development Host Systems
* 	Support for the ARC EM and HS Processors
*	Support for little and big endian configurations
* 	Ability to create C/C++ projects using the ARC elf32 cross-compilation toolchain
* 	Configuration of toolchain parameters per project
* 	Configuration of individual options (such as preprocessor, optimization, warnings, libraries, and debugging levels) for each toolchain component:
	* arc-elf32-gcc
	* arc-elf32-gdb
	* arc-elf32-as
	* arc-elf32-size
* 	Configuration of debug and run configurations for EM Starter Kit using OpenOCD. 
* 	Configuration of debug and run configurations for supported FPGA Development Systems and debug probes (Digilent HS1 or Ashling Opella-XD).
* 	GDB-based debugging using  **Debug**  perspective providing detailed debug information (including breakpoints, variables, registers, and disassembly)

Note: Before you begin, refer to the EM Starter Kit and ARC GDB Getting Started guide and follow the instructions on how to connect the EM Starter Kit to your PC.  This is required for the Eclipse IDE GDB debugger to successfully download and debug programs on the target.


# Building a C Project
## Step 1: Creating a New C Project
1. Select **File >New >C Project** 
    ![Creating a new C project](images/Creating a new C project.png)

    _Creating a new C project_ 

    The **C Project** dialog has two ARC project types:  **ARC Cross ELF32 Target Application** and **ARC Cross ELF32 Target Static Library**.   
    Please note that different project types have different Tool Setting properties and different default options
2. Enter a project name

   ![C Project Creation Dialog](images/C Project Creation Dialog.png)

   _C Project Creation Dialog_ 

   1. Select **Hello World ARC C Project** under **ARC Cross ELF32 Target Application**.   
The Hello ARC project is an example project that comes with the EM Starter Kit Software and uses the UART on the EM Starter Kit to display output.  Refer to the EM Starter Kit Getting Started for instructions on how to connect to the UART on the EM Starter Kit board using the Serial Terminal plugin.
    2. Select the little endian toolchain from **Toolchains** Pane ( EM Starter Kit configurations are little endian)
    3. Click the **Next** button.

3. You can also fill in additional information for a project. Afterwards, click the **Next** button
    ![C project creation - Additional information Dialog](images/C project creation - Additional information Dialog.png)

    _C project creation - Additional information Dialog_ 
4. Select the desired configuration and click **Finish**
    ![C Project creation – Configurations Dialog](images/C Project creation – Configurations Dialog.png)

    _C Project creation – Configurations Dialog_ 

The resulting Hello ARC project created in Eclipse is shown in Figure 5.  

![Final Hello ARC Project in Eclipse ](images/Final Hello ARC Project in Eclipse.png)

_Final Hello ARC Project in Eclipse_ 

File changes could be required depending on version of EM Starter Kit. Users of EM Starter Kit version 1.1 should update file starterkit.h with new values of core and peripherals frequencies. Redefine CPU_CLOCK to 30000000 and PERIPHERAL_CLOCK to 50000000. Resulting file is in shown in Figure 6.

![File starterkit.h updated for EM Starter Kit 1.1](images/File starterkit.h updated for EM Starter Kit 1.1.png)

_File starterkit.h updated for EM Starter Kit 1.1_ 


## Step 2: Configuring the ARC GNU Toolchain
Follow the steps below to configure the ARC GNU toolchain:

1. Right click on the Hello ARC project and select **Properties** from the pop-up menu:

    ![Configuring the toolchain for the project](images/Configuring the toolchain for the project.png)

    _Configuring the toolchain for the project_ 

2. Select desired options for each tool under the Tool Settings tab:

    ![Toolchain Configuration](images/Toolchain Configuration.png)

    _Toolchain Configuration_ 

    Various options can be selected for the compiler, assembler and linker components of the toolchain as desired.  

    Once the configuration options have been selected, click **Apply** and then **OK** to save the toolchain configuration. 
 
## Step 3: Building a Project

1. Right click on the _Hello ARC project_ and select **Build Project** from the pop-up menu

    ![Building a Project](images/Building a Project.png)

    _Building a Project_ 

2. Review the build output log in the Eclipse console tab to confirm success:

    ![Build Output](images/Build Output.png)

    _Build Output_ 

#  Debugging with OpenOCD

## Step 1: Creating a Debug Configuration for the C Project

Once the C Project is successfully compiled by ARC GCC, you can debug the resulting executable on the EM Starter Kit board. 

To debug the project, create a new debug configuration using _arc-elf32-gdb_. 

1. Select **Debug Configurations**  from the  **Run**  menu or by clicking on the down arrow next to the bug icon: 

    ![Debug Configurations](images/Debug Configurations.png)

    _Debug Configurations_ 

2. Double click on the **ARC C/C++ Application**  or click on the top left icon to create a new debug configuration for the project:

    ![ARC Embedded Debug Configurations](images/ARC Embedded Debug Configurations.png)

    _ARC Embedded Debug Configurations_ 

3. Select a name for the new debug configuration (by default, it equals the project name followed by “Debug”).

    ![New debug Configuration](images/New debug Configuration.png)

    _New debug Configuration_ 

4. Click the **Debugger** tab.

    ![Default values in the Debugger tab for JTAG via OpenOCD](images/Default values in the Debugger tab for JTAG via OpenOCD.png)

    _Default values in the Debugger tab for JTAG via OpenOCD_ 

    ![Default values in the GDBserver Debugger Options tab](images/Default values in the GDBserver Debugger Options tab.png)

    _Default values in the GDBserver Debugger Options tab_ 


    Select the **JTAG via OpenOCD** or **JTAG via Ashling** for use with EM Starter Kit. Select the **nSIM** for use simulator without hardware be connected.  

    The “**COM Ports**” **picklist** shows the value for Digilent USB Serial Port from the Windows registry. You can modify the value as desired, but the selection must match the port number in Device and Printers as shown in below.

    ![Digilent USB Serial COM Port](images/Digilent USB Serial COM Port.png)

    _Digilent USB Serial COM Port_ 

    ![USB Serial COM Port](images/USB Serial COM Port.png)

    _USB Serial COM Port_ 

5. Click the **Commands** tab.

    ![Default values in the Commands tab](images/Default values in the Commands tab.png)

    _Default values in the Commands tab_ 

    The default **“Initialize”** and **“Run”** commands is null, you can use them directly, or modify the list as desired. 
   
6. Click the **Debug **button in the **Debug configurations** dialog to initiate debug session. 

    This action automatically launches the Serial terminal and OpenOCD applications in the background and   connects to the UART on the EM Starter Kit board. After checking the “Allocate console (necessary for input)" in **Common Tab**, OpenOCD startup log messages will appear in the console. 

    ![Check “Allocate console” in Common Tab](images/Check “Allocate console” in Common Tab.png)

    _Check “Allocate console” in Common Tab_ 

7. Click **Yes** in the confirmation dialog to switch to the Debug perspective

    ![Perspective Switch](images/Perspective Switch.png)

    _Perspective Switch_ 

    ![Launch of OpenOCD](images/Launch of OpenOCD.png)

    _Launch of OpenOCD_ 

    ![Launch of Serial terminal](images/Launch of Serial terminal.png)

    _Launch of Serial terminal_ 

8. Click the **Debug** button in the **Debug configurations** dialog to initiate the debug session:

    ![Debugging Process](images/Debugging Process.png)

    _Debugging Process_ 

## Step 2: Debugging an Application
The **Debug** perspective provides an integrated debug environment with individual windows to display various debugging data such as the debug stack, variables, registers  breakpoints, etc. 

![Debug Perspective](images/Debug Perspective.png)

_Debug Perspective_ 

1. To set a breakpoint, place your cursor on the marker bar along the left edge of the editor window on the line where you want the breakpoint:

    ![Source File Window in Debug Perspective with Breakpoint Set](images/Source File Window in Debug Perspective with Breakpoint Set.png)

    _Source File Window in Debug Perspective with Breakpoint Set_ 

2. Examine Variables, Breakpoints, Expressions or Registers from different tabs of the same debug perspective: 

    ![Registers Window in Debug Perspective](images/Registers Window in Debug Perspective.png)

    _Registers Window in Debug Perspective_ 

3. Examine the debug Views showing the debugger in use:

    ![Debug Window in Debug Perspective](images/Debug Window in Debug Perspective.png)

    _Debug Window in Debug Perspective_ 

    ![Hello ARC Debug Console in Debug Perspective](images/Hello ARC Debug Console in Debug Perspective.png)

    _Hello ARC Debug Console in Debug Perspective_ 

4. Switch Console tabs to view OpenOCD **Console** output:  

    ![Multiple Consoles in the Debug Perspective](images/Multiple Consoles in the Debug Perspective.png)

    _Multiple Consoles in the Debug Perspective_ 

    ![Hello ARC Debug Console Output](images/Hello ARC Debug Console Output.png)

    _Hello ARC Debug Console Output_ 

    ![OpenOCD Console Output](images/OpenOCD Console Output.png)

    _OpenOCD Console Output_ 

5. Step through each line by using F5 (step into), and F6 (step over). 

    ![Stepping Toolbar](images/Stepping Toolbar.png)

    _Stepping Toolbar_ 

6. Toggle breakpoint at the last line of main(), which is "}" , and then clicking Resume or pressing F8.

    ![Click Resume or Press F8](images/Click Resume or Press F8.png)

    _Click Resume or Press F8_ 

    ![Final Output Printed to Serial Terminal Window through UART](images/Final Output Printed to Serial Terminal Window through UART.png)

    _Final Output Printed to Serial Terminal Window through UART_ 
 
7. Terminate all external tools before you quit current debugging process.

    ![Consoles for child processes](images/Consoles for child processes.png)

    _Consoles for child processes_ 

