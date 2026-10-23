# Interpreters and the Python Virtual Machine

An interpreter is a program that executes code according to a language's rules. Real language implementations often combine parsing, bytecode, interpretation, and just-in-time compilation.

## Curiosity questions and answers

### 35. Where does the Python interpreter run?

The Python interpreter is itself a native program running as an operating-system process. It uses the CPU and memory like other programs, and it asks the OS for services such as reading files and writing output.

### 36. How does Python read your `.py` file?

When asked to run a script, Python locates and reads the source file, decodes it as text, and parses it according to Python's grammar. It then compiles the parsed code into code objects, commonly represented as bytecode, and executes them. Details vary by implementation and version.

### 37. Does Python directly understand its source code?

The Python implementation understands Python's grammar and semantics; the CPU does not directly understand Python source text. The implementation parses and compiles source into an internal representation, then executes it using its runtime and machine instructions.

### 38. What is bytecode?

Bytecode is a lower-level instruction format for a virtual machine, between source code and native machine code. CPython commonly compiles Python source into bytecode; cached bytecode files may speed later startup, but they are version- and implementation-specific and are not the original source.

### 39. What is the Python Virtual Machine?

The Python Virtual Machine (PVM) is the execution component that runs Python code objects, including bytecode in CPython. It is part of the interpreter implementation, not a separate physical computer. Other Python implementations can execute Python semantics differently.
