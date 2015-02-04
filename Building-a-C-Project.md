Creating a New C Project
------------------------

1. Select **File >New >C Project**
    ![Creating a new C project](images/Creating a new C project.png)

    _Creating a new C project_

    The **C Project** dialog has two ARC project types:  **ARC Cross ELF32 Target Application** and **ARC Cross ELF32 Target Static Library**.
    Please note that different project types have different Tool Setting properties and different default options, and if you don't see some toolchain in the list, then you should check PATH contents.
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

The resulting Hello ARC project created in Eclipse is:

![Final Hello ARC Project in Eclipse ](images/Final Hello ARC Project in Eclipse.png)

_Final Hello ARC Project in Eclipse_

File changes could be required depending on version of EM Starter Kit. Users of EM Starter Kit version 1.1 should update file starterkit.h with new values of core and peripherals frequencies. Redefine CPU_CLOCK to 30000000 and PERIPHERAL_CLOCK to 50000000.

![File starterkit.h updated for EM Starter Kit 1.1](images/File starterkit.h updated for EM Starter Kit 1.1.png)

_File starterkit.h updated for EM Starter Kit 1.1_


Configuring the ARC GNU Toolchain
---------------------------------

Follow the steps below to configure the ARC GNU toolchain:

1. Right click on the Hello ARC project and select **Properties** from the pop-up menu:

    ![Configuring the toolchain for the project](images/Configuring the toolchain for the project.png)

    _Configuring the toolchain for the project_

2. Select desired options for each tool under the Tool Settings tab:

    ![Toolchain Configuration](images/Toolchain Configuration.png)

    _Toolchain Configuration_

    Various options can be selected for the compiler, assembler and linker components of the toolchain as desired.

    Once the configuration options have been selected, click **Apply** and then **OK** to save the toolchain configuration.


Building a Project
------------------

1. Right click on the _Hello ARC project_ and select **Build Project** from the pop-up menu

    ![Building a Project](images/Building a Project.png)

    _Building a Project_

2. Review the build output log in the Eclipse console tab to confirm success:

    ![Build Output](images/Build Output.png)

    _Build Output_