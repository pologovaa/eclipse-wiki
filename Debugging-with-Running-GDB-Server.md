
It is expected here that you have already built your application and created a
 debug configuration for it. About how to do it you can read on the following
pages:
* [Building an Application](Building-User-Guide)
* [Creating a Debug Configuration](Creating-a-Debug-Configuration)


### Running GDB server properties

![Connect to running GDB server tab](images/debugging/running_gdb/running_gdb_tab.png)
_Connect to running GDB server tab_

If you want to connect to a GDB server that is already running, you should choose
a host address and also specify commands to be passed to the GDB client on the
**Commands** tab.

![Commands tab](images/debugging/commands_tab.png)
_Commands tab_


### OpenOCD as running GDB server

If you have a running OpenOCD server, you can connect to it just by choosing
**Connect to running GDB Server** under **ARC GDB Server** on **Debugger**
 tab and specifying port number and host address on which your OpenOCD is
 running. You do not need to specify any initialize commands for GDB in
 **Commands tab**, it will connect to OpenOCD using host address and port number
 from **Debugger** tab.

![Debugging using running GDB server](images/debugging/running_gdb/running_gdb_debug.png)

 _Debugging using running GDB server_

![Debug window](images/debugging/running_gdb/processes_list.png)

  _Debug window_

![OpenOCD output in console](images/debugging/running_gdb/openocd_output.png)

  _OpenOCD output in console_
