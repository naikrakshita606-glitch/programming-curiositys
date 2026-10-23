# Garbage Collection

Memory management reuses memory when data is no longer needed. Python manages ordinary object lifetimes automatically, but programs still need to release external resources such as open files and network connections explicitly.

## Curiosity questions and answers

### 20. Who cleans unused memory?

The language runtime and memory allocator manage most object memory; the operating system manages the process's address space and physical-memory allocation. In CPython, reference counting often reclaims objects promptly, and a cyclic garbage collector handles groups of objects that refer to one another. Other Python implementations may use different strategies.

### 28. What is garbage collection?

Garbage collection is runtime work that finds objects a program can no longer reach and reuses their memory. It reduces the need for programmers to free every object manually, though it does not guarantee that memory is returned to the operating system immediately.

### 29. Why doesn’t unused memory remain forever?

Reclaiming unreachable memory lets a process reuse it for future objects and prevents unbounded growth in long-running applications. “Unused” means the program can no longer reach the object; an object still referenced by a cache or global variable is not garbage, even if the program no longer finds it useful.

### 30. What happens when your program consumes too much memory?

The operating system may reclaim caches, move data through virtual memory, slow the program, or terminate a process when memory is exhausted. The program may also receive an allocation error such as Python's `MemoryError`. Large memory use can result from genuinely large data or from retaining references unintentionally; profiling and bounded data structures help identify and control it.
