
It is expected here that you have already built your application and created a
 debug configuration for it. About how to do it you can read on the following
pages:
* [Building an Application](Building-User-Guide)
* [Creating a Debug Configuration](Creating-a-Debug-Configuration)

### Specifying custom GDB server properties

![Custom GDB Server tab](images/debugging/custom_gdb/custom_gdb_tab.png)
_Custom GDB Server tab_

You can use some other GDB server. In that case you should specify a path to
this server executable file, its command-line arguments and also commands to
be passed to the GDB client. These are on the **Commands** tab of the dialog.

![Commands tab](images/debugging/commands_tab.png)
_Commands tab_


### OpenOCD as a custom GDB server

To use OpenOCD as a custom GDB server, user needs to specify command line options
for OpenOCD. It is not necessary to specify any commands for GDB on the
 **Commands** tab, it will connect to OpenOCD automatically.

![Custom GDB server properties](images/debugging/custom_gdb/custom_properties.png)

  _Custom GDB server properties_

![Debugging using custom GDB server](images/debugging/custom_gdb/custom_debug_session.png)

  _Debugging using custom GDB server_

