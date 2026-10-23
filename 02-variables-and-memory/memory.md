# Memory

Memory is the working space a running computer uses to hold instructions and data. Main memory (RAM) is fast and temporary; storage such as an SSD keeps data across shutdowns.

## Curiosity questions and answers

### 21. What is RAM doing while your program runs?

RAM holds the program's active instructions and data so the CPU can access them quickly. The operating system gives each process an address space, tracks its memory use, and manages access to physical memory. RAM is shared by the system, not reserved exclusively for one program.

### 22. What is the difference between RAM and storage?

RAM is working memory: it is fast, usually volatile, and holds active data. Storage is persistent and keeps files when power is off, but is generally slower. Programs and files are typically loaded from storage into RAM before the CPU uses them; virtual memory can extend the address space using storage, but it is not a substitute for RAM performance.

### 23. Where does a Python variable live?

A Python name exists in a namespace maintained by the interpreter, and it refers to an object. The namespace and object occupy memory in the Python process, but their exact locations and representation are implementation details. Some data may be temporarily optimized or stored differently internally.

### 24. What is a memory address?

A memory address identifies a location in an address space. A process uses virtual addresses, which the operating system and hardware map to physical memory. Addresses are meaningful within a process and over a period of time; they are not generally permanent locations.

### 25. Why can’t we normally see memory addresses in Python?

Python is designed to let programs work with values and references without managing raw addresses. Hiding addresses makes code more portable and helps the runtime manage memory safely. Tools such as debuggers and implementation-specific functions can expose identity or address-like details, but those details are not stable or a safe basis for program logic.
