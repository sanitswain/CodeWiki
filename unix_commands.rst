Useful UNIX commands
====================

VI Commands
-----------

**Modes of operations**
  
The **vi** program has 3 modes of operation.

#. **Command mode:** All the commands pressed in this mode are interpreted as editor commands. 
   For example if you hit **dd** it will delete current line. Commands pressed in this mode will 
   not be visible to users.

#. **Insert mode:** This mode permits insertion, editing or replacement of existing texts.

#. **Ex Command mode:** This mode allows to enter commands at the command line. 
   The bottom line of **vi** screen is called command line. All the commands entered in this 
   mode are displayed in the command line. Ex-commands should be prefixed with **:** (colon)


**Block commands for editing**
  
Block commands are operated on multiple lines.

.. list-table::
   :widths: 30 70
   :header-rows: 1

   * - Command
     - Function
   * - :nd
     - Deletes **nth** line.
       Example: **:5d** deletes 5th line
   * - :m,n d
     - Deletes line from m to n.
   * - :n mo p
     - Moves the line n after line p.
   * - :m,n mo p
     - Moves line m to n after  line p.
   * - :m co p
     - Copies line m after line p.
   * - :m,n co p
     - Copies lines m to n after line p.
   * - :m,n w filename
     - Write lines m to n to a file.
   * - :m,n w >> filename
     - Appends lines m to n to a file.
       

**Find and Replace**
  
Following commands are used to find a pattern and replace with new string. These commands should be executed in ex-commands mode.

.. list-table::
   :widths: 25 75
   :header-rows: 1

   * - Command
     - Function
   * - :s/str1/str2
     - Replace first occurrence of **str1** with **str2** in current line.
       Example: **:s/cmd/command**
   * - :s/str1/str2/g
     - Replace all occurrences of **str1** with **str2** in current line. 'g' stands for global.
   * - :m,n s/str1/str2/g
     - Replace all occurrences of **str1** with **str2** in from lines m to n.
   * - :1,$ s/str1/str2/g
     - Replace all occurrence of **str1** with **str2** from 1st line to end.
   * - :1,. s/str1/str2/g
     - Replace all occurrence of **str1** with **str2** from 1st line to current line.
   * - :.,$ s/str1/str2/g
     - Replace all occurrence of **str1** with **str2** from current line to end.