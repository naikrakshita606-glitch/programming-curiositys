# Threads

A thread is a path of execution within a process. Threads in the same process share memory and resources, which makes communication convenient but requires care when they access shared state.

## Curiosity questions and answers

### 34. What is a thread?

A thread is an execution sequence the operating system or runtime can schedule. A process can have multiple threads to make progress on concurrent work, such as handling requests while waiting for I/O. Shared data can cause race conditions unless access is coordinated. Python's Global Interpreter Lock limits simultaneous execution of Python bytecode in a thread in standard CPython builds, but threads can still help with I/O-bound tasks; other implementations or builds may differ.
