# My Wiki for GDB

## Most common commands
- `backtrace`   --shows all functions called until current point
    - AKA stack trace

- `next`        -- skips to next command in current file
    - AKA step over

- `step`        -- steps into the current command or over if not a function
    - AKA step into

- `cuntinue`    -- continues the run after a breakpoints

- `display <expression>` -- displayed value of expression at breakpoints

- print
    - `print <var>`   -- prints variables in current scope
    - `print locals`  -- prints every var in local scope
        - `set print pretty`
        - `set print elements <num>` -- the number of elements in an array to print
        - `set print addrase`        -- prints the memory address of with values
        - ....
