# Processes

A process is a running program managed by the operating system. It provides an isolated address space and resources such as open files, while containing one or more threads that execute instructions.

## Curiosity questions and answers

### 31. Who receives the `python app.py` command?

Usually the command-line shell receives the text after you press Enter. It resolves `python` using its command lookup rules and asks the operating system to start the Python executable with `app.py` as an argument. An IDE, task runner, or other launcher can perform a similar role.

### 32. How does the operating system know where Python is?

The shell searches locations configured in the environment, commonly the `PATH` variable, or uses an explicit path or shell alias. The operating system then loads the selected executable. Virtual environments and environment managers can change which Python is found.

### 33. What is a process?

A process is an executing program instance with its own virtual address space, security context, and operating-system-managed resources. Two launches of the same script normally create separate processes, though they can communicate through files, pipes, sockets, or other inter-process mechanisms.

### 40. What happens when the program crashes?

A crash may be an unhandled exception, an explicit exit, or a severe fault such as an invalid memory access. The runtime or operating system reports or records the failure, stops the affected execution, and releases process resources. Other processes generally continue; a supervisor may restart the failed service. A crash does not automatically undo changes already written to files or databases.
