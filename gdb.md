# My Wiki for GDB

## Most common commands
- backtrace [StackTrace]            Shows all functions called until current point
- run                   (or r)      Starts the program being debugged.
- next      [step Over] (or n)      Executes the next line of code, stepping over functions.
- step      [step over] (or s)      Executes the next line of code, stepping into functions.
- continue              (or c)      Resumes execution until the program stops or a breakpoint is hit.
- quit                  (or q)      Exits GDB.

### Break Points
- break                 (or b)      Sets a breakpoint at a specified location.
- info breakpoints      (or i b)    Lists all active breakpoints.
- delete breakpoints    (or d b)    Deletes a breakpoint.

### See Variables or Command Info
- display <expression>              Displayed value of expression at breakpoints
- list                  (or l)      Displays the source code around the current line.
- watch                 (or w)      Sets a watchpoint on an expression.
- x                     (examine)   Examines memory at a specific address.

- print                 (or p)      Prints the value of an expression.
    - `print <var>`                 Prints variables in current scope
    - `print locals`                Prints every var in local scope
