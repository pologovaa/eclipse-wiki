1. Creating C project
    
  ![C Project for nSIM debugging](images/C Project for nSIM debugging.png)

    _C Project for nSIM debugging_
  
2. Choosing nSIM gdbserver under Debug Configuration
   
   ![Choosing nSIM on debug tab](images/Choosing nSIM on debug tab.png)
    
   _Choosing nSIM on debug tab_

   In this tab, user need to indicate correct properties file/TCF file for
   current CPU core. In general it is recommended to use TCF files, because
   they are generated from the Build Configuration Registers and thus most
   reliably describe target core. nSIM Properties files contain list of
   key-values for nSIM properties which allow to describe target core and
   additional simulation features, full list of properties is documented in the
   nSIM User Guide.  It is possible to specify both TCF and properties file,
   with properties file being able to override parameters set in TCF. For
   example, if you have a TCF for a little endian core, but would like to
   simulate it as a big endian, it is possible to create an properties file
   that will set only a single property for big endian, then in IDE GUI in nSIM
   GDBserver settings specify bath to both TCF and properties file and that
   will give a desired results.
   
   ![Choosing proper properties file for nSIM](images/Choosing proper properties file for nSIM.png)

    To see output from the target application, go to **Common** tab and check
    "Allocate console (necessary for input)".

    ![Check “Allocate console” in Common Tab]
    (images/Check “Allocate console” in Common Tab.png)

    _Check “Allocate console” in Common Tab_

   _Choosing proper properties file for nSIM_
3. Debugging an ARC EM C project

To debug application using nSIM, press "Debug" button of IDE.
    
   ![Start nSIM gdbserver debugging](images/Start nSIM gdbserver debugging.png)
    
   _Start nSIM gdbserver debugging.jpg_  
   
   ![Debugging with nSIM gdbserver](images/Debugging with nSIM gdbserver.png)
    
   _Debugging with nSIM gdbserver_

   ![Debug Window](images/Debug Window.png)
    
   _Debug Window_

   ![Open nSIM gdbserver properties](images/Open nSIM gdbserver properties.png)
     
   _Open nSIM gdbserver properties_

   ![nSIM gdbserver properties](images/nSIM gdbserver properties.png)
     
   _nSIM gdbserver properties_


   ![nSIM gdbserver output in console](images/nSIM gdbserver output in console.png)
     
   _nSIM gdbserver output in console_

