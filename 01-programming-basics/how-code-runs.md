# How Code Runs

Computers execute machine instructions, but people usually write source code in a higher-level language. A language implementation translates or interprets that code, and the operating system provides access to files, memory, and devices.

## Curiosity questions and answers

### 4. How does a computer understand `if`, `for`, `while` and `function`?

These are language constructs with defined meanings. A compiler or interpreter parses their syntax into an internal representation and implements their behavior using machine instructions and runtime support. An `if` chooses a path, a loop repeats work, and a function groups reusable behavior; the processor itself does not recognize the English words.

### 10. What actually happens when you run a program?

The shell or launcher asks the operating system to start a program. The OS creates a process, loads the executable and required libraries into memory, and schedules its threads. If the program is written in a language requiring a runtime, that runtime loads or translates the code. The CPU executes instructions; the program may request files, network access, or other services through the OS. Output is sent to a screen, file, or another destination, and the process eventually exits or fails.
