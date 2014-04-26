
                                                               [Page 1 of 13]








         This file contains late-breaking news about the FST software
         changes that were not available when the manual was printed.
         For this reason, they are not documented in the manuals.
         Unless otherwise labelled, information applies to all Version 3.1
         FST packages. (Information that is only applicable to special FST
         packages is appropriately labelled.)









                                                               [Page 2 of 13]

                     1. Installing the software
                        þ Creating a project path
                        þ Changing the monitor type and mouse type
                        þ Configuring the printer
                     2. Allocation list editor
                        þ Free entries
                     3. Importing files
                        þ File types
                     4. FPC online mode
                        þ The main menu
                        þ Modification of the configuration byte
                        þ Erasing the FPC 405 memory
                        þ Selective program start
                     5. Fieldbus configurator
                        þ Reading and loading the configuration
                        þ Changing the configuration
                        þ Split addressing of I/O modules
                     7. Fieldbus functions of FST 202 C
                        þ Release V 3.11
                     6. Miscellaneous


                                                               [Page 3 of 13]

         1. Installing the software

         þ Creating a project path
         In the FST configuration you can enter a project directory
         that does not exist for the function "PC configuration".
         The project directory will be created automatically after
         the confirmation prompt. It is not necessary to create this
         project directory with the DOS command MD (make directory).
         (See manual Section 2.2.1 PC configuration.)

         þ Changing the monitor type and mouse type
         In the PC configuration, enter M for a monochrome monitor
         or F for a color monitor. After changing the monitor type,
         the monitor adapter, or the mouse type you have to exit
         the configuration with F8 and then you must restart FST
         in order to make the new configuration valid.
         (See manual Section 2.2.5 Quitting configuration.)





                                                               [Page 4 of 13]
         þ Configuring the printer                             

         In the printer selection menu there is also the entry
         User-specific. Select this entry if your printer is not
         supported by the FST software. Then, after activating the
         function "Printer characters" you can enter the control
         characters of your printer. The control characters for
         the EPSON FX 80/81 are entered as default values.


         Also, the default control characters for each printer are
         available at any time. If you change the printer characters
         for your printer, these are stored separately. When selecting
         a printer, you can then choose whether you want to use the
         default values or your changed values for the printer during
         printing.
         (See manual Section 2.2.4 Selecting printer type.)






                                                               [Page 5 of 13]
         2. Allocation list editor                             

         þ Free entries
         In order to allow better management of the allocation list,
         you can use the "Free entries" function to find out how
         many entries are still available. You can activate this
         function with F7 within the allocation list or with the
         Extended commands in the STL or LDR editor. The free space
         is also related to the amount of memory installed in your
         computer.


         The number of entries remaining available depends on the
         size of the RAM available for the allocation list. For
         this reason, the LDR and STL editors show a smaller number
         of free entries, as the programs themselves require RAM.

         (See manual Section Chapter 4 under Allocation list)





                                                               [Page 6 of 13]
         3. Importing files                                    

         þ File types
         In addition to programs and program modules, other types
         of FST file can be imported into a project or LIB directory.

         For example: - Allocation lists       (*.BEL)
                      - Project documentation  (*.DOC)
                      - Display files          (*.ANZ)
                      - Position control files (*.LAR)
                      - Make files (drivers)   (*.MAK)
         Make files can only be imported into the LIB directory.
         After selecting the destination directory you are presented
         with a standard input mask. The file extension OBJ is
         generally entered as a default. First enter the correct file
         extension for the file to be imported. After confirmation,
         the input mask changes according to the type of file.
         (See manual Section 3.9 Importing files)





                                                               [Page 7 of 13]
         4. FPC online mode                                    

         þ Change of the configuration byte (FST 101 only)
      	The initial menu of FST 101 can be changed with Function key F6 of
         the operating mode (the configuration byte). By pressing F6, you can
         select between EPROM operation with or without battery or RAM
         operation. The operating mode only takes effect after the FPC 101
         has been switched off and back on. The currently valid configuration
         is indicated in the initial menu.
         þ The main menue
         The FPC online mode main menu for the FPC 405 provides
         information about 3 levels of memory.











                                                               [Page 8 of 13]
         These are
         - Largest memory area: shows the size of the largest
         contiguous memory area. The largest control program to
         be loaded must not exceed this size.
         - Total free memory: shows the total amount of memory
         available for control programs.
         - Free memory for programs: shows the amount of memory
         available for data files that can be addressed by BASIC
         programs.
         (See manual Section 7.1.2 Entering on-line mode)













                                                               [Page 9 of 13]

         þ Erasing the FPC 405 memory

         After activating the function "Reset FPC" (F4) you can

         - Erase programs
         - Erase data files
         - Erase entire memory contents
         (See manual Section 7.1.3 Scope of Delivery)


         þ Selective program start
         The functionality for selectively starting and stopping of
         programs has been added to system status. After activating
         the function "System status", you can select a program with
         the cursor keys. The selected program is highlighted. You
         can then toggle between start program and stop program with
         either the Enter key or with function F4.
         (See manual Section 7.2.7 Static display of system status.)




                                                               [Page 10 of 13]
         5. Fieldbus configurator

         þ Reading and loading the configuration
         During NOMINAL-ACTUAL comparison without a NOMINAL configu-
         ration, the ACTUAL configuration is read and stored as the
         NOMINAL configuration. Loading the NOMINAL configuration
         also causes the NOMINAL configuration to be stored. Please
         note that after activating the function "Abort edit" only
         the last-saved version of the configuration file remains
         available.

         þ Changing the configuration
         The FPC must be erased after every change to the fieldbus
         configuration in order to prevent switching errors on the
         fieldbus. The first creation of a NOMINAL configuration or
         reading of an ACTUAL configuration also requires erasing of
         the FPC memory. If you load a changed NOMINAL configuration, a
         prompt appears asking whether you want to erase the FPC memory.
         You can initiate erasing of the controller by entering a Y.
         (See manual Chapter 8, Fieldbus)



                                                              [Page 11 of 13]
         þ Split addressing of I/O modules                    

         If a 405 Remote Pack is equipped with a mix of E.CEA-1616
         and E.CEE-32 or E.CAA-32 cards, gaps may occur in the memory
         area of these participants.
         When configuring these participants in the fieldbus configu-
         rator you must enter the number of I/O units as if there were
         no gaps.

         Example:
         E.CEA-1616  (System address, 0; IW0; OW0)
         E.CEE-32   (System address, 2; IW2; IW3)

         IW1 represents a gap. In the configurator you must enter
         that 4 IWs and 1 OW are present.








                                                              [Page 12 of 13]

         6. Fieldbus functions of FST 202 C

         þ Release V 3.11
         The programming software FST 202 C is extended by fieldbus
         functions. All modified programs are identified with the
         release V 3.11. The PLC programs of the release V3.1 are
         further valid.

         Please regard the messages on page N-9 (What is new?) of
         the FST manual and the following device descriptions:

                 SB-202  no. 18371-GB
                                         and
                 SF-202  no. 18373-GB








                                                              [Page 13 of 13]
         7. Miscellaneous                                     

         þ Text and STL editor (changing a search path)
         When saving or reading a block the function "Change search
         path" allows you to change not only the filename, but also
         the complete pathname. By overwriting, you can change the
         drive, the directory path and/or the file extension.

         (See manual Section 5.1.2 Block commands)

         þ Program modules
         The FPC 404 does not allow LDR program modules to be created.
         (See manual Section 4.1.1 Creating a new program.)

         þ BASIC Compiler mode (only FST 405):
           Now you can also use the compiler mode for BASIC programs -
           in the manual announced as "not yet avaiable".
           (See manual Section 4.1.1 Creating a new program.)





- End of README -
